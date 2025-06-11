<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.27`](#composer11027)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.25`](#composer2225)
-	[`composer:2.8`](#composer28)
-	[`composer:2.8.9`](#composer289)
-	[`composer:latest`](#composerlatest)
-	[`composer:lts`](#composerlts)

## `composer:1`

```console
$ docker pull composer@sha256:71710191403da99f9ee23a5f4ce586615d5343cb8dc2fedc8ee6b02661d5e5f0
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
$ docker pull composer@sha256:4c53f0c3983068037d0ae5025f624a34e0161d07421903c621755cd7b79219f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76564511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a86750c1f342d7d0c03f934e0fab17d24792466052aa9d81071faeb6415eca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41ed00f4f69f9b33b5e886fedfa6143b6e95cd34c48de5a67dfca449d27075`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 3.5 MB (3468342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3dd3a928e1a1d32cf4174792bbec9d7d27add5d439d1765653b7fc22f66b92`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0721ec88e7a2844011b208a2272d18e4e309abd51c06c8e85a7fd685455524c`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f084ac2a53f05708a861a663438bea25fa87e41a10129b5c0a01e67aed1432c`  
		Last Modified: Wed, 11 Jun 2025 01:13:20 GMT  
		Size: 13.6 MB (13640521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87939f6f4e61218155cd7a88d809fc899e6d6a2b413033839baacad75def377a`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07468323dd1f0b8efa9f6be2eaf69811d60fee46c187e62fc1b05bd2bd100fa`  
		Last Modified: Wed, 11 Jun 2025 01:13:18 GMT  
		Size: 21.0 MB (20969804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d64e952347861cf8f1c360fcf1984249571751d095594a156d453d4cb4ec8b`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f854fc0d234074345274bcbda7bb11f7295b4bae6d7d400dcbe3bd892683a59`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860cdf46be6d7d1d3f8d39843f7297bfcad7f2061c5091785431569d5aef15a6`  
		Last Modified: Wed, 11 Jun 2025 01:14:30 GMT  
		Size: 33.9 MB (33928419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2417eb329e1350384f208e99d8a7b62dc527e52472c11398e054a99584d2cb0c`  
		Last Modified: Wed, 11 Jun 2025 01:14:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f74ea2dbf3bc0f243011cf49eded65284a6d0b6c30abc6b8933dd97beb5e96`  
		Last Modified: Wed, 11 Jun 2025 01:14:29 GMT  
		Size: 735.5 KB (735536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5097fdee9087545b7f49d7cfeb9e072b5f9938f2845d37c7eca15f7d41fc3c`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641cbabe81032e6beede3a4dc850d1fc1e44443f97c49a628393301c1f428062`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:f478ad00541c4e680716dd5adeff2e68ec2cc4d035d36e579f1125ea87ff37e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c78e654255109a0413537e2b175f5589c413d4c29bf54ea54b10c37362bed38`

```dockerfile
```

-	Layers:
	-	`sha256:fbd8ab339738c2150419d7f3e94805ec8ab44f5bac15d330cb352596388d9d01`  
		Last Modified: Wed, 11 Jun 2025 04:13:31 GMT  
		Size: 2.2 MB (2173838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31904e69e1fd6f3ec041500925a0ba8027ae489d72b979c14fc0abfb2463657a`  
		Last Modified: Wed, 11 Jun 2025 04:13:32 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:20279bcf5818513330f8831adbdb201fd22560a21fcb21e68a26b112daa6d255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74233398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2fc11a754f1feb9ae36681f641c64515252e49e5ca543c2cf1035ffb26bd77`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d738e6a7e1662efb7b90b7f0a4b2cce2f9247f395ab8c1924148a0d2dde272c3`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 13.6 MB (13640499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeec31f51dc18a99c6251ab6abd48a6b17b9bd04c498ca1ce606fbe0119a506`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a9bea01d63368fc6a169811ad55c9f7baf8d06c4a3c909bea5606bf5d161c`  
		Last Modified: Tue, 10 Jun 2025 23:54:15 GMT  
		Size: 19.1 MB (19091501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab1a6cbed4c7bce681ea2c1ba6335b04364d328abb8504ac38b7cb01546c1e`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7ac6548196a7241e2ff5aeb2ebaa92bd912151a57decbc09707501826e55d`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 20.0 KB (19986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a52088bfe28e3394348499664afc0150422c289f500eeb5736a846fb654a75`  
		Last Modified: Wed, 11 Jun 2025 01:34:01 GMT  
		Size: 33.8 MB (33807058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfadb48984526f1d970423f530584b05a533cf586b26af60f4077fe0d75af65`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf9ff0c926fffcd87f7c6e5cfb7a725d493067ba9283b2c1efddcbb53a1402`  
		Last Modified: Wed, 11 Jun 2025 01:34:42 GMT  
		Size: 736.1 KB (736126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51378ea70fd28d9aac94ff703323e73b3fbd24fbe401f0d32312160954168a2b`  
		Last Modified: Fri, 06 Jun 2025 18:42:25 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d765cf697fdc1cd49a825bc745561e714e462f63b61d2d3bb2b2db4aa91a55`  
		Last Modified: Wed, 11 Jun 2025 01:34:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:b65b6f7284622c7326cf3c0db5c7a85c18b9f169d085590651d752e28a3f8dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7667b1ab7acf4853718556822f307bcea5fed1ee9dc872234b106e10d4bf1c6`

```dockerfile
```

-	Layers:
	-	`sha256:f58d6aee9b7d0600d675290fe75755c44222821eafa2959a5153b91a7a412d52`  
		Last Modified: Wed, 11 Jun 2025 04:13:36 GMT  
		Size: 30.3 KB (30296 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:7899db68c464d1ef59c2906c8b15f7ead98141e355c2f9f2ead0104cadb406c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70995356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171861bcb6abf6fd32629fc7e96e657d07e27461a4cc7b1ff62a441190300847`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc30cbedbf54d9515871da07398fab0a70176613fac2230d3b598dd61f7dea64`  
		Last Modified: Wed, 11 Jun 2025 11:39:15 GMT  
		Size: 13.6 MB (13640514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ce30718845b98da85d3f2d4b2a979b2c4c9a318019ee4c5a3897dbb7a35b7`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788f675ffad6ad044155d5d8863ebb06f9142fe48298e02c274f65b961260418`  
		Last Modified: Wed, 11 Jun 2025 11:39:16 GMT  
		Size: 18.1 MB (18066806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2746b1c3debbab52b7827813726cffe0c2a6316b37ceefd0c7c7085cb9219577`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60271e3bc7668883349e90adf3ad21e0a859246f2f3d1430bd66ba8532b8cc1`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 20.0 KB (19984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bab94d85f8d4b9a1b97076f46ba751dc69827e8eaeb013290df1d46760098`  
		Last Modified: Wed, 11 Jun 2025 19:24:25 GMT  
		Size: 32.1 MB (32069944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d696523fff13201849f3282a4e284e28727f89ba185ff8bdb03a58fc314ccb55`  
		Last Modified: Wed, 11 Jun 2025 18:47:28 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35831c7ef69580355c4bb571b10c0df79cced513d276a1447723ffb9504869c8`  
		Last Modified: Wed, 11 Jun 2025 18:21:10 GMT  
		Size: 726.6 KB (726612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48006c8e93aaa7de2d158ea6c63a66aaa8fb263c40af5569c0fb94f036ae158d`  
		Last Modified: Wed, 11 Jun 2025 18:21:10 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7032c03fb42068e4949481bbd4be3be1f665e7a82c3a933a2a05576ddb8542df`  
		Last Modified: Wed, 11 Jun 2025 18:21:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:e4911230caf8b6f49835f9ce0d5aab76795b9641674f35d57346f40c54c0d808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c147bad3161baf64fa74a22365f15e8966fa9a74044b7dbef71a98f4f2cd1d`

```dockerfile
```

-	Layers:
	-	`sha256:4e3a0048403d9f55c2827fe342a857dce79b273373bbce34ce9f5966c342ddb1`  
		Last Modified: Wed, 11 Jun 2025 19:13:28 GMT  
		Size: 2.2 MB (2174154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a4c52a5df2729767b1dc823b38cce3fe92c907a2dd74cd9d5f8dc1225f7666c`  
		Last Modified: Wed, 11 Jun 2025 19:13:29 GMT  
		Size: 30.5 KB (30511 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:9ed447b7de769153bff4e0bc259dcdcfa950d8bcc26159660fbb55f7c01630d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76537210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f7de927ebb4f8985451bf78352f7e70ca2e3c379f8ab55bc851bcd276fc939`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e263556d24cfaaa81ec9153b95e1b25d54abdb35b46c3c74fa988a9f252f3`  
		Last Modified: Wed, 11 Jun 2025 09:16:54 GMT  
		Size: 3.5 MB (3470681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5bea448bb73ac691df99daf5772e7cb7307f122b4e0544c289a55be9ee24`  
		Last Modified: Wed, 11 Jun 2025 09:17:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a64acbbc8d220ea4c16baed763b26899f58299a8b85d3b8513f03b3023893`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123dcf4adf55a39c8cf4f202302f0a9dfd6d576c94bf8db94686e5a5ee1f4cf4`  
		Last Modified: Wed, 11 Jun 2025 09:33:08 GMT  
		Size: 13.6 MB (13640507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff08fc5740a571af506cddc0c38e20506f6151e574d4a10d77b748c7c3bd4b`  
		Last Modified: Wed, 11 Jun 2025 09:08:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc080435edc41cfa70a84f9586ffca3f880a9b4cedccc53c481889b18e1e1c2`  
		Last Modified: Wed, 11 Jun 2025 09:33:10 GMT  
		Size: 20.5 MB (20518887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3995038baa7f047e93509966aa2798fbc7bddf48517c43343b9add69edd5df`  
		Last Modified: Wed, 11 Jun 2025 09:08:59 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae69002966a0d0881786cca5d1dfa7b1fb54c0e7b1e4b6bf9c41f92f6208ec`  
		Last Modified: Wed, 11 Jun 2025 09:17:23 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5db0ec87df386dd8e7ed3e3a943ff4f92de4b419fe7f9bb1b4051dd24a6721`  
		Last Modified: Wed, 11 Jun 2025 15:13:38 GMT  
		Size: 34.0 MB (34010836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae1182fb6a9705ef49f6995317dfcfc6ef3d4b2292bc160d0ba7f8c246dda2e`  
		Last Modified: Wed, 11 Jun 2025 15:13:33 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d035e6ddd2f2b3ec3b75c60a418c5edd649b9e313a6bb9e5e7773ba65e752fb`  
		Last Modified: Wed, 11 Jun 2025 15:14:15 GMT  
		Size: 735.5 KB (735525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c87c5ee74b70a3f06c4198ca30f242c8f86f4da742fa485fc832839f15d66ed`  
		Last Modified: Wed, 11 Jun 2025 15:14:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70801ea2d0c992556c4485255efc32138f222c98823d965aaa17a8310c061f7c`  
		Last Modified: Wed, 11 Jun 2025 15:14:14 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:6d3c24b55e1a06c20901c37c28b0608aa905a2e24610daeeb7c9d04e9deb04ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ceb0ce8799fa17d423d608b8fd00d8d068a3716660186f4afaaa84a81386fb`

```dockerfile
```

-	Layers:
	-	`sha256:70a2c138ed0dcae3ceb6cb26356205083bc719e4ee6f4808e2c5977387e0e60f`  
		Last Modified: Wed, 11 Jun 2025 16:14:29 GMT  
		Size: 2.2 MB (2173978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4e4d7f1ec86be9db7404583ea0e16101f3e3a930504b89a937c451afa277ab`  
		Last Modified: Wed, 11 Jun 2025 16:14:30 GMT  
		Size: 30.5 KB (30539 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:c931c43b30b90ffa516a08c25e05ef4da2830208b91b340f6db6b671ad194a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77486369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4685a639678296eb95b2c1f87add779cb15ae1b1b99a242c2f35c073c3a63ea2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298f020aec5b2eb58f3f5d72ed081bd6c76a95799b7e438e4f3384447e42693d`  
		Last Modified: Wed, 11 Jun 2025 01:13:13 GMT  
		Size: 3.5 MB (3527774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ebeb8397f1f59382fb3bd2f49e7ae5aa3c63f7a6f5adde3d5af0fe196ad48`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c3fa431069cd36b1283a6dd73ec3c559701f45df22999775e61dd0dd4d578`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7db0fb8a413bd77d83d365246beba56a6d3ab745a296bb3119dd1c4844e7e2`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 13.6 MB (13640494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c81720a5bbf56ccfa06979187dbca8afa1859fb3d323625fe188373b9a06ed`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8fb25f24bc12988d302f27fbc0c27090c75c814e4f8dcb4396e125eafae7cb`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 21.5 MB (21493036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b67d63641d3800bf94c0e5eb453a80e9e00ec38acbc41e8b2dbe883e470dd6d`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821e028fb8ab3dacea139b63763d5d53b2d0981367d47fcd3f94182a0a2ac456`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 20.2 KB (20182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5a5771e66b8b5e97c3a2a977ca7089edbbca018038d8b56551bbbc0a8d6d01`  
		Last Modified: Wed, 11 Jun 2025 01:14:24 GMT  
		Size: 34.4 MB (34436667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d09bf8efac1bb2cb2458be039d96f810d55feb69816e0ae630509068dac26`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063d9bef4e56fa69cf33904760f4b8a2f1d7ce9202307e5ab7ceebf791d361f8`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 747.3 KB (747342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5097fdee9087545b7f49d7cfeb9e072b5f9938f2845d37c7eca15f7d41fc3c`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387efffd50fee23b95960319fa3959d346523333031fe1d80e9259d8eaa96a01`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:7bfabce3d40ae9cd2ffe1c3af8a88e3982a81a513f446328bd8e147aa8820688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99944fb53daf14ff0eee173447232e4dba802c0c847264e95f3572a37b733a06`

```dockerfile
```

-	Layers:
	-	`sha256:bdcfb0ffcb7c6b897ce1b98f040a3a0448451a4ef0f435242338c7d26870cc50`  
		Last Modified: Wed, 11 Jun 2025 04:13:49 GMT  
		Size: 2.2 MB (2173626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3c212fd7248554662d6a514fe1bcb0ad2719dd3cf20d75e5f74404172681c28`  
		Last Modified: Wed, 11 Jun 2025 04:13:50 GMT  
		Size: 30.4 KB (30386 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:13ea0fc5522c5ed3ab51d3d2cfed1000e4408455702be521a0c258f2851d07f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78910180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5470486ae40a27b00e10ebf16e30162c97cb75bb126a462d352afd2e799a1c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeaaf729ae44f9ac3f9b3f4551595556a417993152b53954f6f6a89f90a4954`  
		Last Modified: Wed, 11 Jun 2025 09:12:57 GMT  
		Size: 13.6 MB (13640505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928f2bed6e9375b5161e1fcbc32d598a194fc67da4a537c5d6a3aaab21aa3d0`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f75742ee54512415191653f6d3e2b7b2a4ff66bc4dcc60a24c12d00a0db76`  
		Last Modified: Wed, 11 Jun 2025 09:12:58 GMT  
		Size: 21.9 MB (21874047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189ddb23dd34f7e52d4b584e89ed11029f27d1dee76f138e62d772e61c75c0b6`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c88f7798e99a903cbf372177b9f7b8f2c70690f8dac0d589ec956038b045f`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a315ceb76a2ac2dda2c8bd167ee4d021a2f0885e86b42406a0c9eb02fb75b9e`  
		Last Modified: Wed, 11 Jun 2025 19:17:11 GMT  
		Size: 35.3 MB (35278992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197c9bbd782fcb082df2515b2222b6e5b48b183fca060886fc83d969d7daf6a`  
		Last Modified: Wed, 11 Jun 2025 19:17:08 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab01f9e69af64380336278b102d19cb9b79bb1e44ec420dbf8dc35ba490efd7a`  
		Last Modified: Wed, 11 Jun 2025 19:17:49 GMT  
		Size: 742.5 KB (742453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955d854b102f56238a18f4a89a2c22c5b722fc4858215da1cb3f658c158e82ac`  
		Last Modified: Wed, 11 Jun 2025 19:17:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe112e2374db26b2488d2a392933f334abe3f348f2f6d812a8c44bd78aa3e9d`  
		Last Modified: Wed, 11 Jun 2025 19:17:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:16e916224447f736b57c62b6cdf6bfdb544805d8289c2e13ebc4a658f0cc2990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c675920a44dfa4f1ff54eb4d3dfceca1a03a12563a2892854b28f2e417dab3`

```dockerfile
```

-	Layers:
	-	`sha256:c1a677b4e0534afc87f8bd8b2a044a4833daf0816eed4a5d159d437b690d4c8a`  
		Last Modified: Wed, 11 Jun 2025 22:13:35 GMT  
		Size: 2.2 MB (2172395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41d3b25ebe3fd471a8f0bb887db2c1d4dc3c097a3f097794ec59faba6a8ef463`  
		Last Modified: Wed, 11 Jun 2025 22:13:36 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:5621e50b235a59b8c69976cb12497086899daf383a9f2387fcac2f460308a6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73012087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a013faef78749ce18cec25c1e2a66f2c0df7a86cdc76c2ecf1eb1668d4bfcf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba389b9b1d6d27f7a263c92d52685675ded66f85f52a097bec1b658400eebc5`  
		Last Modified: Wed, 11 Jun 2025 02:39:58 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb4f8cea261544e7d849e5aa9581396ef8d4bd1b7c14ceb536acc047c9ff257`  
		Last Modified: Wed, 11 Jun 2025 02:40:00 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d9086703155ae9ef802a8a0d3e98de9aabdf18c7eb07d7758e92bef886259`  
		Last Modified: Wed, 11 Jun 2025 14:10:42 GMT  
		Size: 31.1 MB (31107690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b0b41c4564a3bd6fb68327d016b7b9e8acab85e9d3bf36c289ab0ca8ce1509`  
		Last Modified: Wed, 11 Jun 2025 14:10:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e8e2aad51b270919d00a8fe3370667b4acf4d40bc259e8405e1e98caa6ec`  
		Last Modified: Wed, 11 Jun 2025 14:20:34 GMT  
		Size: 733.3 KB (733285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619ca568e26bd59a624f3efad0fb970dc1c1cd1c759e29ea0f76f5e41d0f1d0f`  
		Last Modified: Wed, 11 Jun 2025 14:20:34 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b551e410dbc4ba1533ca034710366ff88c5f38eb054838d5acbb233aa0c59360`  
		Last Modified: Wed, 11 Jun 2025 14:20:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:2765c553acb5e422fc9bd56345ed25d5d0c827fefa1342505926c555fb9e4bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee68a0f763af2ce7d70f1f0f8e9dcdabaf134609d7908d1be471c866910af6fb`

```dockerfile
```

-	Layers:
	-	`sha256:249e2c285a2c9be43c98dea78f964f76f84afafffc235a47b059fdaebee0c8a0`  
		Last Modified: Wed, 11 Jun 2025 16:14:39 GMT  
		Size: 2.2 MB (2170662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e733ed7787fb847005cc32eea74c9e170cf49a1ee1436b4166d587627cff1381`  
		Last Modified: Wed, 11 Jun 2025 16:14:40 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:e3c80ca5a4116ac2671ef315c8b0f82b809a2fa6d145fb47ba594b1f4052e6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75036696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f03ddf3fd969299650f1d100ba587fa0d82061b05ab2734774e7384ef049be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035d42a37d5be6b1617300170ead6ce8970a5e2e4154fe287efc8af1e2f7441`  
		Last Modified: Wed, 11 Jun 2025 08:13:18 GMT  
		Size: 13.6 MB (13640519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca62563344c489947dce07a51fbce42cb5c2f338f525f3dc64a869bb23eea05`  
		Last Modified: Wed, 11 Jun 2025 06:17:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12b2d32a5b3932415a1a3b75f1dce848914c79f4be0b381c79061048ef8945`  
		Last Modified: Wed, 11 Jun 2025 10:56:19 GMT  
		Size: 21.4 MB (21446797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13957f45dfaafb933ab00f3283ea48d057cd2179a84687ebe45ad163f535de`  
		Last Modified: Wed, 11 Jun 2025 06:17:35 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48dd1edbbaf646c03ef3f286cc921fbc422e665578b988b9d03d890364f0d5`  
		Last Modified: Wed, 11 Jun 2025 07:14:21 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7301cbc0841ac3202a1b74a41aa6043f1d38879737a0da5c17da8e63aa32c2`  
		Last Modified: Wed, 11 Jun 2025 11:04:18 GMT  
		Size: 31.8 MB (31839063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae5612a3f46089fbce6bbf1de47ad49c5c4c6be46ad9e038f366a967187ab7`  
		Last Modified: Wed, 11 Jun 2025 11:04:10 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e197005d164da5b36acfa623b1a069914b6bacc27101eb05c08f8f5fd5a4c39b`  
		Last Modified: Wed, 11 Jun 2025 15:34:16 GMT  
		Size: 739.0 KB (738955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680555285dbd83e3be42aeb005ae570f5ff1b5eaba5768a244d0bade965d8a02`  
		Last Modified: Wed, 11 Jun 2025 15:34:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4c35a9662ffb17a097e48f01c2d0845aaf10492f17ecd5817ec9ff656bcb05`  
		Last Modified: Wed, 11 Jun 2025 15:34:16 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:050a6da2bec725aa6dc3a351946d020713c887b51087bee6d6c4501189633bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e563acc207b8e53760cf9517b2184d6041b6da8b3275bc23f254220bb442f9de`

```dockerfile
```

-	Layers:
	-	`sha256:e102856ffe80ca255ecd65446faf4798b6fad772c5ea22d21f9655b26f510cfb`  
		Last Modified: Wed, 11 Jun 2025 13:13:39 GMT  
		Size: 2.2 MB (2170450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed36825c442dab5cf11d326c01ec64c30cf744a8c5edfa107e9dc397ba146f6`  
		Last Modified: Wed, 11 Jun 2025 13:13:39 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:71710191403da99f9ee23a5f4ce586615d5343cb8dc2fedc8ee6b02661d5e5f0
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
$ docker pull composer@sha256:4c53f0c3983068037d0ae5025f624a34e0161d07421903c621755cd7b79219f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76564511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a86750c1f342d7d0c03f934e0fab17d24792466052aa9d81071faeb6415eca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41ed00f4f69f9b33b5e886fedfa6143b6e95cd34c48de5a67dfca449d27075`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 3.5 MB (3468342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3dd3a928e1a1d32cf4174792bbec9d7d27add5d439d1765653b7fc22f66b92`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0721ec88e7a2844011b208a2272d18e4e309abd51c06c8e85a7fd685455524c`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f084ac2a53f05708a861a663438bea25fa87e41a10129b5c0a01e67aed1432c`  
		Last Modified: Wed, 11 Jun 2025 01:13:20 GMT  
		Size: 13.6 MB (13640521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87939f6f4e61218155cd7a88d809fc899e6d6a2b413033839baacad75def377a`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07468323dd1f0b8efa9f6be2eaf69811d60fee46c187e62fc1b05bd2bd100fa`  
		Last Modified: Wed, 11 Jun 2025 01:13:18 GMT  
		Size: 21.0 MB (20969804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d64e952347861cf8f1c360fcf1984249571751d095594a156d453d4cb4ec8b`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f854fc0d234074345274bcbda7bb11f7295b4bae6d7d400dcbe3bd892683a59`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860cdf46be6d7d1d3f8d39843f7297bfcad7f2061c5091785431569d5aef15a6`  
		Last Modified: Wed, 11 Jun 2025 01:14:30 GMT  
		Size: 33.9 MB (33928419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2417eb329e1350384f208e99d8a7b62dc527e52472c11398e054a99584d2cb0c`  
		Last Modified: Wed, 11 Jun 2025 01:14:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f74ea2dbf3bc0f243011cf49eded65284a6d0b6c30abc6b8933dd97beb5e96`  
		Last Modified: Wed, 11 Jun 2025 01:14:29 GMT  
		Size: 735.5 KB (735536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5097fdee9087545b7f49d7cfeb9e072b5f9938f2845d37c7eca15f7d41fc3c`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641cbabe81032e6beede3a4dc850d1fc1e44443f97c49a628393301c1f428062`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:f478ad00541c4e680716dd5adeff2e68ec2cc4d035d36e579f1125ea87ff37e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c78e654255109a0413537e2b175f5589c413d4c29bf54ea54b10c37362bed38`

```dockerfile
```

-	Layers:
	-	`sha256:fbd8ab339738c2150419d7f3e94805ec8ab44f5bac15d330cb352596388d9d01`  
		Last Modified: Wed, 11 Jun 2025 04:13:31 GMT  
		Size: 2.2 MB (2173838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31904e69e1fd6f3ec041500925a0ba8027ae489d72b979c14fc0abfb2463657a`  
		Last Modified: Wed, 11 Jun 2025 04:13:32 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:20279bcf5818513330f8831adbdb201fd22560a21fcb21e68a26b112daa6d255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74233398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2fc11a754f1feb9ae36681f641c64515252e49e5ca543c2cf1035ffb26bd77`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d738e6a7e1662efb7b90b7f0a4b2cce2f9247f395ab8c1924148a0d2dde272c3`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 13.6 MB (13640499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeec31f51dc18a99c6251ab6abd48a6b17b9bd04c498ca1ce606fbe0119a506`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a9bea01d63368fc6a169811ad55c9f7baf8d06c4a3c909bea5606bf5d161c`  
		Last Modified: Tue, 10 Jun 2025 23:54:15 GMT  
		Size: 19.1 MB (19091501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab1a6cbed4c7bce681ea2c1ba6335b04364d328abb8504ac38b7cb01546c1e`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7ac6548196a7241e2ff5aeb2ebaa92bd912151a57decbc09707501826e55d`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 20.0 KB (19986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a52088bfe28e3394348499664afc0150422c289f500eeb5736a846fb654a75`  
		Last Modified: Wed, 11 Jun 2025 01:34:01 GMT  
		Size: 33.8 MB (33807058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfadb48984526f1d970423f530584b05a533cf586b26af60f4077fe0d75af65`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf9ff0c926fffcd87f7c6e5cfb7a725d493067ba9283b2c1efddcbb53a1402`  
		Last Modified: Wed, 11 Jun 2025 01:34:42 GMT  
		Size: 736.1 KB (736126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51378ea70fd28d9aac94ff703323e73b3fbd24fbe401f0d32312160954168a2b`  
		Last Modified: Fri, 06 Jun 2025 18:42:25 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d765cf697fdc1cd49a825bc745561e714e462f63b61d2d3bb2b2db4aa91a55`  
		Last Modified: Wed, 11 Jun 2025 01:34:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:b65b6f7284622c7326cf3c0db5c7a85c18b9f169d085590651d752e28a3f8dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7667b1ab7acf4853718556822f307bcea5fed1ee9dc872234b106e10d4bf1c6`

```dockerfile
```

-	Layers:
	-	`sha256:f58d6aee9b7d0600d675290fe75755c44222821eafa2959a5153b91a7a412d52`  
		Last Modified: Wed, 11 Jun 2025 04:13:36 GMT  
		Size: 30.3 KB (30296 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:7899db68c464d1ef59c2906c8b15f7ead98141e355c2f9f2ead0104cadb406c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70995356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171861bcb6abf6fd32629fc7e96e657d07e27461a4cc7b1ff62a441190300847`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc30cbedbf54d9515871da07398fab0a70176613fac2230d3b598dd61f7dea64`  
		Last Modified: Wed, 11 Jun 2025 11:39:15 GMT  
		Size: 13.6 MB (13640514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ce30718845b98da85d3f2d4b2a979b2c4c9a318019ee4c5a3897dbb7a35b7`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788f675ffad6ad044155d5d8863ebb06f9142fe48298e02c274f65b961260418`  
		Last Modified: Wed, 11 Jun 2025 11:39:16 GMT  
		Size: 18.1 MB (18066806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2746b1c3debbab52b7827813726cffe0c2a6316b37ceefd0c7c7085cb9219577`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60271e3bc7668883349e90adf3ad21e0a859246f2f3d1430bd66ba8532b8cc1`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 20.0 KB (19984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bab94d85f8d4b9a1b97076f46ba751dc69827e8eaeb013290df1d46760098`  
		Last Modified: Wed, 11 Jun 2025 19:24:25 GMT  
		Size: 32.1 MB (32069944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d696523fff13201849f3282a4e284e28727f89ba185ff8bdb03a58fc314ccb55`  
		Last Modified: Wed, 11 Jun 2025 18:47:28 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35831c7ef69580355c4bb571b10c0df79cced513d276a1447723ffb9504869c8`  
		Last Modified: Wed, 11 Jun 2025 18:21:10 GMT  
		Size: 726.6 KB (726612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48006c8e93aaa7de2d158ea6c63a66aaa8fb263c40af5569c0fb94f036ae158d`  
		Last Modified: Wed, 11 Jun 2025 18:21:10 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7032c03fb42068e4949481bbd4be3be1f665e7a82c3a933a2a05576ddb8542df`  
		Last Modified: Wed, 11 Jun 2025 18:21:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:e4911230caf8b6f49835f9ce0d5aab76795b9641674f35d57346f40c54c0d808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c147bad3161baf64fa74a22365f15e8966fa9a74044b7dbef71a98f4f2cd1d`

```dockerfile
```

-	Layers:
	-	`sha256:4e3a0048403d9f55c2827fe342a857dce79b273373bbce34ce9f5966c342ddb1`  
		Last Modified: Wed, 11 Jun 2025 19:13:28 GMT  
		Size: 2.2 MB (2174154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a4c52a5df2729767b1dc823b38cce3fe92c907a2dd74cd9d5f8dc1225f7666c`  
		Last Modified: Wed, 11 Jun 2025 19:13:29 GMT  
		Size: 30.5 KB (30511 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:9ed447b7de769153bff4e0bc259dcdcfa950d8bcc26159660fbb55f7c01630d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76537210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f7de927ebb4f8985451bf78352f7e70ca2e3c379f8ab55bc851bcd276fc939`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e263556d24cfaaa81ec9153b95e1b25d54abdb35b46c3c74fa988a9f252f3`  
		Last Modified: Wed, 11 Jun 2025 09:16:54 GMT  
		Size: 3.5 MB (3470681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5bea448bb73ac691df99daf5772e7cb7307f122b4e0544c289a55be9ee24`  
		Last Modified: Wed, 11 Jun 2025 09:17:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a64acbbc8d220ea4c16baed763b26899f58299a8b85d3b8513f03b3023893`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123dcf4adf55a39c8cf4f202302f0a9dfd6d576c94bf8db94686e5a5ee1f4cf4`  
		Last Modified: Wed, 11 Jun 2025 09:33:08 GMT  
		Size: 13.6 MB (13640507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff08fc5740a571af506cddc0c38e20506f6151e574d4a10d77b748c7c3bd4b`  
		Last Modified: Wed, 11 Jun 2025 09:08:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc080435edc41cfa70a84f9586ffca3f880a9b4cedccc53c481889b18e1e1c2`  
		Last Modified: Wed, 11 Jun 2025 09:33:10 GMT  
		Size: 20.5 MB (20518887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3995038baa7f047e93509966aa2798fbc7bddf48517c43343b9add69edd5df`  
		Last Modified: Wed, 11 Jun 2025 09:08:59 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae69002966a0d0881786cca5d1dfa7b1fb54c0e7b1e4b6bf9c41f92f6208ec`  
		Last Modified: Wed, 11 Jun 2025 09:17:23 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5db0ec87df386dd8e7ed3e3a943ff4f92de4b419fe7f9bb1b4051dd24a6721`  
		Last Modified: Wed, 11 Jun 2025 15:13:38 GMT  
		Size: 34.0 MB (34010836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae1182fb6a9705ef49f6995317dfcfc6ef3d4b2292bc160d0ba7f8c246dda2e`  
		Last Modified: Wed, 11 Jun 2025 15:13:33 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d035e6ddd2f2b3ec3b75c60a418c5edd649b9e313a6bb9e5e7773ba65e752fb`  
		Last Modified: Wed, 11 Jun 2025 15:14:15 GMT  
		Size: 735.5 KB (735525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c87c5ee74b70a3f06c4198ca30f242c8f86f4da742fa485fc832839f15d66ed`  
		Last Modified: Wed, 11 Jun 2025 15:14:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70801ea2d0c992556c4485255efc32138f222c98823d965aaa17a8310c061f7c`  
		Last Modified: Wed, 11 Jun 2025 15:14:14 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:6d3c24b55e1a06c20901c37c28b0608aa905a2e24610daeeb7c9d04e9deb04ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ceb0ce8799fa17d423d608b8fd00d8d068a3716660186f4afaaa84a81386fb`

```dockerfile
```

-	Layers:
	-	`sha256:70a2c138ed0dcae3ceb6cb26356205083bc719e4ee6f4808e2c5977387e0e60f`  
		Last Modified: Wed, 11 Jun 2025 16:14:29 GMT  
		Size: 2.2 MB (2173978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4e4d7f1ec86be9db7404583ea0e16101f3e3a930504b89a937c451afa277ab`  
		Last Modified: Wed, 11 Jun 2025 16:14:30 GMT  
		Size: 30.5 KB (30539 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:c931c43b30b90ffa516a08c25e05ef4da2830208b91b340f6db6b671ad194a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77486369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4685a639678296eb95b2c1f87add779cb15ae1b1b99a242c2f35c073c3a63ea2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298f020aec5b2eb58f3f5d72ed081bd6c76a95799b7e438e4f3384447e42693d`  
		Last Modified: Wed, 11 Jun 2025 01:13:13 GMT  
		Size: 3.5 MB (3527774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ebeb8397f1f59382fb3bd2f49e7ae5aa3c63f7a6f5adde3d5af0fe196ad48`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c3fa431069cd36b1283a6dd73ec3c559701f45df22999775e61dd0dd4d578`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7db0fb8a413bd77d83d365246beba56a6d3ab745a296bb3119dd1c4844e7e2`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 13.6 MB (13640494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c81720a5bbf56ccfa06979187dbca8afa1859fb3d323625fe188373b9a06ed`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8fb25f24bc12988d302f27fbc0c27090c75c814e4f8dcb4396e125eafae7cb`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 21.5 MB (21493036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b67d63641d3800bf94c0e5eb453a80e9e00ec38acbc41e8b2dbe883e470dd6d`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821e028fb8ab3dacea139b63763d5d53b2d0981367d47fcd3f94182a0a2ac456`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 20.2 KB (20182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5a5771e66b8b5e97c3a2a977ca7089edbbca018038d8b56551bbbc0a8d6d01`  
		Last Modified: Wed, 11 Jun 2025 01:14:24 GMT  
		Size: 34.4 MB (34436667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d09bf8efac1bb2cb2458be039d96f810d55feb69816e0ae630509068dac26`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063d9bef4e56fa69cf33904760f4b8a2f1d7ce9202307e5ab7ceebf791d361f8`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 747.3 KB (747342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5097fdee9087545b7f49d7cfeb9e072b5f9938f2845d37c7eca15f7d41fc3c`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387efffd50fee23b95960319fa3959d346523333031fe1d80e9259d8eaa96a01`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:7bfabce3d40ae9cd2ffe1c3af8a88e3982a81a513f446328bd8e147aa8820688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99944fb53daf14ff0eee173447232e4dba802c0c847264e95f3572a37b733a06`

```dockerfile
```

-	Layers:
	-	`sha256:bdcfb0ffcb7c6b897ce1b98f040a3a0448451a4ef0f435242338c7d26870cc50`  
		Last Modified: Wed, 11 Jun 2025 04:13:49 GMT  
		Size: 2.2 MB (2173626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3c212fd7248554662d6a514fe1bcb0ad2719dd3cf20d75e5f74404172681c28`  
		Last Modified: Wed, 11 Jun 2025 04:13:50 GMT  
		Size: 30.4 KB (30386 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:13ea0fc5522c5ed3ab51d3d2cfed1000e4408455702be521a0c258f2851d07f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78910180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5470486ae40a27b00e10ebf16e30162c97cb75bb126a462d352afd2e799a1c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeaaf729ae44f9ac3f9b3f4551595556a417993152b53954f6f6a89f90a4954`  
		Last Modified: Wed, 11 Jun 2025 09:12:57 GMT  
		Size: 13.6 MB (13640505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928f2bed6e9375b5161e1fcbc32d598a194fc67da4a537c5d6a3aaab21aa3d0`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f75742ee54512415191653f6d3e2b7b2a4ff66bc4dcc60a24c12d00a0db76`  
		Last Modified: Wed, 11 Jun 2025 09:12:58 GMT  
		Size: 21.9 MB (21874047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189ddb23dd34f7e52d4b584e89ed11029f27d1dee76f138e62d772e61c75c0b6`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c88f7798e99a903cbf372177b9f7b8f2c70690f8dac0d589ec956038b045f`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a315ceb76a2ac2dda2c8bd167ee4d021a2f0885e86b42406a0c9eb02fb75b9e`  
		Last Modified: Wed, 11 Jun 2025 19:17:11 GMT  
		Size: 35.3 MB (35278992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197c9bbd782fcb082df2515b2222b6e5b48b183fca060886fc83d969d7daf6a`  
		Last Modified: Wed, 11 Jun 2025 19:17:08 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab01f9e69af64380336278b102d19cb9b79bb1e44ec420dbf8dc35ba490efd7a`  
		Last Modified: Wed, 11 Jun 2025 19:17:49 GMT  
		Size: 742.5 KB (742453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955d854b102f56238a18f4a89a2c22c5b722fc4858215da1cb3f658c158e82ac`  
		Last Modified: Wed, 11 Jun 2025 19:17:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe112e2374db26b2488d2a392933f334abe3f348f2f6d812a8c44bd78aa3e9d`  
		Last Modified: Wed, 11 Jun 2025 19:17:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:16e916224447f736b57c62b6cdf6bfdb544805d8289c2e13ebc4a658f0cc2990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c675920a44dfa4f1ff54eb4d3dfceca1a03a12563a2892854b28f2e417dab3`

```dockerfile
```

-	Layers:
	-	`sha256:c1a677b4e0534afc87f8bd8b2a044a4833daf0816eed4a5d159d437b690d4c8a`  
		Last Modified: Wed, 11 Jun 2025 22:13:35 GMT  
		Size: 2.2 MB (2172395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41d3b25ebe3fd471a8f0bb887db2c1d4dc3c097a3f097794ec59faba6a8ef463`  
		Last Modified: Wed, 11 Jun 2025 22:13:36 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:5621e50b235a59b8c69976cb12497086899daf383a9f2387fcac2f460308a6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73012087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a013faef78749ce18cec25c1e2a66f2c0df7a86cdc76c2ecf1eb1668d4bfcf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba389b9b1d6d27f7a263c92d52685675ded66f85f52a097bec1b658400eebc5`  
		Last Modified: Wed, 11 Jun 2025 02:39:58 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb4f8cea261544e7d849e5aa9581396ef8d4bd1b7c14ceb536acc047c9ff257`  
		Last Modified: Wed, 11 Jun 2025 02:40:00 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d9086703155ae9ef802a8a0d3e98de9aabdf18c7eb07d7758e92bef886259`  
		Last Modified: Wed, 11 Jun 2025 14:10:42 GMT  
		Size: 31.1 MB (31107690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b0b41c4564a3bd6fb68327d016b7b9e8acab85e9d3bf36c289ab0ca8ce1509`  
		Last Modified: Wed, 11 Jun 2025 14:10:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e8e2aad51b270919d00a8fe3370667b4acf4d40bc259e8405e1e98caa6ec`  
		Last Modified: Wed, 11 Jun 2025 14:20:34 GMT  
		Size: 733.3 KB (733285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619ca568e26bd59a624f3efad0fb970dc1c1cd1c759e29ea0f76f5e41d0f1d0f`  
		Last Modified: Wed, 11 Jun 2025 14:20:34 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b551e410dbc4ba1533ca034710366ff88c5f38eb054838d5acbb233aa0c59360`  
		Last Modified: Wed, 11 Jun 2025 14:20:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:2765c553acb5e422fc9bd56345ed25d5d0c827fefa1342505926c555fb9e4bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee68a0f763af2ce7d70f1f0f8e9dcdabaf134609d7908d1be471c866910af6fb`

```dockerfile
```

-	Layers:
	-	`sha256:249e2c285a2c9be43c98dea78f964f76f84afafffc235a47b059fdaebee0c8a0`  
		Last Modified: Wed, 11 Jun 2025 16:14:39 GMT  
		Size: 2.2 MB (2170662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e733ed7787fb847005cc32eea74c9e170cf49a1ee1436b4166d587627cff1381`  
		Last Modified: Wed, 11 Jun 2025 16:14:40 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:e3c80ca5a4116ac2671ef315c8b0f82b809a2fa6d145fb47ba594b1f4052e6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75036696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f03ddf3fd969299650f1d100ba587fa0d82061b05ab2734774e7384ef049be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035d42a37d5be6b1617300170ead6ce8970a5e2e4154fe287efc8af1e2f7441`  
		Last Modified: Wed, 11 Jun 2025 08:13:18 GMT  
		Size: 13.6 MB (13640519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca62563344c489947dce07a51fbce42cb5c2f338f525f3dc64a869bb23eea05`  
		Last Modified: Wed, 11 Jun 2025 06:17:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12b2d32a5b3932415a1a3b75f1dce848914c79f4be0b381c79061048ef8945`  
		Last Modified: Wed, 11 Jun 2025 10:56:19 GMT  
		Size: 21.4 MB (21446797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13957f45dfaafb933ab00f3283ea48d057cd2179a84687ebe45ad163f535de`  
		Last Modified: Wed, 11 Jun 2025 06:17:35 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48dd1edbbaf646c03ef3f286cc921fbc422e665578b988b9d03d890364f0d5`  
		Last Modified: Wed, 11 Jun 2025 07:14:21 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7301cbc0841ac3202a1b74a41aa6043f1d38879737a0da5c17da8e63aa32c2`  
		Last Modified: Wed, 11 Jun 2025 11:04:18 GMT  
		Size: 31.8 MB (31839063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae5612a3f46089fbce6bbf1de47ad49c5c4c6be46ad9e038f366a967187ab7`  
		Last Modified: Wed, 11 Jun 2025 11:04:10 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e197005d164da5b36acfa623b1a069914b6bacc27101eb05c08f8f5fd5a4c39b`  
		Last Modified: Wed, 11 Jun 2025 15:34:16 GMT  
		Size: 739.0 KB (738955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680555285dbd83e3be42aeb005ae570f5ff1b5eaba5768a244d0bade965d8a02`  
		Last Modified: Wed, 11 Jun 2025 15:34:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4c35a9662ffb17a097e48f01c2d0845aaf10492f17ecd5817ec9ff656bcb05`  
		Last Modified: Wed, 11 Jun 2025 15:34:16 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:050a6da2bec725aa6dc3a351946d020713c887b51087bee6d6c4501189633bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e563acc207b8e53760cf9517b2184d6041b6da8b3275bc23f254220bb442f9de`

```dockerfile
```

-	Layers:
	-	`sha256:e102856ffe80ca255ecd65446faf4798b6fad772c5ea22d21f9655b26f510cfb`  
		Last Modified: Wed, 11 Jun 2025 13:13:39 GMT  
		Size: 2.2 MB (2170450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed36825c442dab5cf11d326c01ec64c30cf744a8c5edfa107e9dc397ba146f6`  
		Last Modified: Wed, 11 Jun 2025 13:13:39 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:71710191403da99f9ee23a5f4ce586615d5343cb8dc2fedc8ee6b02661d5e5f0
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
$ docker pull composer@sha256:4c53f0c3983068037d0ae5025f624a34e0161d07421903c621755cd7b79219f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76564511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a86750c1f342d7d0c03f934e0fab17d24792466052aa9d81071faeb6415eca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41ed00f4f69f9b33b5e886fedfa6143b6e95cd34c48de5a67dfca449d27075`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 3.5 MB (3468342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3dd3a928e1a1d32cf4174792bbec9d7d27add5d439d1765653b7fc22f66b92`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0721ec88e7a2844011b208a2272d18e4e309abd51c06c8e85a7fd685455524c`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f084ac2a53f05708a861a663438bea25fa87e41a10129b5c0a01e67aed1432c`  
		Last Modified: Wed, 11 Jun 2025 01:13:20 GMT  
		Size: 13.6 MB (13640521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87939f6f4e61218155cd7a88d809fc899e6d6a2b413033839baacad75def377a`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07468323dd1f0b8efa9f6be2eaf69811d60fee46c187e62fc1b05bd2bd100fa`  
		Last Modified: Wed, 11 Jun 2025 01:13:18 GMT  
		Size: 21.0 MB (20969804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d64e952347861cf8f1c360fcf1984249571751d095594a156d453d4cb4ec8b`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f854fc0d234074345274bcbda7bb11f7295b4bae6d7d400dcbe3bd892683a59`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860cdf46be6d7d1d3f8d39843f7297bfcad7f2061c5091785431569d5aef15a6`  
		Last Modified: Wed, 11 Jun 2025 01:14:30 GMT  
		Size: 33.9 MB (33928419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2417eb329e1350384f208e99d8a7b62dc527e52472c11398e054a99584d2cb0c`  
		Last Modified: Wed, 11 Jun 2025 01:14:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f74ea2dbf3bc0f243011cf49eded65284a6d0b6c30abc6b8933dd97beb5e96`  
		Last Modified: Wed, 11 Jun 2025 01:14:29 GMT  
		Size: 735.5 KB (735536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5097fdee9087545b7f49d7cfeb9e072b5f9938f2845d37c7eca15f7d41fc3c`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641cbabe81032e6beede3a4dc850d1fc1e44443f97c49a628393301c1f428062`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:f478ad00541c4e680716dd5adeff2e68ec2cc4d035d36e579f1125ea87ff37e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c78e654255109a0413537e2b175f5589c413d4c29bf54ea54b10c37362bed38`

```dockerfile
```

-	Layers:
	-	`sha256:fbd8ab339738c2150419d7f3e94805ec8ab44f5bac15d330cb352596388d9d01`  
		Last Modified: Wed, 11 Jun 2025 04:13:31 GMT  
		Size: 2.2 MB (2173838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31904e69e1fd6f3ec041500925a0ba8027ae489d72b979c14fc0abfb2463657a`  
		Last Modified: Wed, 11 Jun 2025 04:13:32 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v6

```console
$ docker pull composer@sha256:20279bcf5818513330f8831adbdb201fd22560a21fcb21e68a26b112daa6d255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74233398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2fc11a754f1feb9ae36681f641c64515252e49e5ca543c2cf1035ffb26bd77`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d738e6a7e1662efb7b90b7f0a4b2cce2f9247f395ab8c1924148a0d2dde272c3`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 13.6 MB (13640499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeec31f51dc18a99c6251ab6abd48a6b17b9bd04c498ca1ce606fbe0119a506`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a9bea01d63368fc6a169811ad55c9f7baf8d06c4a3c909bea5606bf5d161c`  
		Last Modified: Tue, 10 Jun 2025 23:54:15 GMT  
		Size: 19.1 MB (19091501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab1a6cbed4c7bce681ea2c1ba6335b04364d328abb8504ac38b7cb01546c1e`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7ac6548196a7241e2ff5aeb2ebaa92bd912151a57decbc09707501826e55d`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 20.0 KB (19986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a52088bfe28e3394348499664afc0150422c289f500eeb5736a846fb654a75`  
		Last Modified: Wed, 11 Jun 2025 01:34:01 GMT  
		Size: 33.8 MB (33807058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfadb48984526f1d970423f530584b05a533cf586b26af60f4077fe0d75af65`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf9ff0c926fffcd87f7c6e5cfb7a725d493067ba9283b2c1efddcbb53a1402`  
		Last Modified: Wed, 11 Jun 2025 01:34:42 GMT  
		Size: 736.1 KB (736126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51378ea70fd28d9aac94ff703323e73b3fbd24fbe401f0d32312160954168a2b`  
		Last Modified: Fri, 06 Jun 2025 18:42:25 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d765cf697fdc1cd49a825bc745561e714e462f63b61d2d3bb2b2db4aa91a55`  
		Last Modified: Wed, 11 Jun 2025 01:34:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:b65b6f7284622c7326cf3c0db5c7a85c18b9f169d085590651d752e28a3f8dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7667b1ab7acf4853718556822f307bcea5fed1ee9dc872234b106e10d4bf1c6`

```dockerfile
```

-	Layers:
	-	`sha256:f58d6aee9b7d0600d675290fe75755c44222821eafa2959a5153b91a7a412d52`  
		Last Modified: Wed, 11 Jun 2025 04:13:36 GMT  
		Size: 30.3 KB (30296 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v7

```console
$ docker pull composer@sha256:7899db68c464d1ef59c2906c8b15f7ead98141e355c2f9f2ead0104cadb406c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70995356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171861bcb6abf6fd32629fc7e96e657d07e27461a4cc7b1ff62a441190300847`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc30cbedbf54d9515871da07398fab0a70176613fac2230d3b598dd61f7dea64`  
		Last Modified: Wed, 11 Jun 2025 11:39:15 GMT  
		Size: 13.6 MB (13640514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ce30718845b98da85d3f2d4b2a979b2c4c9a318019ee4c5a3897dbb7a35b7`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788f675ffad6ad044155d5d8863ebb06f9142fe48298e02c274f65b961260418`  
		Last Modified: Wed, 11 Jun 2025 11:39:16 GMT  
		Size: 18.1 MB (18066806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2746b1c3debbab52b7827813726cffe0c2a6316b37ceefd0c7c7085cb9219577`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60271e3bc7668883349e90adf3ad21e0a859246f2f3d1430bd66ba8532b8cc1`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 20.0 KB (19984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bab94d85f8d4b9a1b97076f46ba751dc69827e8eaeb013290df1d46760098`  
		Last Modified: Wed, 11 Jun 2025 19:24:25 GMT  
		Size: 32.1 MB (32069944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d696523fff13201849f3282a4e284e28727f89ba185ff8bdb03a58fc314ccb55`  
		Last Modified: Wed, 11 Jun 2025 18:47:28 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35831c7ef69580355c4bb571b10c0df79cced513d276a1447723ffb9504869c8`  
		Last Modified: Wed, 11 Jun 2025 18:21:10 GMT  
		Size: 726.6 KB (726612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48006c8e93aaa7de2d158ea6c63a66aaa8fb263c40af5569c0fb94f036ae158d`  
		Last Modified: Wed, 11 Jun 2025 18:21:10 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7032c03fb42068e4949481bbd4be3be1f665e7a82c3a933a2a05576ddb8542df`  
		Last Modified: Wed, 11 Jun 2025 18:21:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:e4911230caf8b6f49835f9ce0d5aab76795b9641674f35d57346f40c54c0d808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c147bad3161baf64fa74a22365f15e8966fa9a74044b7dbef71a98f4f2cd1d`

```dockerfile
```

-	Layers:
	-	`sha256:4e3a0048403d9f55c2827fe342a857dce79b273373bbce34ce9f5966c342ddb1`  
		Last Modified: Wed, 11 Jun 2025 19:13:28 GMT  
		Size: 2.2 MB (2174154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a4c52a5df2729767b1dc823b38cce3fe92c907a2dd74cd9d5f8dc1225f7666c`  
		Last Modified: Wed, 11 Jun 2025 19:13:29 GMT  
		Size: 30.5 KB (30511 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:9ed447b7de769153bff4e0bc259dcdcfa950d8bcc26159660fbb55f7c01630d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76537210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f7de927ebb4f8985451bf78352f7e70ca2e3c379f8ab55bc851bcd276fc939`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e263556d24cfaaa81ec9153b95e1b25d54abdb35b46c3c74fa988a9f252f3`  
		Last Modified: Wed, 11 Jun 2025 09:16:54 GMT  
		Size: 3.5 MB (3470681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5bea448bb73ac691df99daf5772e7cb7307f122b4e0544c289a55be9ee24`  
		Last Modified: Wed, 11 Jun 2025 09:17:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a64acbbc8d220ea4c16baed763b26899f58299a8b85d3b8513f03b3023893`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123dcf4adf55a39c8cf4f202302f0a9dfd6d576c94bf8db94686e5a5ee1f4cf4`  
		Last Modified: Wed, 11 Jun 2025 09:33:08 GMT  
		Size: 13.6 MB (13640507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff08fc5740a571af506cddc0c38e20506f6151e574d4a10d77b748c7c3bd4b`  
		Last Modified: Wed, 11 Jun 2025 09:08:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc080435edc41cfa70a84f9586ffca3f880a9b4cedccc53c481889b18e1e1c2`  
		Last Modified: Wed, 11 Jun 2025 09:33:10 GMT  
		Size: 20.5 MB (20518887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3995038baa7f047e93509966aa2798fbc7bddf48517c43343b9add69edd5df`  
		Last Modified: Wed, 11 Jun 2025 09:08:59 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae69002966a0d0881786cca5d1dfa7b1fb54c0e7b1e4b6bf9c41f92f6208ec`  
		Last Modified: Wed, 11 Jun 2025 09:17:23 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5db0ec87df386dd8e7ed3e3a943ff4f92de4b419fe7f9bb1b4051dd24a6721`  
		Last Modified: Wed, 11 Jun 2025 15:13:38 GMT  
		Size: 34.0 MB (34010836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae1182fb6a9705ef49f6995317dfcfc6ef3d4b2292bc160d0ba7f8c246dda2e`  
		Last Modified: Wed, 11 Jun 2025 15:13:33 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d035e6ddd2f2b3ec3b75c60a418c5edd649b9e313a6bb9e5e7773ba65e752fb`  
		Last Modified: Wed, 11 Jun 2025 15:14:15 GMT  
		Size: 735.5 KB (735525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c87c5ee74b70a3f06c4198ca30f242c8f86f4da742fa485fc832839f15d66ed`  
		Last Modified: Wed, 11 Jun 2025 15:14:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70801ea2d0c992556c4485255efc32138f222c98823d965aaa17a8310c061f7c`  
		Last Modified: Wed, 11 Jun 2025 15:14:14 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:6d3c24b55e1a06c20901c37c28b0608aa905a2e24610daeeb7c9d04e9deb04ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ceb0ce8799fa17d423d608b8fd00d8d068a3716660186f4afaaa84a81386fb`

```dockerfile
```

-	Layers:
	-	`sha256:70a2c138ed0dcae3ceb6cb26356205083bc719e4ee6f4808e2c5977387e0e60f`  
		Last Modified: Wed, 11 Jun 2025 16:14:29 GMT  
		Size: 2.2 MB (2173978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4e4d7f1ec86be9db7404583ea0e16101f3e3a930504b89a937c451afa277ab`  
		Last Modified: Wed, 11 Jun 2025 16:14:30 GMT  
		Size: 30.5 KB (30539 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; 386

```console
$ docker pull composer@sha256:c931c43b30b90ffa516a08c25e05ef4da2830208b91b340f6db6b671ad194a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77486369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4685a639678296eb95b2c1f87add779cb15ae1b1b99a242c2f35c073c3a63ea2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298f020aec5b2eb58f3f5d72ed081bd6c76a95799b7e438e4f3384447e42693d`  
		Last Modified: Wed, 11 Jun 2025 01:13:13 GMT  
		Size: 3.5 MB (3527774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ebeb8397f1f59382fb3bd2f49e7ae5aa3c63f7a6f5adde3d5af0fe196ad48`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c3fa431069cd36b1283a6dd73ec3c559701f45df22999775e61dd0dd4d578`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7db0fb8a413bd77d83d365246beba56a6d3ab745a296bb3119dd1c4844e7e2`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 13.6 MB (13640494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c81720a5bbf56ccfa06979187dbca8afa1859fb3d323625fe188373b9a06ed`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8fb25f24bc12988d302f27fbc0c27090c75c814e4f8dcb4396e125eafae7cb`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 21.5 MB (21493036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b67d63641d3800bf94c0e5eb453a80e9e00ec38acbc41e8b2dbe883e470dd6d`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821e028fb8ab3dacea139b63763d5d53b2d0981367d47fcd3f94182a0a2ac456`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 20.2 KB (20182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5a5771e66b8b5e97c3a2a977ca7089edbbca018038d8b56551bbbc0a8d6d01`  
		Last Modified: Wed, 11 Jun 2025 01:14:24 GMT  
		Size: 34.4 MB (34436667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d09bf8efac1bb2cb2458be039d96f810d55feb69816e0ae630509068dac26`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063d9bef4e56fa69cf33904760f4b8a2f1d7ce9202307e5ab7ceebf791d361f8`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 747.3 KB (747342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5097fdee9087545b7f49d7cfeb9e072b5f9938f2845d37c7eca15f7d41fc3c`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387efffd50fee23b95960319fa3959d346523333031fe1d80e9259d8eaa96a01`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:7bfabce3d40ae9cd2ffe1c3af8a88e3982a81a513f446328bd8e147aa8820688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99944fb53daf14ff0eee173447232e4dba802c0c847264e95f3572a37b733a06`

```dockerfile
```

-	Layers:
	-	`sha256:bdcfb0ffcb7c6b897ce1b98f040a3a0448451a4ef0f435242338c7d26870cc50`  
		Last Modified: Wed, 11 Jun 2025 04:13:49 GMT  
		Size: 2.2 MB (2173626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3c212fd7248554662d6a514fe1bcb0ad2719dd3cf20d75e5f74404172681c28`  
		Last Modified: Wed, 11 Jun 2025 04:13:50 GMT  
		Size: 30.4 KB (30386 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; ppc64le

```console
$ docker pull composer@sha256:13ea0fc5522c5ed3ab51d3d2cfed1000e4408455702be521a0c258f2851d07f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78910180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5470486ae40a27b00e10ebf16e30162c97cb75bb126a462d352afd2e799a1c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeaaf729ae44f9ac3f9b3f4551595556a417993152b53954f6f6a89f90a4954`  
		Last Modified: Wed, 11 Jun 2025 09:12:57 GMT  
		Size: 13.6 MB (13640505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928f2bed6e9375b5161e1fcbc32d598a194fc67da4a537c5d6a3aaab21aa3d0`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f75742ee54512415191653f6d3e2b7b2a4ff66bc4dcc60a24c12d00a0db76`  
		Last Modified: Wed, 11 Jun 2025 09:12:58 GMT  
		Size: 21.9 MB (21874047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189ddb23dd34f7e52d4b584e89ed11029f27d1dee76f138e62d772e61c75c0b6`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c88f7798e99a903cbf372177b9f7b8f2c70690f8dac0d589ec956038b045f`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a315ceb76a2ac2dda2c8bd167ee4d021a2f0885e86b42406a0c9eb02fb75b9e`  
		Last Modified: Wed, 11 Jun 2025 19:17:11 GMT  
		Size: 35.3 MB (35278992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197c9bbd782fcb082df2515b2222b6e5b48b183fca060886fc83d969d7daf6a`  
		Last Modified: Wed, 11 Jun 2025 19:17:08 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab01f9e69af64380336278b102d19cb9b79bb1e44ec420dbf8dc35ba490efd7a`  
		Last Modified: Wed, 11 Jun 2025 19:17:49 GMT  
		Size: 742.5 KB (742453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955d854b102f56238a18f4a89a2c22c5b722fc4858215da1cb3f658c158e82ac`  
		Last Modified: Wed, 11 Jun 2025 19:17:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe112e2374db26b2488d2a392933f334abe3f348f2f6d812a8c44bd78aa3e9d`  
		Last Modified: Wed, 11 Jun 2025 19:17:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:16e916224447f736b57c62b6cdf6bfdb544805d8289c2e13ebc4a658f0cc2990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c675920a44dfa4f1ff54eb4d3dfceca1a03a12563a2892854b28f2e417dab3`

```dockerfile
```

-	Layers:
	-	`sha256:c1a677b4e0534afc87f8bd8b2a044a4833daf0816eed4a5d159d437b690d4c8a`  
		Last Modified: Wed, 11 Jun 2025 22:13:35 GMT  
		Size: 2.2 MB (2172395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41d3b25ebe3fd471a8f0bb887db2c1d4dc3c097a3f097794ec59faba6a8ef463`  
		Last Modified: Wed, 11 Jun 2025 22:13:36 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; riscv64

```console
$ docker pull composer@sha256:5621e50b235a59b8c69976cb12497086899daf383a9f2387fcac2f460308a6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73012087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a013faef78749ce18cec25c1e2a66f2c0df7a86cdc76c2ecf1eb1668d4bfcf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba389b9b1d6d27f7a263c92d52685675ded66f85f52a097bec1b658400eebc5`  
		Last Modified: Wed, 11 Jun 2025 02:39:58 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb4f8cea261544e7d849e5aa9581396ef8d4bd1b7c14ceb536acc047c9ff257`  
		Last Modified: Wed, 11 Jun 2025 02:40:00 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d9086703155ae9ef802a8a0d3e98de9aabdf18c7eb07d7758e92bef886259`  
		Last Modified: Wed, 11 Jun 2025 14:10:42 GMT  
		Size: 31.1 MB (31107690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b0b41c4564a3bd6fb68327d016b7b9e8acab85e9d3bf36c289ab0ca8ce1509`  
		Last Modified: Wed, 11 Jun 2025 14:10:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e8e2aad51b270919d00a8fe3370667b4acf4d40bc259e8405e1e98caa6ec`  
		Last Modified: Wed, 11 Jun 2025 14:20:34 GMT  
		Size: 733.3 KB (733285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619ca568e26bd59a624f3efad0fb970dc1c1cd1c759e29ea0f76f5e41d0f1d0f`  
		Last Modified: Wed, 11 Jun 2025 14:20:34 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b551e410dbc4ba1533ca034710366ff88c5f38eb054838d5acbb233aa0c59360`  
		Last Modified: Wed, 11 Jun 2025 14:20:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:2765c553acb5e422fc9bd56345ed25d5d0c827fefa1342505926c555fb9e4bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee68a0f763af2ce7d70f1f0f8e9dcdabaf134609d7908d1be471c866910af6fb`

```dockerfile
```

-	Layers:
	-	`sha256:249e2c285a2c9be43c98dea78f964f76f84afafffc235a47b059fdaebee0c8a0`  
		Last Modified: Wed, 11 Jun 2025 16:14:39 GMT  
		Size: 2.2 MB (2170662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e733ed7787fb847005cc32eea74c9e170cf49a1ee1436b4166d587627cff1381`  
		Last Modified: Wed, 11 Jun 2025 16:14:40 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; s390x

```console
$ docker pull composer@sha256:e3c80ca5a4116ac2671ef315c8b0f82b809a2fa6d145fb47ba594b1f4052e6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75036696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f03ddf3fd969299650f1d100ba587fa0d82061b05ab2734774e7384ef049be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035d42a37d5be6b1617300170ead6ce8970a5e2e4154fe287efc8af1e2f7441`  
		Last Modified: Wed, 11 Jun 2025 08:13:18 GMT  
		Size: 13.6 MB (13640519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca62563344c489947dce07a51fbce42cb5c2f338f525f3dc64a869bb23eea05`  
		Last Modified: Wed, 11 Jun 2025 06:17:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12b2d32a5b3932415a1a3b75f1dce848914c79f4be0b381c79061048ef8945`  
		Last Modified: Wed, 11 Jun 2025 10:56:19 GMT  
		Size: 21.4 MB (21446797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13957f45dfaafb933ab00f3283ea48d057cd2179a84687ebe45ad163f535de`  
		Last Modified: Wed, 11 Jun 2025 06:17:35 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48dd1edbbaf646c03ef3f286cc921fbc422e665578b988b9d03d890364f0d5`  
		Last Modified: Wed, 11 Jun 2025 07:14:21 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7301cbc0841ac3202a1b74a41aa6043f1d38879737a0da5c17da8e63aa32c2`  
		Last Modified: Wed, 11 Jun 2025 11:04:18 GMT  
		Size: 31.8 MB (31839063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae5612a3f46089fbce6bbf1de47ad49c5c4c6be46ad9e038f366a967187ab7`  
		Last Modified: Wed, 11 Jun 2025 11:04:10 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e197005d164da5b36acfa623b1a069914b6bacc27101eb05c08f8f5fd5a4c39b`  
		Last Modified: Wed, 11 Jun 2025 15:34:16 GMT  
		Size: 739.0 KB (738955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680555285dbd83e3be42aeb005ae570f5ff1b5eaba5768a244d0bade965d8a02`  
		Last Modified: Wed, 11 Jun 2025 15:34:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4c35a9662ffb17a097e48f01c2d0845aaf10492f17ecd5817ec9ff656bcb05`  
		Last Modified: Wed, 11 Jun 2025 15:34:16 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:050a6da2bec725aa6dc3a351946d020713c887b51087bee6d6c4501189633bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e563acc207b8e53760cf9517b2184d6041b6da8b3275bc23f254220bb442f9de`

```dockerfile
```

-	Layers:
	-	`sha256:e102856ffe80ca255ecd65446faf4798b6fad772c5ea22d21f9655b26f510cfb`  
		Last Modified: Wed, 11 Jun 2025 13:13:39 GMT  
		Size: 2.2 MB (2170450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed36825c442dab5cf11d326c01ec64c30cf744a8c5edfa107e9dc397ba146f6`  
		Last Modified: Wed, 11 Jun 2025 13:13:39 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:eec936bdc4364a9f3f5984ef8764f10f67a5c4ffb127ac7d151d651b3611b4a8
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
$ docker pull composer@sha256:018ee8a1b80d8a42a6db5059b17b32009f0520248d4ca4ac5cea362650b0e452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76805423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89499392c7c0f772f148806eeb7d8177e801124b561c04da6d3515c0dd28ac9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41ed00f4f69f9b33b5e886fedfa6143b6e95cd34c48de5a67dfca449d27075`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 3.5 MB (3468342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3dd3a928e1a1d32cf4174792bbec9d7d27add5d439d1765653b7fc22f66b92`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0721ec88e7a2844011b208a2272d18e4e309abd51c06c8e85a7fd685455524c`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f084ac2a53f05708a861a663438bea25fa87e41a10129b5c0a01e67aed1432c`  
		Last Modified: Wed, 11 Jun 2025 01:13:20 GMT  
		Size: 13.6 MB (13640521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87939f6f4e61218155cd7a88d809fc899e6d6a2b413033839baacad75def377a`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07468323dd1f0b8efa9f6be2eaf69811d60fee46c187e62fc1b05bd2bd100fa`  
		Last Modified: Wed, 11 Jun 2025 01:13:18 GMT  
		Size: 21.0 MB (20969804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d64e952347861cf8f1c360fcf1984249571751d095594a156d453d4cb4ec8b`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f854fc0d234074345274bcbda7bb11f7295b4bae6d7d400dcbe3bd892683a59`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7aa3b0bb08cff094c890c8f9bd94d1242d8e4eecc66695b56cf0b71486bfdd`  
		Last Modified: Wed, 11 Jun 2025 01:14:39 GMT  
		Size: 33.9 MB (33928445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4004cd9be3af376ad1def28d7db8a22858965bcd6aabcb6389c7b356e3975`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275f621c47ad6f7e352d718837b79434a5bf362a7338d9131c9708977015fad3`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 976.4 KB (976410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8d98e8d78d1f43122ec0387f46a806641cb2d802951aa0ffecee3114bacc7d`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac122cbf35bfacbe46e1db0cf0b0e168d63b2f524e502932abd69bae48da849`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:e3c78b7bbcaa7aea33836758c8b9297dc69e88ada9dcf94a219e83a015c48eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3f6a2abbcf87370cfc2126f9525aa69638db268a01997e2937720170aac18a`

```dockerfile
```

-	Layers:
	-	`sha256:a4349da333f6fb53bdfe252104e833e07a89b4bec877467a87db370af1fd23ad`  
		Last Modified: Wed, 11 Jun 2025 04:13:49 GMT  
		Size: 2.2 MB (2175332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0ff13651ccad2a566eb25c6f530e75b55bdc5271773b6597b1742a8794872b`  
		Last Modified: Wed, 11 Jun 2025 04:13:49 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:cabd4f8b3fa60afcf17a1d2f439a04f5b18930b89f774227d79c7ec0e5196bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74474043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e33ae9428155f4f4eed862cc84c35990e94b325d9eac5bd6852b530e3468672`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d738e6a7e1662efb7b90b7f0a4b2cce2f9247f395ab8c1924148a0d2dde272c3`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 13.6 MB (13640499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeec31f51dc18a99c6251ab6abd48a6b17b9bd04c498ca1ce606fbe0119a506`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a9bea01d63368fc6a169811ad55c9f7baf8d06c4a3c909bea5606bf5d161c`  
		Last Modified: Tue, 10 Jun 2025 23:54:15 GMT  
		Size: 19.1 MB (19091501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab1a6cbed4c7bce681ea2c1ba6335b04364d328abb8504ac38b7cb01546c1e`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7ac6548196a7241e2ff5aeb2ebaa92bd912151a57decbc09707501826e55d`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 20.0 KB (19986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a52088bfe28e3394348499664afc0150422c289f500eeb5736a846fb654a75`  
		Last Modified: Wed, 11 Jun 2025 01:34:01 GMT  
		Size: 33.8 MB (33807058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfadb48984526f1d970423f530584b05a533cf586b26af60f4077fe0d75af65`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6d0b23171c56910ae6db9d8b6fbf79c0503339a96ab31fc527f9a6092cfad8`  
		Last Modified: Wed, 11 Jun 2025 01:46:48 GMT  
		Size: 976.8 KB (976760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1af69bdf34fca59d7eb30b0f9edddd220ae82577ff30612722efcaccd1b88b0`  
		Last Modified: Fri, 06 Jun 2025 18:42:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0441808df82eb88aa8599d9a72092fed54d4074aa052e4fe1aa44d650d466752`  
		Last Modified: Wed, 11 Jun 2025 01:46:54 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:4ae2055f652cf96d80673ff0c82c642b9fe193093bbadeed702a46c8c7abc211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f498a213c449143c593b740936c06c1a30c28c0d681279674dfc37963deaf3bc`

```dockerfile
```

-	Layers:
	-	`sha256:edcb3fe774625cf135154b452fccdedc661e27ac48b3ef0c34f6210991443adf`  
		Last Modified: Wed, 11 Jun 2025 04:13:54 GMT  
		Size: 30.6 KB (30593 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:48e7ae6497265451eeebf1afb34eb14d45dc622a97cf0616cdbb4dfed65f4964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71235844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4d4c70ce2e197972a272c79e1de0a223700e919ac7e20e3e042ed6af9edeb1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc30cbedbf54d9515871da07398fab0a70176613fac2230d3b598dd61f7dea64`  
		Last Modified: Wed, 11 Jun 2025 11:39:15 GMT  
		Size: 13.6 MB (13640514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ce30718845b98da85d3f2d4b2a979b2c4c9a318019ee4c5a3897dbb7a35b7`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788f675ffad6ad044155d5d8863ebb06f9142fe48298e02c274f65b961260418`  
		Last Modified: Wed, 11 Jun 2025 11:39:16 GMT  
		Size: 18.1 MB (18066806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2746b1c3debbab52b7827813726cffe0c2a6316b37ceefd0c7c7085cb9219577`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60271e3bc7668883349e90adf3ad21e0a859246f2f3d1430bd66ba8532b8cc1`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 20.0 KB (19984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bab94d85f8d4b9a1b97076f46ba751dc69827e8eaeb013290df1d46760098`  
		Last Modified: Wed, 11 Jun 2025 19:24:25 GMT  
		Size: 32.1 MB (32069944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d696523fff13201849f3282a4e284e28727f89ba185ff8bdb03a58fc314ccb55`  
		Last Modified: Wed, 11 Jun 2025 18:47:28 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1819f872292f162c5379693691995426aacfa08ced25e4fd27a7ef43bb70147e`  
		Last Modified: Wed, 11 Jun 2025 18:21:50 GMT  
		Size: 967.1 KB (967091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c70e26991c83798cff0473fb35dff58387d2282ab12408ad15c3d469049331`  
		Last Modified: Wed, 11 Jun 2025 18:21:50 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9619b4783886f7500963c4f9dda9a0b1ef6d8d2901a870df7fcf054f2977af9`  
		Last Modified: Wed, 11 Jun 2025 18:21:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:94b06f9d43410646d3710eebd61f14bfaa661a19b74568998125cd7805f89ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd587ba7c7d03810b426db14935e43d11776b7b25b4fb5bc04ca10a7d2aa98`

```dockerfile
```

-	Layers:
	-	`sha256:6a6062bb951a633715a67b8f08256496b7c24f71c8f9a44aa4dd6a44816e62d7`  
		Last Modified: Wed, 11 Jun 2025 19:13:41 GMT  
		Size: 2.2 MB (2175656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895f61efaeb21f18b801c568f7d0cc74cc84baf4aaef9cd4658e9b7e1f6140d0`  
		Last Modified: Wed, 11 Jun 2025 19:13:42 GMT  
		Size: 30.8 KB (30809 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:e58df78ba28a1c71954c3845a0a87bd0d0e9cc88f3e14bd3c658d0b20f6a0ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76777731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f8d65691d8f2daf38f59650b5ace82ee4a24b8238dab957493be3c7f09608c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e263556d24cfaaa81ec9153b95e1b25d54abdb35b46c3c74fa988a9f252f3`  
		Last Modified: Wed, 11 Jun 2025 09:16:54 GMT  
		Size: 3.5 MB (3470681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5bea448bb73ac691df99daf5772e7cb7307f122b4e0544c289a55be9ee24`  
		Last Modified: Wed, 11 Jun 2025 09:17:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a64acbbc8d220ea4c16baed763b26899f58299a8b85d3b8513f03b3023893`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123dcf4adf55a39c8cf4f202302f0a9dfd6d576c94bf8db94686e5a5ee1f4cf4`  
		Last Modified: Wed, 11 Jun 2025 09:33:08 GMT  
		Size: 13.6 MB (13640507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff08fc5740a571af506cddc0c38e20506f6151e574d4a10d77b748c7c3bd4b`  
		Last Modified: Wed, 11 Jun 2025 09:08:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc080435edc41cfa70a84f9586ffca3f880a9b4cedccc53c481889b18e1e1c2`  
		Last Modified: Wed, 11 Jun 2025 09:33:10 GMT  
		Size: 20.5 MB (20518887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3995038baa7f047e93509966aa2798fbc7bddf48517c43343b9add69edd5df`  
		Last Modified: Wed, 11 Jun 2025 09:08:59 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae69002966a0d0881786cca5d1dfa7b1fb54c0e7b1e4b6bf9c41f92f6208ec`  
		Last Modified: Wed, 11 Jun 2025 09:17:23 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5db0ec87df386dd8e7ed3e3a943ff4f92de4b419fe7f9bb1b4051dd24a6721`  
		Last Modified: Wed, 11 Jun 2025 15:13:38 GMT  
		Size: 34.0 MB (34010836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae1182fb6a9705ef49f6995317dfcfc6ef3d4b2292bc160d0ba7f8c246dda2e`  
		Last Modified: Wed, 11 Jun 2025 15:13:33 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797f0b16aefb6bb6a7d6af6400cee5b8275b81be5a286e77b19b60bb7069ccb`  
		Last Modified: Wed, 11 Jun 2025 16:14:10 GMT  
		Size: 976.0 KB (976036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb78c70c901a5531ae4ae81501f0dbcae57add862161bc2d6d794228ec77479b`  
		Last Modified: Wed, 11 Jun 2025 15:15:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecc1e772b20c5a6d138ed8532d8899007acf289e3afcc409f9f2dd7b823a3a`  
		Last Modified: Wed, 11 Jun 2025 16:14:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:bf2265f44da3580d35ee4c2c278cefbf8b84fe72cb09fc00c35769f60d2befe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb3cfb1574adf3b66d7d63eaea712bfe54b3ed449c5a4f7d725c6aac9c62637`

```dockerfile
```

-	Layers:
	-	`sha256:c1c94bc49ec527aeadb9fd32cc4e4d6c71f92ccc6bf8378d9e5605b406dea882`  
		Last Modified: Wed, 11 Jun 2025 16:14:27 GMT  
		Size: 2.2 MB (2175484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:160a3cc68b0b43e857b6a305bb01a248206c40228e2706205e52cc4f13d27827`  
		Last Modified: Wed, 11 Jun 2025 16:14:28 GMT  
		Size: 30.8 KB (30841 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:750071636b642978927235b533d02d608b033945c5033962df7051345c6e71f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77728785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d8f82a6bc78d1d8cafba2f7b0419bf619047ac664f19abd2484cb15db3d62a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298f020aec5b2eb58f3f5d72ed081bd6c76a95799b7e438e4f3384447e42693d`  
		Last Modified: Wed, 11 Jun 2025 01:13:13 GMT  
		Size: 3.5 MB (3527774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ebeb8397f1f59382fb3bd2f49e7ae5aa3c63f7a6f5adde3d5af0fe196ad48`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c3fa431069cd36b1283a6dd73ec3c559701f45df22999775e61dd0dd4d578`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7db0fb8a413bd77d83d365246beba56a6d3ab745a296bb3119dd1c4844e7e2`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 13.6 MB (13640494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c81720a5bbf56ccfa06979187dbca8afa1859fb3d323625fe188373b9a06ed`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8fb25f24bc12988d302f27fbc0c27090c75c814e4f8dcb4396e125eafae7cb`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 21.5 MB (21493036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b67d63641d3800bf94c0e5eb453a80e9e00ec38acbc41e8b2dbe883e470dd6d`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821e028fb8ab3dacea139b63763d5d53b2d0981367d47fcd3f94182a0a2ac456`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 20.2 KB (20182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1119f1ba214f23f34c82cc094cd0e38eb36a07f01af7a3a2c1c889ee61a77db3`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 34.4 MB (34436698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e31d6c9586eea6c3de20adb86bf981bec9980b3172386076809f101620c92a`  
		Last Modified: Wed, 11 Jun 2025 01:14:21 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c939d938a848601c211ad3b2c18ae5a586f353150d3c2da6e15d0e16b07b3c32`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 989.7 KB (989719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3eff2062ef4c05ca74719dbdada1fc575f4ac3c462dc93f769ec0616dcd340a`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641cbabe81032e6beede3a4dc850d1fc1e44443f97c49a628393301c1f428062`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:7d715ef7738b0addf94a6781ff48dd6078ae85b0d26bb40e418fee4ee6627d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ad46144f5e50e5457bb9e9f8a06ba8c4851e3779a2576ec37d2a824736899e`

```dockerfile
```

-	Layers:
	-	`sha256:dedc8c889585c446bbb163d8a5210d74c241aa533895ab3cdc6bd610464d0580`  
		Last Modified: Wed, 11 Jun 2025 04:14:03 GMT  
		Size: 2.2 MB (2175115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63769367fa7293dabf75d47f54c596d481a9f54afae2ca939ff141f974997deb`  
		Last Modified: Wed, 11 Jun 2025 04:14:04 GMT  
		Size: 30.7 KB (30671 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:1fd39a59baae0a3da27befe8bbadd4914f23443cbc9b4159fd5ce829359875b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79150787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d400cc0b9a64ff3231bde898eadea11b3ce8dd9a1c531a8bd2f31230edd3dd94`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeaaf729ae44f9ac3f9b3f4551595556a417993152b53954f6f6a89f90a4954`  
		Last Modified: Wed, 11 Jun 2025 09:12:57 GMT  
		Size: 13.6 MB (13640505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928f2bed6e9375b5161e1fcbc32d598a194fc67da4a537c5d6a3aaab21aa3d0`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f75742ee54512415191653f6d3e2b7b2a4ff66bc4dcc60a24c12d00a0db76`  
		Last Modified: Wed, 11 Jun 2025 09:12:58 GMT  
		Size: 21.9 MB (21874047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189ddb23dd34f7e52d4b584e89ed11029f27d1dee76f138e62d772e61c75c0b6`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c88f7798e99a903cbf372177b9f7b8f2c70690f8dac0d589ec956038b045f`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a315ceb76a2ac2dda2c8bd167ee4d021a2f0885e86b42406a0c9eb02fb75b9e`  
		Last Modified: Wed, 11 Jun 2025 19:17:11 GMT  
		Size: 35.3 MB (35278992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197c9bbd782fcb082df2515b2222b6e5b48b183fca060886fc83d969d7daf6a`  
		Last Modified: Wed, 11 Jun 2025 19:17:08 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8e973c99bbdd714f82e6ab04b25a7dcef834cd2d7bbb384a34f1c65a900780`  
		Last Modified: Wed, 11 Jun 2025 19:18:36 GMT  
		Size: 983.1 KB (983051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a391ffa32455d41b4896457555da8b12cb549ec69ec4c078c83aed5823bc98cb`  
		Last Modified: Wed, 11 Jun 2025 19:18:36 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8229b8e376ebcbfbbfcf1c18e022a5c236be96f045dd864dea42549f79848976`  
		Last Modified: Wed, 11 Jun 2025 19:18:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:78143bd363e9e068532e34388330ac247f22cee1de541766d34a94b1e9427b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a231199ec7a4eb832715c76662085ff303c353d133f8ca2aef387491d0d58281`

```dockerfile
```

-	Layers:
	-	`sha256:f11d69a5442a1a8dab33f2a614e72c72fc13dd8bb29efbb534497f6d84ec21f2`  
		Last Modified: Wed, 11 Jun 2025 22:13:45 GMT  
		Size: 2.2 MB (2173895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f24043697a6971ebf4ad46f5f85045dbf9bd92262b3e3e81b15d8b2cb68270f`  
		Last Modified: Wed, 11 Jun 2025 22:13:46 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:095cf4a1a75e00a43f5e7312124aca62aba0904617cd7ed2fd1a3391b5eb9946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73253045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43eaf5201b1e5bf4f61358597bacf05cd564df9f76e290fef6c22d6a4c2d8fdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba389b9b1d6d27f7a263c92d52685675ded66f85f52a097bec1b658400eebc5`  
		Last Modified: Wed, 11 Jun 2025 02:39:58 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb4f8cea261544e7d849e5aa9581396ef8d4bd1b7c14ceb536acc047c9ff257`  
		Last Modified: Wed, 11 Jun 2025 02:40:00 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d9086703155ae9ef802a8a0d3e98de9aabdf18c7eb07d7758e92bef886259`  
		Last Modified: Wed, 11 Jun 2025 14:10:42 GMT  
		Size: 31.1 MB (31107690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b0b41c4564a3bd6fb68327d016b7b9e8acab85e9d3bf36c289ab0ca8ce1509`  
		Last Modified: Wed, 11 Jun 2025 14:10:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8c46aaff4fe26053289768a5165cca4fede2adcef172239064e710c0501d6a`  
		Last Modified: Wed, 11 Jun 2025 14:20:44 GMT  
		Size: 974.2 KB (974233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65f1c78f1dd61273b3e7fac034634cb1238a7d1363adbd117fb741a1ea095f8`  
		Last Modified: Wed, 11 Jun 2025 14:20:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781fec4df0b23993d663bf76d5c1d53827797435ab4f54367dd5645f77be1cc1`  
		Last Modified: Wed, 11 Jun 2025 14:20:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:622db2049cbf42407d2cc1d70399fde106734b5092fd3d9d5a163930104b13bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5237221f89c8021500be82942f1cf01305d44181e6aa30c8fe2a4fbbcb84694c`

```dockerfile
```

-	Layers:
	-	`sha256:40022f797a7ac516632052656e2b4741d3ce6dbac1117ea76623f1e7c87599d6`  
		Last Modified: Wed, 11 Jun 2025 16:14:36 GMT  
		Size: 2.2 MB (2172162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b53e4a9418a6015beae947fe3ac8fbd8d384abb338aa90b797e82fbd8dc846f`  
		Last Modified: Wed, 11 Jun 2025 16:14:37 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:7d27600ab67cfc6c40ea5fd1af1ea73dded84af12bb5e5b1a9118da4369fb824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75277343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd39398b87aa3b3309d23d5fd809f569f2a0aff333203baa1ef91633f510cf12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035d42a37d5be6b1617300170ead6ce8970a5e2e4154fe287efc8af1e2f7441`  
		Last Modified: Wed, 11 Jun 2025 08:13:18 GMT  
		Size: 13.6 MB (13640519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca62563344c489947dce07a51fbce42cb5c2f338f525f3dc64a869bb23eea05`  
		Last Modified: Wed, 11 Jun 2025 06:17:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12b2d32a5b3932415a1a3b75f1dce848914c79f4be0b381c79061048ef8945`  
		Last Modified: Wed, 11 Jun 2025 10:56:19 GMT  
		Size: 21.4 MB (21446797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13957f45dfaafb933ab00f3283ea48d057cd2179a84687ebe45ad163f535de`  
		Last Modified: Wed, 11 Jun 2025 06:17:35 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48dd1edbbaf646c03ef3f286cc921fbc422e665578b988b9d03d890364f0d5`  
		Last Modified: Wed, 11 Jun 2025 07:14:21 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7301cbc0841ac3202a1b74a41aa6043f1d38879737a0da5c17da8e63aa32c2`  
		Last Modified: Wed, 11 Jun 2025 11:04:18 GMT  
		Size: 31.8 MB (31839063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae5612a3f46089fbce6bbf1de47ad49c5c4c6be46ad9e038f366a967187ab7`  
		Last Modified: Wed, 11 Jun 2025 11:04:10 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36388a5f9c7916974f5cf3654e81ca2bc90cb34ffb6a658bf7d6584d7d1e5c6`  
		Last Modified: Wed, 11 Jun 2025 11:05:52 GMT  
		Size: 979.6 KB (979592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11693de6db036153784208d91f2a3ad3ababdeed6f12cb07075c734ff290b80`  
		Last Modified: Wed, 11 Jun 2025 11:05:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18732189f7f9d716f90279e3b63ead59c1bd5bf286e3d75453eb893472e7420e`  
		Last Modified: Wed, 11 Jun 2025 11:05:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:18842ac7bb6a77638947fad992e2138a19a8ea04f1cee94797521afd0865df51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6455776eabb0daabfa5ff498dc09f7041dc7823d04bed8961bcbc7ad54689dd2`

```dockerfile
```

-	Layers:
	-	`sha256:1db08bc0f34e2331cd5923ad8217fe1fece1225931e22ef20464a13a1929e974`  
		Last Modified: Wed, 11 Jun 2025 13:13:52 GMT  
		Size: 2.2 MB (2171944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7682273cff8d79d7d74b49145ecdece43133c158854bd9dd21a5030563f9afb3`  
		Last Modified: Wed, 11 Jun 2025 13:13:53 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:d1f7d20ea14a08d37a6d5dd4293d78b68b0441737cf0cf3b4a11e9835ed3339f
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
$ docker pull composer@sha256:66c210df6092e9ffd6aae866adda031924eec1463f027158f60be5badfb77c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76649453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274e1a9f42a6603ffb572547fe9ef6f09b2df1a46588a3bd34e375789a761414`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41ed00f4f69f9b33b5e886fedfa6143b6e95cd34c48de5a67dfca449d27075`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 3.5 MB (3468342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3dd3a928e1a1d32cf4174792bbec9d7d27add5d439d1765653b7fc22f66b92`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0721ec88e7a2844011b208a2272d18e4e309abd51c06c8e85a7fd685455524c`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f084ac2a53f05708a861a663438bea25fa87e41a10129b5c0a01e67aed1432c`  
		Last Modified: Wed, 11 Jun 2025 01:13:20 GMT  
		Size: 13.6 MB (13640521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87939f6f4e61218155cd7a88d809fc899e6d6a2b413033839baacad75def377a`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07468323dd1f0b8efa9f6be2eaf69811d60fee46c187e62fc1b05bd2bd100fa`  
		Last Modified: Wed, 11 Jun 2025 01:13:18 GMT  
		Size: 21.0 MB (20969804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d64e952347861cf8f1c360fcf1984249571751d095594a156d453d4cb4ec8b`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f854fc0d234074345274bcbda7bb11f7295b4bae6d7d400dcbe3bd892683a59`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a983a9e67738612dca1d606b492e33ae4772239864276c2e9bb701fd5ebc24ab`  
		Last Modified: Wed, 11 Jun 2025 01:14:29 GMT  
		Size: 33.9 MB (33928524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4eddb6321370e9aea8f80682132fdc57b74e210ab2efcced5a16afbbea8392`  
		Last Modified: Wed, 11 Jun 2025 01:14:27 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34096107b75deddc3c26ef831ee95ec5d5d90cd5a8a06d16d820b7ccbe12cd2d`  
		Last Modified: Wed, 11 Jun 2025 01:14:28 GMT  
		Size: 820.4 KB (820361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f33c62710586fcee38c006ff77c73c8512ff387a2bc8eb5e1b023a9f98b215e`  
		Last Modified: Wed, 11 Jun 2025 01:14:27 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4c85bab44c6212eef3eeee94969b44f80db62609d8698045bc32bb1a65bb71`  
		Last Modified: Wed, 11 Jun 2025 01:14:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:512324e4110a0bf6414d38b70de4f4a7f2248ff4fc595a5812435dba49691022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04b71eda3eddc033744c6560d8f10f7b0de55b93df4439b9a5e3e1119ce00cc`

```dockerfile
```

-	Layers:
	-	`sha256:ece2f5f71f9f874c22b05c5d9b3c8ce911621f638b9f7ea92949f4763433f11d`  
		Last Modified: Wed, 11 Jun 2025 04:14:00 GMT  
		Size: 2.2 MB (2175038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4137fd02ac043dc683560f7c85ac1dbcb28e9c9f5d5a03600e90f819c0a66961`  
		Last Modified: Wed, 11 Jun 2025 04:14:01 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:b4aa7e8e101938a53e03775f4534ee26dcfb36f70505c18e85bf66d01f9c0ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74317808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ed425857cba64206a646cabe2f9a8d324ec0d8a820783dc4291625118e4339`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d738e6a7e1662efb7b90b7f0a4b2cce2f9247f395ab8c1924148a0d2dde272c3`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 13.6 MB (13640499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeec31f51dc18a99c6251ab6abd48a6b17b9bd04c498ca1ce606fbe0119a506`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a9bea01d63368fc6a169811ad55c9f7baf8d06c4a3c909bea5606bf5d161c`  
		Last Modified: Tue, 10 Jun 2025 23:54:15 GMT  
		Size: 19.1 MB (19091501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab1a6cbed4c7bce681ea2c1ba6335b04364d328abb8504ac38b7cb01546c1e`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7ac6548196a7241e2ff5aeb2ebaa92bd912151a57decbc09707501826e55d`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 20.0 KB (19986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a52088bfe28e3394348499664afc0150422c289f500eeb5736a846fb654a75`  
		Last Modified: Wed, 11 Jun 2025 01:34:01 GMT  
		Size: 33.8 MB (33807058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfadb48984526f1d970423f530584b05a533cf586b26af60f4077fe0d75af65`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07dea40c6caddf6bdae192a744e3231fdcca79d1be718ed3bef4de7f8b4fbbf`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 820.5 KB (820524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d457fcbfa723120617f86dcb4efa382bf960cdfc50ac9c337575328a956407f6`  
		Last Modified: Fri, 06 Jun 2025 18:41:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d13ade04f1c3949a7c8fad3b6d3e005313812670a868b8e35c048ff3d3e342f`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:64cfcb2cfcd2778f1199141172672925fad657e6dac36c3ea0ca54727b3929b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a9079774811c129322fa73f782aa6eaaca32d9cf62043301abb742e7ca7d62`

```dockerfile
```

-	Layers:
	-	`sha256:7983cb32e3739991648b53a980ad98f5bb4686b536f719a02f9fad1f437649e6`  
		Last Modified: Wed, 11 Jun 2025 04:14:06 GMT  
		Size: 30.3 KB (30282 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:58893f135334ec29555376b95fc04c9862a2f8332e3e6c9046c5815d31d1bd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71079557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c0e947182a4e650b5bf0a550f9161cc3d2754207790a89b482c58ee5824fa0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc30cbedbf54d9515871da07398fab0a70176613fac2230d3b598dd61f7dea64`  
		Last Modified: Wed, 11 Jun 2025 11:39:15 GMT  
		Size: 13.6 MB (13640514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ce30718845b98da85d3f2d4b2a979b2c4c9a318019ee4c5a3897dbb7a35b7`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788f675ffad6ad044155d5d8863ebb06f9142fe48298e02c274f65b961260418`  
		Last Modified: Wed, 11 Jun 2025 11:39:16 GMT  
		Size: 18.1 MB (18066806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2746b1c3debbab52b7827813726cffe0c2a6316b37ceefd0c7c7085cb9219577`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60271e3bc7668883349e90adf3ad21e0a859246f2f3d1430bd66ba8532b8cc1`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 20.0 KB (19984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bab94d85f8d4b9a1b97076f46ba751dc69827e8eaeb013290df1d46760098`  
		Last Modified: Wed, 11 Jun 2025 19:24:25 GMT  
		Size: 32.1 MB (32069944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d696523fff13201849f3282a4e284e28727f89ba185ff8bdb03a58fc314ccb55`  
		Last Modified: Wed, 11 Jun 2025 18:47:28 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb0b283c0550b0d57ccd0a7a90fdd170a824a4fb688f9ca63d43272a0e4a68f`  
		Last Modified: Wed, 11 Jun 2025 18:48:14 GMT  
		Size: 810.8 KB (810804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b29f0dbbbf18851f15f6ca488e3c9c66614a80976f420f840344823dd79f56`  
		Last Modified: Wed, 11 Jun 2025 18:48:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b2d00a029d07cf1009735df624fd16018bc88ec70ce9902ae0b13184835d1d`  
		Last Modified: Wed, 11 Jun 2025 18:48:20 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:7e8eab146f11f853085da9ff953ff9d4ab3c78ddd7288b0bbce287f7428ec379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439f87fb6a2364d089c9a12622c33e05239477d5c171d1b96ff897b3934588ef`

```dockerfile
```

-	Layers:
	-	`sha256:b49cc057be66bf6aa815e35859c7c7ee91dd72e94920c37a7e49c6d4ed1a8f84`  
		Last Modified: Wed, 11 Jun 2025 19:13:49 GMT  
		Size: 2.2 MB (2175354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cca50545151f25b54270eadf543a8ff4824180bb0dfeb6e1051852dc1a3467c`  
		Last Modified: Wed, 11 Jun 2025 19:13:50 GMT  
		Size: 30.5 KB (30497 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:9044a7410ca203d0a6900fe8157d8b61b4689354676c576c59c2ca5d311c2a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76621790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d36340425074e3267adab0200c49b19b26091c03d75492134fe000a5f2c56b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e263556d24cfaaa81ec9153b95e1b25d54abdb35b46c3c74fa988a9f252f3`  
		Last Modified: Wed, 11 Jun 2025 09:16:54 GMT  
		Size: 3.5 MB (3470681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5bea448bb73ac691df99daf5772e7cb7307f122b4e0544c289a55be9ee24`  
		Last Modified: Wed, 11 Jun 2025 09:17:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a64acbbc8d220ea4c16baed763b26899f58299a8b85d3b8513f03b3023893`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123dcf4adf55a39c8cf4f202302f0a9dfd6d576c94bf8db94686e5a5ee1f4cf4`  
		Last Modified: Wed, 11 Jun 2025 09:33:08 GMT  
		Size: 13.6 MB (13640507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff08fc5740a571af506cddc0c38e20506f6151e574d4a10d77b748c7c3bd4b`  
		Last Modified: Wed, 11 Jun 2025 09:08:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc080435edc41cfa70a84f9586ffca3f880a9b4cedccc53c481889b18e1e1c2`  
		Last Modified: Wed, 11 Jun 2025 09:33:10 GMT  
		Size: 20.5 MB (20518887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3995038baa7f047e93509966aa2798fbc7bddf48517c43343b9add69edd5df`  
		Last Modified: Wed, 11 Jun 2025 09:08:59 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae69002966a0d0881786cca5d1dfa7b1fb54c0e7b1e4b6bf9c41f92f6208ec`  
		Last Modified: Wed, 11 Jun 2025 09:17:23 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5db0ec87df386dd8e7ed3e3a943ff4f92de4b419fe7f9bb1b4051dd24a6721`  
		Last Modified: Wed, 11 Jun 2025 15:13:38 GMT  
		Size: 34.0 MB (34010836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae1182fb6a9705ef49f6995317dfcfc6ef3d4b2292bc160d0ba7f8c246dda2e`  
		Last Modified: Wed, 11 Jun 2025 15:13:33 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dfc85b8d16b0b91207b67136a251d9ce8cb168c850f64361a44b74eb632811`  
		Last Modified: Wed, 11 Jun 2025 15:13:34 GMT  
		Size: 820.1 KB (820096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801a936554b178c085f387589b6ab70e3a77b266c792480de4b102e440b5ec69`  
		Last Modified: Wed, 11 Jun 2025 15:13:34 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfea21537f7903164af0fde73e8af3f3e4bb31c1202f44c707716aa939f99af`  
		Last Modified: Wed, 11 Jun 2025 15:13:34 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:d4ac00e2410ff8bd92a7611f7037d8f15546d354f2c4a2381701593533daac36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb743ca06e77355f35a167507d2ef19a4f8eafffb33dc3953830b73b0e7d7327`

```dockerfile
```

-	Layers:
	-	`sha256:7adbbd77a0986b5f5fdaee5236dd188409aa46b4d1ab6910c8d9e50cf9ba35a0`  
		Last Modified: Wed, 11 Jun 2025 16:16:36 GMT  
		Size: 2.2 MB (2175178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4f36bc05bbc26c871efc8f9fe269ca0e1e870ccf0a8856bb6ef17c7cdb0bf3`  
		Last Modified: Wed, 11 Jun 2025 16:16:36 GMT  
		Size: 30.5 KB (30525 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:e58c3feb27440e5618d734afd387375c6b5e4349448cad8511c199832dc837c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77573235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2857e9dc2712a9e06ed2418cdac6fc9e27233b5acbd1f75203413982c3edadb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298f020aec5b2eb58f3f5d72ed081bd6c76a95799b7e438e4f3384447e42693d`  
		Last Modified: Wed, 11 Jun 2025 01:13:13 GMT  
		Size: 3.5 MB (3527774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ebeb8397f1f59382fb3bd2f49e7ae5aa3c63f7a6f5adde3d5af0fe196ad48`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c3fa431069cd36b1283a6dd73ec3c559701f45df22999775e61dd0dd4d578`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7db0fb8a413bd77d83d365246beba56a6d3ab745a296bb3119dd1c4844e7e2`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 13.6 MB (13640494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c81720a5bbf56ccfa06979187dbca8afa1859fb3d323625fe188373b9a06ed`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8fb25f24bc12988d302f27fbc0c27090c75c814e4f8dcb4396e125eafae7cb`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 21.5 MB (21493036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b67d63641d3800bf94c0e5eb453a80e9e00ec38acbc41e8b2dbe883e470dd6d`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821e028fb8ab3dacea139b63763d5d53b2d0981367d47fcd3f94182a0a2ac456`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 20.2 KB (20182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5a5771e66b8b5e97c3a2a977ca7089edbbca018038d8b56551bbbc0a8d6d01`  
		Last Modified: Wed, 11 Jun 2025 01:14:24 GMT  
		Size: 34.4 MB (34436667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d09bf8efac1bb2cb2458be039d96f810d55feb69816e0ae630509068dac26`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1e8618a4823c0932806a1a13fbea222f86845076795faa053ecbec1f0d6faa`  
		Last Modified: Wed, 11 Jun 2025 01:14:24 GMT  
		Size: 834.2 KB (834197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bf71238eca349012bf52da0f1f044400815dc5c63c3e0d0288129c0099d23c`  
		Last Modified: Wed, 11 Jun 2025 01:14:24 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387efffd50fee23b95960319fa3959d346523333031fe1d80e9259d8eaa96a01`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:3291d3d1223e7ff57f0794dac617e0a065379495827e752dc779fc6b9adfb2b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d841ab56e87fbb2face98ec347c5d4c254578da7ff3da9f83ef7e2374c43f3e7`

```dockerfile
```

-	Layers:
	-	`sha256:f4b5321199f919e712820423725d97f48a66609b51ef20a0a0653f7922f39d1d`  
		Last Modified: Wed, 11 Jun 2025 04:14:19 GMT  
		Size: 2.2 MB (2174826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462b55391ee34015a5c4784b415a263c63d3f8b068f1b00fe9a649b3c0cb16ca`  
		Last Modified: Wed, 11 Jun 2025 04:14:19 GMT  
		Size: 30.4 KB (30372 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:71aa4fb51ed8eb9644b328c54c8dbd79b62fc9e1a2a49d05ffbda05e0aaa5359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78994764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f211c2e27a87bc96d094c6ccb729242c29d0744ca672f3092c687e605a14f648`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeaaf729ae44f9ac3f9b3f4551595556a417993152b53954f6f6a89f90a4954`  
		Last Modified: Wed, 11 Jun 2025 09:12:57 GMT  
		Size: 13.6 MB (13640505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928f2bed6e9375b5161e1fcbc32d598a194fc67da4a537c5d6a3aaab21aa3d0`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f75742ee54512415191653f6d3e2b7b2a4ff66bc4dcc60a24c12d00a0db76`  
		Last Modified: Wed, 11 Jun 2025 09:12:58 GMT  
		Size: 21.9 MB (21874047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189ddb23dd34f7e52d4b584e89ed11029f27d1dee76f138e62d772e61c75c0b6`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c88f7798e99a903cbf372177b9f7b8f2c70690f8dac0d589ec956038b045f`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a315ceb76a2ac2dda2c8bd167ee4d021a2f0885e86b42406a0c9eb02fb75b9e`  
		Last Modified: Wed, 11 Jun 2025 19:17:11 GMT  
		Size: 35.3 MB (35278992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197c9bbd782fcb082df2515b2222b6e5b48b183fca060886fc83d969d7daf6a`  
		Last Modified: Wed, 11 Jun 2025 19:17:08 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47adf6bb7b9725c3f35a917e6a4788e15e78e2d5f2c6c85b8519cd883a6c868`  
		Last Modified: Wed, 11 Jun 2025 19:17:09 GMT  
		Size: 827.0 KB (827027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0370e10fb9013c22215e0a1c53730207f82dbcf7c04bfc697979d4d2c23c672`  
		Last Modified: Wed, 11 Jun 2025 19:17:10 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b04a1f8b11ff0e8bffdcfb54d185f40d9ce0064b3e530f991ab7e45d3a2502`  
		Last Modified: Wed, 11 Jun 2025 19:17:10 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:109ce7c6ad825e2f9db75f1454aa4eee4c1f8410800be5f83dac44f96929d961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029ad0a254e8c664e15a883aee697a19477f33b01a2138dd82265136223f95b0`

```dockerfile
```

-	Layers:
	-	`sha256:186b2b238a8d42cb52d9062db2c413f6d9b50458fa75bd34dac85458f0b686ec`  
		Last Modified: Wed, 11 Jun 2025 22:13:55 GMT  
		Size: 2.2 MB (2173595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0618ed7cbb2b799975882052f2b94e8ab513868dc41d8345cb8b958cdb373cfe`  
		Last Modified: Wed, 11 Jun 2025 22:13:56 GMT  
		Size: 30.4 KB (30444 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:bfe80827bc9e5b2930762190b55732402255b8a181f8df2b5fdd63364720454a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73096995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b61a446bf05f8cf261e8b5ca68a500ea349fb70f01ac94af71786e9c7b5f1e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba389b9b1d6d27f7a263c92d52685675ded66f85f52a097bec1b658400eebc5`  
		Last Modified: Wed, 11 Jun 2025 02:39:58 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb4f8cea261544e7d849e5aa9581396ef8d4bd1b7c14ceb536acc047c9ff257`  
		Last Modified: Wed, 11 Jun 2025 02:40:00 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d9086703155ae9ef802a8a0d3e98de9aabdf18c7eb07d7758e92bef886259`  
		Last Modified: Wed, 11 Jun 2025 14:10:42 GMT  
		Size: 31.1 MB (31107690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b0b41c4564a3bd6fb68327d016b7b9e8acab85e9d3bf36c289ab0ca8ce1509`  
		Last Modified: Wed, 11 Jun 2025 14:10:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd07fd0d74a58ec594fbc8a688e3b05865a7f96d929c001758e8500260f120d0`  
		Last Modified: Wed, 11 Jun 2025 14:10:32 GMT  
		Size: 818.2 KB (818183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb153d0ff046a6570955b52d245bb74ed310886b1b41d7f1276a94be51d1651e`  
		Last Modified: Wed, 11 Jun 2025 14:10:32 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0107a874ee1b41715b767b7e76f9c687e4103a990e1ad58a680f956b3a6a8e6`  
		Last Modified: Wed, 11 Jun 2025 14:10:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:5ebb7ee2da696e426e23ef9915deab697fdf041040ef86646a171fc28290d6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3878fc9b762a647ee250302ecbd413ba31f025c2aa113487791b6993e2d722b8`

```dockerfile
```

-	Layers:
	-	`sha256:8eb63f1ce3f7eee516d9412f330b8f069a2aa8f274b19d2e5159366987013326`  
		Last Modified: Wed, 11 Jun 2025 16:16:49 GMT  
		Size: 2.2 MB (2171862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ee7486ca8791bfa6fef745038a5ce0428eaad643e8ec60b82c8c3c429dc415`  
		Last Modified: Wed, 11 Jun 2025 16:16:50 GMT  
		Size: 30.4 KB (30443 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:eb73759c697f34583db9b7494c7e3ede0cab059e5b1ecb3284e8b669556ac825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75121248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16813e2e25d58914b7f1eef4abf346a0c5c5e2a8fca7a5e73979a19adbd18bd2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035d42a37d5be6b1617300170ead6ce8970a5e2e4154fe287efc8af1e2f7441`  
		Last Modified: Wed, 11 Jun 2025 08:13:18 GMT  
		Size: 13.6 MB (13640519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca62563344c489947dce07a51fbce42cb5c2f338f525f3dc64a869bb23eea05`  
		Last Modified: Wed, 11 Jun 2025 06:17:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12b2d32a5b3932415a1a3b75f1dce848914c79f4be0b381c79061048ef8945`  
		Last Modified: Wed, 11 Jun 2025 10:56:19 GMT  
		Size: 21.4 MB (21446797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13957f45dfaafb933ab00f3283ea48d057cd2179a84687ebe45ad163f535de`  
		Last Modified: Wed, 11 Jun 2025 06:17:35 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48dd1edbbaf646c03ef3f286cc921fbc422e665578b988b9d03d890364f0d5`  
		Last Modified: Wed, 11 Jun 2025 07:14:21 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7301cbc0841ac3202a1b74a41aa6043f1d38879737a0da5c17da8e63aa32c2`  
		Last Modified: Wed, 11 Jun 2025 11:04:18 GMT  
		Size: 31.8 MB (31839063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae5612a3f46089fbce6bbf1de47ad49c5c4c6be46ad9e038f366a967187ab7`  
		Last Modified: Wed, 11 Jun 2025 11:04:10 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70afb032b9f3ac1656f5cca28aa6ec4c1623d47b8430c88d251746f6984495ae`  
		Last Modified: Wed, 11 Jun 2025 11:04:11 GMT  
		Size: 823.5 KB (823498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1267181c9b46b09997bd9cce442e3bac321de699df11a589af306e7a077084`  
		Last Modified: Wed, 11 Jun 2025 11:04:12 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f7264726be68bf863c89466f20b9622a3f4ea819a2af3233e3a056c28d822f`  
		Last Modified: Wed, 11 Jun 2025 11:04:12 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:a00f107a9222298d04a4296d68b654eda679f38487306c5030196a196197e226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63a1562e3a671aa92d1395152adb5b0079f86770497164b6b2ad4dcad16fe6e`

```dockerfile
```

-	Layers:
	-	`sha256:404683acfdb9dcf447ee6e137627e78d91adcaece87a371f891eb286377dbef3`  
		Last Modified: Wed, 11 Jun 2025 13:13:55 GMT  
		Size: 2.2 MB (2171650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4d2f8be03d02a58b777e3161bd961cf75269a73ae8d084cfabe949c7b04a3a`  
		Last Modified: Wed, 11 Jun 2025 13:13:56 GMT  
		Size: 30.4 KB (30402 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.25`

```console
$ docker pull composer@sha256:d1f7d20ea14a08d37a6d5dd4293d78b68b0441737cf0cf3b4a11e9835ed3339f
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
$ docker pull composer@sha256:66c210df6092e9ffd6aae866adda031924eec1463f027158f60be5badfb77c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76649453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274e1a9f42a6603ffb572547fe9ef6f09b2df1a46588a3bd34e375789a761414`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41ed00f4f69f9b33b5e886fedfa6143b6e95cd34c48de5a67dfca449d27075`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 3.5 MB (3468342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3dd3a928e1a1d32cf4174792bbec9d7d27add5d439d1765653b7fc22f66b92`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0721ec88e7a2844011b208a2272d18e4e309abd51c06c8e85a7fd685455524c`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f084ac2a53f05708a861a663438bea25fa87e41a10129b5c0a01e67aed1432c`  
		Last Modified: Wed, 11 Jun 2025 01:13:20 GMT  
		Size: 13.6 MB (13640521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87939f6f4e61218155cd7a88d809fc899e6d6a2b413033839baacad75def377a`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07468323dd1f0b8efa9f6be2eaf69811d60fee46c187e62fc1b05bd2bd100fa`  
		Last Modified: Wed, 11 Jun 2025 01:13:18 GMT  
		Size: 21.0 MB (20969804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d64e952347861cf8f1c360fcf1984249571751d095594a156d453d4cb4ec8b`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f854fc0d234074345274bcbda7bb11f7295b4bae6d7d400dcbe3bd892683a59`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a983a9e67738612dca1d606b492e33ae4772239864276c2e9bb701fd5ebc24ab`  
		Last Modified: Wed, 11 Jun 2025 01:14:29 GMT  
		Size: 33.9 MB (33928524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4eddb6321370e9aea8f80682132fdc57b74e210ab2efcced5a16afbbea8392`  
		Last Modified: Wed, 11 Jun 2025 01:14:27 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34096107b75deddc3c26ef831ee95ec5d5d90cd5a8a06d16d820b7ccbe12cd2d`  
		Last Modified: Wed, 11 Jun 2025 01:14:28 GMT  
		Size: 820.4 KB (820361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f33c62710586fcee38c006ff77c73c8512ff387a2bc8eb5e1b023a9f98b215e`  
		Last Modified: Wed, 11 Jun 2025 01:14:27 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4c85bab44c6212eef3eeee94969b44f80db62609d8698045bc32bb1a65bb71`  
		Last Modified: Wed, 11 Jun 2025 01:14:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:512324e4110a0bf6414d38b70de4f4a7f2248ff4fc595a5812435dba49691022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04b71eda3eddc033744c6560d8f10f7b0de55b93df4439b9a5e3e1119ce00cc`

```dockerfile
```

-	Layers:
	-	`sha256:ece2f5f71f9f874c22b05c5d9b3c8ce911621f638b9f7ea92949f4763433f11d`  
		Last Modified: Wed, 11 Jun 2025 04:14:00 GMT  
		Size: 2.2 MB (2175038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4137fd02ac043dc683560f7c85ac1dbcb28e9c9f5d5a03600e90f819c0a66961`  
		Last Modified: Wed, 11 Jun 2025 04:14:01 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v6

```console
$ docker pull composer@sha256:b4aa7e8e101938a53e03775f4534ee26dcfb36f70505c18e85bf66d01f9c0ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74317808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ed425857cba64206a646cabe2f9a8d324ec0d8a820783dc4291625118e4339`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d738e6a7e1662efb7b90b7f0a4b2cce2f9247f395ab8c1924148a0d2dde272c3`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 13.6 MB (13640499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeec31f51dc18a99c6251ab6abd48a6b17b9bd04c498ca1ce606fbe0119a506`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a9bea01d63368fc6a169811ad55c9f7baf8d06c4a3c909bea5606bf5d161c`  
		Last Modified: Tue, 10 Jun 2025 23:54:15 GMT  
		Size: 19.1 MB (19091501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab1a6cbed4c7bce681ea2c1ba6335b04364d328abb8504ac38b7cb01546c1e`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7ac6548196a7241e2ff5aeb2ebaa92bd912151a57decbc09707501826e55d`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 20.0 KB (19986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a52088bfe28e3394348499664afc0150422c289f500eeb5736a846fb654a75`  
		Last Modified: Wed, 11 Jun 2025 01:34:01 GMT  
		Size: 33.8 MB (33807058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfadb48984526f1d970423f530584b05a533cf586b26af60f4077fe0d75af65`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07dea40c6caddf6bdae192a744e3231fdcca79d1be718ed3bef4de7f8b4fbbf`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 820.5 KB (820524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d457fcbfa723120617f86dcb4efa382bf960cdfc50ac9c337575328a956407f6`  
		Last Modified: Fri, 06 Jun 2025 18:41:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d13ade04f1c3949a7c8fad3b6d3e005313812670a868b8e35c048ff3d3e342f`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:64cfcb2cfcd2778f1199141172672925fad657e6dac36c3ea0ca54727b3929b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a9079774811c129322fa73f782aa6eaaca32d9cf62043301abb742e7ca7d62`

```dockerfile
```

-	Layers:
	-	`sha256:7983cb32e3739991648b53a980ad98f5bb4686b536f719a02f9fad1f437649e6`  
		Last Modified: Wed, 11 Jun 2025 04:14:06 GMT  
		Size: 30.3 KB (30282 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v7

```console
$ docker pull composer@sha256:58893f135334ec29555376b95fc04c9862a2f8332e3e6c9046c5815d31d1bd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71079557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c0e947182a4e650b5bf0a550f9161cc3d2754207790a89b482c58ee5824fa0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc30cbedbf54d9515871da07398fab0a70176613fac2230d3b598dd61f7dea64`  
		Last Modified: Wed, 11 Jun 2025 11:39:15 GMT  
		Size: 13.6 MB (13640514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ce30718845b98da85d3f2d4b2a979b2c4c9a318019ee4c5a3897dbb7a35b7`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788f675ffad6ad044155d5d8863ebb06f9142fe48298e02c274f65b961260418`  
		Last Modified: Wed, 11 Jun 2025 11:39:16 GMT  
		Size: 18.1 MB (18066806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2746b1c3debbab52b7827813726cffe0c2a6316b37ceefd0c7c7085cb9219577`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60271e3bc7668883349e90adf3ad21e0a859246f2f3d1430bd66ba8532b8cc1`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 20.0 KB (19984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bab94d85f8d4b9a1b97076f46ba751dc69827e8eaeb013290df1d46760098`  
		Last Modified: Wed, 11 Jun 2025 19:24:25 GMT  
		Size: 32.1 MB (32069944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d696523fff13201849f3282a4e284e28727f89ba185ff8bdb03a58fc314ccb55`  
		Last Modified: Wed, 11 Jun 2025 18:47:28 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb0b283c0550b0d57ccd0a7a90fdd170a824a4fb688f9ca63d43272a0e4a68f`  
		Last Modified: Wed, 11 Jun 2025 18:48:14 GMT  
		Size: 810.8 KB (810804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b29f0dbbbf18851f15f6ca488e3c9c66614a80976f420f840344823dd79f56`  
		Last Modified: Wed, 11 Jun 2025 18:48:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b2d00a029d07cf1009735df624fd16018bc88ec70ce9902ae0b13184835d1d`  
		Last Modified: Wed, 11 Jun 2025 18:48:20 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:7e8eab146f11f853085da9ff953ff9d4ab3c78ddd7288b0bbce287f7428ec379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439f87fb6a2364d089c9a12622c33e05239477d5c171d1b96ff897b3934588ef`

```dockerfile
```

-	Layers:
	-	`sha256:b49cc057be66bf6aa815e35859c7c7ee91dd72e94920c37a7e49c6d4ed1a8f84`  
		Last Modified: Wed, 11 Jun 2025 19:13:49 GMT  
		Size: 2.2 MB (2175354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cca50545151f25b54270eadf543a8ff4824180bb0dfeb6e1051852dc1a3467c`  
		Last Modified: Wed, 11 Jun 2025 19:13:50 GMT  
		Size: 30.5 KB (30497 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:9044a7410ca203d0a6900fe8157d8b61b4689354676c576c59c2ca5d311c2a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76621790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d36340425074e3267adab0200c49b19b26091c03d75492134fe000a5f2c56b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e263556d24cfaaa81ec9153b95e1b25d54abdb35b46c3c74fa988a9f252f3`  
		Last Modified: Wed, 11 Jun 2025 09:16:54 GMT  
		Size: 3.5 MB (3470681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5bea448bb73ac691df99daf5772e7cb7307f122b4e0544c289a55be9ee24`  
		Last Modified: Wed, 11 Jun 2025 09:17:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a64acbbc8d220ea4c16baed763b26899f58299a8b85d3b8513f03b3023893`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123dcf4adf55a39c8cf4f202302f0a9dfd6d576c94bf8db94686e5a5ee1f4cf4`  
		Last Modified: Wed, 11 Jun 2025 09:33:08 GMT  
		Size: 13.6 MB (13640507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff08fc5740a571af506cddc0c38e20506f6151e574d4a10d77b748c7c3bd4b`  
		Last Modified: Wed, 11 Jun 2025 09:08:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc080435edc41cfa70a84f9586ffca3f880a9b4cedccc53c481889b18e1e1c2`  
		Last Modified: Wed, 11 Jun 2025 09:33:10 GMT  
		Size: 20.5 MB (20518887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3995038baa7f047e93509966aa2798fbc7bddf48517c43343b9add69edd5df`  
		Last Modified: Wed, 11 Jun 2025 09:08:59 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae69002966a0d0881786cca5d1dfa7b1fb54c0e7b1e4b6bf9c41f92f6208ec`  
		Last Modified: Wed, 11 Jun 2025 09:17:23 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5db0ec87df386dd8e7ed3e3a943ff4f92de4b419fe7f9bb1b4051dd24a6721`  
		Last Modified: Wed, 11 Jun 2025 15:13:38 GMT  
		Size: 34.0 MB (34010836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae1182fb6a9705ef49f6995317dfcfc6ef3d4b2292bc160d0ba7f8c246dda2e`  
		Last Modified: Wed, 11 Jun 2025 15:13:33 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dfc85b8d16b0b91207b67136a251d9ce8cb168c850f64361a44b74eb632811`  
		Last Modified: Wed, 11 Jun 2025 15:13:34 GMT  
		Size: 820.1 KB (820096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801a936554b178c085f387589b6ab70e3a77b266c792480de4b102e440b5ec69`  
		Last Modified: Wed, 11 Jun 2025 15:13:34 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfea21537f7903164af0fde73e8af3f3e4bb31c1202f44c707716aa939f99af`  
		Last Modified: Wed, 11 Jun 2025 15:13:34 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:d4ac00e2410ff8bd92a7611f7037d8f15546d354f2c4a2381701593533daac36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb743ca06e77355f35a167507d2ef19a4f8eafffb33dc3953830b73b0e7d7327`

```dockerfile
```

-	Layers:
	-	`sha256:7adbbd77a0986b5f5fdaee5236dd188409aa46b4d1ab6910c8d9e50cf9ba35a0`  
		Last Modified: Wed, 11 Jun 2025 16:16:36 GMT  
		Size: 2.2 MB (2175178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4f36bc05bbc26c871efc8f9fe269ca0e1e870ccf0a8856bb6ef17c7cdb0bf3`  
		Last Modified: Wed, 11 Jun 2025 16:16:36 GMT  
		Size: 30.5 KB (30525 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; 386

```console
$ docker pull composer@sha256:e58c3feb27440e5618d734afd387375c6b5e4349448cad8511c199832dc837c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77573235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2857e9dc2712a9e06ed2418cdac6fc9e27233b5acbd1f75203413982c3edadb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298f020aec5b2eb58f3f5d72ed081bd6c76a95799b7e438e4f3384447e42693d`  
		Last Modified: Wed, 11 Jun 2025 01:13:13 GMT  
		Size: 3.5 MB (3527774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ebeb8397f1f59382fb3bd2f49e7ae5aa3c63f7a6f5adde3d5af0fe196ad48`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c3fa431069cd36b1283a6dd73ec3c559701f45df22999775e61dd0dd4d578`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7db0fb8a413bd77d83d365246beba56a6d3ab745a296bb3119dd1c4844e7e2`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 13.6 MB (13640494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c81720a5bbf56ccfa06979187dbca8afa1859fb3d323625fe188373b9a06ed`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8fb25f24bc12988d302f27fbc0c27090c75c814e4f8dcb4396e125eafae7cb`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 21.5 MB (21493036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b67d63641d3800bf94c0e5eb453a80e9e00ec38acbc41e8b2dbe883e470dd6d`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821e028fb8ab3dacea139b63763d5d53b2d0981367d47fcd3f94182a0a2ac456`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 20.2 KB (20182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5a5771e66b8b5e97c3a2a977ca7089edbbca018038d8b56551bbbc0a8d6d01`  
		Last Modified: Wed, 11 Jun 2025 01:14:24 GMT  
		Size: 34.4 MB (34436667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d09bf8efac1bb2cb2458be039d96f810d55feb69816e0ae630509068dac26`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1e8618a4823c0932806a1a13fbea222f86845076795faa053ecbec1f0d6faa`  
		Last Modified: Wed, 11 Jun 2025 01:14:24 GMT  
		Size: 834.2 KB (834197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bf71238eca349012bf52da0f1f044400815dc5c63c3e0d0288129c0099d23c`  
		Last Modified: Wed, 11 Jun 2025 01:14:24 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387efffd50fee23b95960319fa3959d346523333031fe1d80e9259d8eaa96a01`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:3291d3d1223e7ff57f0794dac617e0a065379495827e752dc779fc6b9adfb2b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d841ab56e87fbb2face98ec347c5d4c254578da7ff3da9f83ef7e2374c43f3e7`

```dockerfile
```

-	Layers:
	-	`sha256:f4b5321199f919e712820423725d97f48a66609b51ef20a0a0653f7922f39d1d`  
		Last Modified: Wed, 11 Jun 2025 04:14:19 GMT  
		Size: 2.2 MB (2174826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462b55391ee34015a5c4784b415a263c63d3f8b068f1b00fe9a649b3c0cb16ca`  
		Last Modified: Wed, 11 Jun 2025 04:14:19 GMT  
		Size: 30.4 KB (30372 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; ppc64le

```console
$ docker pull composer@sha256:71aa4fb51ed8eb9644b328c54c8dbd79b62fc9e1a2a49d05ffbda05e0aaa5359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78994764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f211c2e27a87bc96d094c6ccb729242c29d0744ca672f3092c687e605a14f648`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeaaf729ae44f9ac3f9b3f4551595556a417993152b53954f6f6a89f90a4954`  
		Last Modified: Wed, 11 Jun 2025 09:12:57 GMT  
		Size: 13.6 MB (13640505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928f2bed6e9375b5161e1fcbc32d598a194fc67da4a537c5d6a3aaab21aa3d0`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f75742ee54512415191653f6d3e2b7b2a4ff66bc4dcc60a24c12d00a0db76`  
		Last Modified: Wed, 11 Jun 2025 09:12:58 GMT  
		Size: 21.9 MB (21874047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189ddb23dd34f7e52d4b584e89ed11029f27d1dee76f138e62d772e61c75c0b6`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c88f7798e99a903cbf372177b9f7b8f2c70690f8dac0d589ec956038b045f`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a315ceb76a2ac2dda2c8bd167ee4d021a2f0885e86b42406a0c9eb02fb75b9e`  
		Last Modified: Wed, 11 Jun 2025 19:17:11 GMT  
		Size: 35.3 MB (35278992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197c9bbd782fcb082df2515b2222b6e5b48b183fca060886fc83d969d7daf6a`  
		Last Modified: Wed, 11 Jun 2025 19:17:08 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47adf6bb7b9725c3f35a917e6a4788e15e78e2d5f2c6c85b8519cd883a6c868`  
		Last Modified: Wed, 11 Jun 2025 19:17:09 GMT  
		Size: 827.0 KB (827027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0370e10fb9013c22215e0a1c53730207f82dbcf7c04bfc697979d4d2c23c672`  
		Last Modified: Wed, 11 Jun 2025 19:17:10 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b04a1f8b11ff0e8bffdcfb54d185f40d9ce0064b3e530f991ab7e45d3a2502`  
		Last Modified: Wed, 11 Jun 2025 19:17:10 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:109ce7c6ad825e2f9db75f1454aa4eee4c1f8410800be5f83dac44f96929d961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029ad0a254e8c664e15a883aee697a19477f33b01a2138dd82265136223f95b0`

```dockerfile
```

-	Layers:
	-	`sha256:186b2b238a8d42cb52d9062db2c413f6d9b50458fa75bd34dac85458f0b686ec`  
		Last Modified: Wed, 11 Jun 2025 22:13:55 GMT  
		Size: 2.2 MB (2173595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0618ed7cbb2b799975882052f2b94e8ab513868dc41d8345cb8b958cdb373cfe`  
		Last Modified: Wed, 11 Jun 2025 22:13:56 GMT  
		Size: 30.4 KB (30444 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; riscv64

```console
$ docker pull composer@sha256:bfe80827bc9e5b2930762190b55732402255b8a181f8df2b5fdd63364720454a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73096995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b61a446bf05f8cf261e8b5ca68a500ea349fb70f01ac94af71786e9c7b5f1e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba389b9b1d6d27f7a263c92d52685675ded66f85f52a097bec1b658400eebc5`  
		Last Modified: Wed, 11 Jun 2025 02:39:58 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb4f8cea261544e7d849e5aa9581396ef8d4bd1b7c14ceb536acc047c9ff257`  
		Last Modified: Wed, 11 Jun 2025 02:40:00 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d9086703155ae9ef802a8a0d3e98de9aabdf18c7eb07d7758e92bef886259`  
		Last Modified: Wed, 11 Jun 2025 14:10:42 GMT  
		Size: 31.1 MB (31107690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b0b41c4564a3bd6fb68327d016b7b9e8acab85e9d3bf36c289ab0ca8ce1509`  
		Last Modified: Wed, 11 Jun 2025 14:10:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd07fd0d74a58ec594fbc8a688e3b05865a7f96d929c001758e8500260f120d0`  
		Last Modified: Wed, 11 Jun 2025 14:10:32 GMT  
		Size: 818.2 KB (818183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb153d0ff046a6570955b52d245bb74ed310886b1b41d7f1276a94be51d1651e`  
		Last Modified: Wed, 11 Jun 2025 14:10:32 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0107a874ee1b41715b767b7e76f9c687e4103a990e1ad58a680f956b3a6a8e6`  
		Last Modified: Wed, 11 Jun 2025 14:10:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:5ebb7ee2da696e426e23ef9915deab697fdf041040ef86646a171fc28290d6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3878fc9b762a647ee250302ecbd413ba31f025c2aa113487791b6993e2d722b8`

```dockerfile
```

-	Layers:
	-	`sha256:8eb63f1ce3f7eee516d9412f330b8f069a2aa8f274b19d2e5159366987013326`  
		Last Modified: Wed, 11 Jun 2025 16:16:49 GMT  
		Size: 2.2 MB (2171862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ee7486ca8791bfa6fef745038a5ce0428eaad643e8ec60b82c8c3c429dc415`  
		Last Modified: Wed, 11 Jun 2025 16:16:50 GMT  
		Size: 30.4 KB (30443 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; s390x

```console
$ docker pull composer@sha256:eb73759c697f34583db9b7494c7e3ede0cab059e5b1ecb3284e8b669556ac825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75121248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16813e2e25d58914b7f1eef4abf346a0c5c5e2a8fca7a5e73979a19adbd18bd2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035d42a37d5be6b1617300170ead6ce8970a5e2e4154fe287efc8af1e2f7441`  
		Last Modified: Wed, 11 Jun 2025 08:13:18 GMT  
		Size: 13.6 MB (13640519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca62563344c489947dce07a51fbce42cb5c2f338f525f3dc64a869bb23eea05`  
		Last Modified: Wed, 11 Jun 2025 06:17:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12b2d32a5b3932415a1a3b75f1dce848914c79f4be0b381c79061048ef8945`  
		Last Modified: Wed, 11 Jun 2025 10:56:19 GMT  
		Size: 21.4 MB (21446797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13957f45dfaafb933ab00f3283ea48d057cd2179a84687ebe45ad163f535de`  
		Last Modified: Wed, 11 Jun 2025 06:17:35 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48dd1edbbaf646c03ef3f286cc921fbc422e665578b988b9d03d890364f0d5`  
		Last Modified: Wed, 11 Jun 2025 07:14:21 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7301cbc0841ac3202a1b74a41aa6043f1d38879737a0da5c17da8e63aa32c2`  
		Last Modified: Wed, 11 Jun 2025 11:04:18 GMT  
		Size: 31.8 MB (31839063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae5612a3f46089fbce6bbf1de47ad49c5c4c6be46ad9e038f366a967187ab7`  
		Last Modified: Wed, 11 Jun 2025 11:04:10 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70afb032b9f3ac1656f5cca28aa6ec4c1623d47b8430c88d251746f6984495ae`  
		Last Modified: Wed, 11 Jun 2025 11:04:11 GMT  
		Size: 823.5 KB (823498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1267181c9b46b09997bd9cce442e3bac321de699df11a589af306e7a077084`  
		Last Modified: Wed, 11 Jun 2025 11:04:12 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f7264726be68bf863c89466f20b9622a3f4ea819a2af3233e3a056c28d822f`  
		Last Modified: Wed, 11 Jun 2025 11:04:12 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:a00f107a9222298d04a4296d68b654eda679f38487306c5030196a196197e226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63a1562e3a671aa92d1395152adb5b0079f86770497164b6b2ad4dcad16fe6e`

```dockerfile
```

-	Layers:
	-	`sha256:404683acfdb9dcf447ee6e137627e78d91adcaece87a371f891eb286377dbef3`  
		Last Modified: Wed, 11 Jun 2025 13:13:55 GMT  
		Size: 2.2 MB (2171650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4d2f8be03d02a58b777e3161bd961cf75269a73ae8d084cfabe949c7b04a3a`  
		Last Modified: Wed, 11 Jun 2025 13:13:56 GMT  
		Size: 30.4 KB (30402 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8`

```console
$ docker pull composer@sha256:eec936bdc4364a9f3f5984ef8764f10f67a5c4ffb127ac7d151d651b3611b4a8
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
$ docker pull composer@sha256:018ee8a1b80d8a42a6db5059b17b32009f0520248d4ca4ac5cea362650b0e452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76805423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89499392c7c0f772f148806eeb7d8177e801124b561c04da6d3515c0dd28ac9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41ed00f4f69f9b33b5e886fedfa6143b6e95cd34c48de5a67dfca449d27075`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 3.5 MB (3468342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3dd3a928e1a1d32cf4174792bbec9d7d27add5d439d1765653b7fc22f66b92`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0721ec88e7a2844011b208a2272d18e4e309abd51c06c8e85a7fd685455524c`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f084ac2a53f05708a861a663438bea25fa87e41a10129b5c0a01e67aed1432c`  
		Last Modified: Wed, 11 Jun 2025 01:13:20 GMT  
		Size: 13.6 MB (13640521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87939f6f4e61218155cd7a88d809fc899e6d6a2b413033839baacad75def377a`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07468323dd1f0b8efa9f6be2eaf69811d60fee46c187e62fc1b05bd2bd100fa`  
		Last Modified: Wed, 11 Jun 2025 01:13:18 GMT  
		Size: 21.0 MB (20969804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d64e952347861cf8f1c360fcf1984249571751d095594a156d453d4cb4ec8b`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f854fc0d234074345274bcbda7bb11f7295b4bae6d7d400dcbe3bd892683a59`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7aa3b0bb08cff094c890c8f9bd94d1242d8e4eecc66695b56cf0b71486bfdd`  
		Last Modified: Wed, 11 Jun 2025 01:14:39 GMT  
		Size: 33.9 MB (33928445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4004cd9be3af376ad1def28d7db8a22858965bcd6aabcb6389c7b356e3975`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275f621c47ad6f7e352d718837b79434a5bf362a7338d9131c9708977015fad3`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 976.4 KB (976410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8d98e8d78d1f43122ec0387f46a806641cb2d802951aa0ffecee3114bacc7d`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac122cbf35bfacbe46e1db0cf0b0e168d63b2f524e502932abd69bae48da849`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:e3c78b7bbcaa7aea33836758c8b9297dc69e88ada9dcf94a219e83a015c48eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3f6a2abbcf87370cfc2126f9525aa69638db268a01997e2937720170aac18a`

```dockerfile
```

-	Layers:
	-	`sha256:a4349da333f6fb53bdfe252104e833e07a89b4bec877467a87db370af1fd23ad`  
		Last Modified: Wed, 11 Jun 2025 04:13:49 GMT  
		Size: 2.2 MB (2175332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0ff13651ccad2a566eb25c6f530e75b55bdc5271773b6597b1742a8794872b`  
		Last Modified: Wed, 11 Jun 2025 04:13:49 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:cabd4f8b3fa60afcf17a1d2f439a04f5b18930b89f774227d79c7ec0e5196bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74474043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e33ae9428155f4f4eed862cc84c35990e94b325d9eac5bd6852b530e3468672`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d738e6a7e1662efb7b90b7f0a4b2cce2f9247f395ab8c1924148a0d2dde272c3`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 13.6 MB (13640499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeec31f51dc18a99c6251ab6abd48a6b17b9bd04c498ca1ce606fbe0119a506`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a9bea01d63368fc6a169811ad55c9f7baf8d06c4a3c909bea5606bf5d161c`  
		Last Modified: Tue, 10 Jun 2025 23:54:15 GMT  
		Size: 19.1 MB (19091501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab1a6cbed4c7bce681ea2c1ba6335b04364d328abb8504ac38b7cb01546c1e`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7ac6548196a7241e2ff5aeb2ebaa92bd912151a57decbc09707501826e55d`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 20.0 KB (19986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a52088bfe28e3394348499664afc0150422c289f500eeb5736a846fb654a75`  
		Last Modified: Wed, 11 Jun 2025 01:34:01 GMT  
		Size: 33.8 MB (33807058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfadb48984526f1d970423f530584b05a533cf586b26af60f4077fe0d75af65`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6d0b23171c56910ae6db9d8b6fbf79c0503339a96ab31fc527f9a6092cfad8`  
		Last Modified: Wed, 11 Jun 2025 01:46:48 GMT  
		Size: 976.8 KB (976760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1af69bdf34fca59d7eb30b0f9edddd220ae82577ff30612722efcaccd1b88b0`  
		Last Modified: Fri, 06 Jun 2025 18:42:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0441808df82eb88aa8599d9a72092fed54d4074aa052e4fe1aa44d650d466752`  
		Last Modified: Wed, 11 Jun 2025 01:46:54 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:4ae2055f652cf96d80673ff0c82c642b9fe193093bbadeed702a46c8c7abc211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f498a213c449143c593b740936c06c1a30c28c0d681279674dfc37963deaf3bc`

```dockerfile
```

-	Layers:
	-	`sha256:edcb3fe774625cf135154b452fccdedc661e27ac48b3ef0c34f6210991443adf`  
		Last Modified: Wed, 11 Jun 2025 04:13:54 GMT  
		Size: 30.6 KB (30593 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:48e7ae6497265451eeebf1afb34eb14d45dc622a97cf0616cdbb4dfed65f4964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71235844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4d4c70ce2e197972a272c79e1de0a223700e919ac7e20e3e042ed6af9edeb1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc30cbedbf54d9515871da07398fab0a70176613fac2230d3b598dd61f7dea64`  
		Last Modified: Wed, 11 Jun 2025 11:39:15 GMT  
		Size: 13.6 MB (13640514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ce30718845b98da85d3f2d4b2a979b2c4c9a318019ee4c5a3897dbb7a35b7`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788f675ffad6ad044155d5d8863ebb06f9142fe48298e02c274f65b961260418`  
		Last Modified: Wed, 11 Jun 2025 11:39:16 GMT  
		Size: 18.1 MB (18066806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2746b1c3debbab52b7827813726cffe0c2a6316b37ceefd0c7c7085cb9219577`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60271e3bc7668883349e90adf3ad21e0a859246f2f3d1430bd66ba8532b8cc1`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 20.0 KB (19984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bab94d85f8d4b9a1b97076f46ba751dc69827e8eaeb013290df1d46760098`  
		Last Modified: Wed, 11 Jun 2025 19:24:25 GMT  
		Size: 32.1 MB (32069944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d696523fff13201849f3282a4e284e28727f89ba185ff8bdb03a58fc314ccb55`  
		Last Modified: Wed, 11 Jun 2025 18:47:28 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1819f872292f162c5379693691995426aacfa08ced25e4fd27a7ef43bb70147e`  
		Last Modified: Wed, 11 Jun 2025 18:21:50 GMT  
		Size: 967.1 KB (967091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c70e26991c83798cff0473fb35dff58387d2282ab12408ad15c3d469049331`  
		Last Modified: Wed, 11 Jun 2025 18:21:50 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9619b4783886f7500963c4f9dda9a0b1ef6d8d2901a870df7fcf054f2977af9`  
		Last Modified: Wed, 11 Jun 2025 18:21:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:94b06f9d43410646d3710eebd61f14bfaa661a19b74568998125cd7805f89ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd587ba7c7d03810b426db14935e43d11776b7b25b4fb5bc04ca10a7d2aa98`

```dockerfile
```

-	Layers:
	-	`sha256:6a6062bb951a633715a67b8f08256496b7c24f71c8f9a44aa4dd6a44816e62d7`  
		Last Modified: Wed, 11 Jun 2025 19:13:41 GMT  
		Size: 2.2 MB (2175656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895f61efaeb21f18b801c568f7d0cc74cc84baf4aaef9cd4658e9b7e1f6140d0`  
		Last Modified: Wed, 11 Jun 2025 19:13:42 GMT  
		Size: 30.8 KB (30809 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:e58df78ba28a1c71954c3845a0a87bd0d0e9cc88f3e14bd3c658d0b20f6a0ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76777731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f8d65691d8f2daf38f59650b5ace82ee4a24b8238dab957493be3c7f09608c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e263556d24cfaaa81ec9153b95e1b25d54abdb35b46c3c74fa988a9f252f3`  
		Last Modified: Wed, 11 Jun 2025 09:16:54 GMT  
		Size: 3.5 MB (3470681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5bea448bb73ac691df99daf5772e7cb7307f122b4e0544c289a55be9ee24`  
		Last Modified: Wed, 11 Jun 2025 09:17:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a64acbbc8d220ea4c16baed763b26899f58299a8b85d3b8513f03b3023893`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123dcf4adf55a39c8cf4f202302f0a9dfd6d576c94bf8db94686e5a5ee1f4cf4`  
		Last Modified: Wed, 11 Jun 2025 09:33:08 GMT  
		Size: 13.6 MB (13640507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff08fc5740a571af506cddc0c38e20506f6151e574d4a10d77b748c7c3bd4b`  
		Last Modified: Wed, 11 Jun 2025 09:08:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc080435edc41cfa70a84f9586ffca3f880a9b4cedccc53c481889b18e1e1c2`  
		Last Modified: Wed, 11 Jun 2025 09:33:10 GMT  
		Size: 20.5 MB (20518887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3995038baa7f047e93509966aa2798fbc7bddf48517c43343b9add69edd5df`  
		Last Modified: Wed, 11 Jun 2025 09:08:59 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae69002966a0d0881786cca5d1dfa7b1fb54c0e7b1e4b6bf9c41f92f6208ec`  
		Last Modified: Wed, 11 Jun 2025 09:17:23 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5db0ec87df386dd8e7ed3e3a943ff4f92de4b419fe7f9bb1b4051dd24a6721`  
		Last Modified: Wed, 11 Jun 2025 15:13:38 GMT  
		Size: 34.0 MB (34010836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae1182fb6a9705ef49f6995317dfcfc6ef3d4b2292bc160d0ba7f8c246dda2e`  
		Last Modified: Wed, 11 Jun 2025 15:13:33 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797f0b16aefb6bb6a7d6af6400cee5b8275b81be5a286e77b19b60bb7069ccb`  
		Last Modified: Wed, 11 Jun 2025 16:14:10 GMT  
		Size: 976.0 KB (976036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb78c70c901a5531ae4ae81501f0dbcae57add862161bc2d6d794228ec77479b`  
		Last Modified: Wed, 11 Jun 2025 15:15:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecc1e772b20c5a6d138ed8532d8899007acf289e3afcc409f9f2dd7b823a3a`  
		Last Modified: Wed, 11 Jun 2025 16:14:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:bf2265f44da3580d35ee4c2c278cefbf8b84fe72cb09fc00c35769f60d2befe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb3cfb1574adf3b66d7d63eaea712bfe54b3ed449c5a4f7d725c6aac9c62637`

```dockerfile
```

-	Layers:
	-	`sha256:c1c94bc49ec527aeadb9fd32cc4e4d6c71f92ccc6bf8378d9e5605b406dea882`  
		Last Modified: Wed, 11 Jun 2025 16:14:27 GMT  
		Size: 2.2 MB (2175484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:160a3cc68b0b43e857b6a305bb01a248206c40228e2706205e52cc4f13d27827`  
		Last Modified: Wed, 11 Jun 2025 16:14:28 GMT  
		Size: 30.8 KB (30841 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; 386

```console
$ docker pull composer@sha256:750071636b642978927235b533d02d608b033945c5033962df7051345c6e71f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77728785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d8f82a6bc78d1d8cafba2f7b0419bf619047ac664f19abd2484cb15db3d62a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298f020aec5b2eb58f3f5d72ed081bd6c76a95799b7e438e4f3384447e42693d`  
		Last Modified: Wed, 11 Jun 2025 01:13:13 GMT  
		Size: 3.5 MB (3527774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ebeb8397f1f59382fb3bd2f49e7ae5aa3c63f7a6f5adde3d5af0fe196ad48`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c3fa431069cd36b1283a6dd73ec3c559701f45df22999775e61dd0dd4d578`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7db0fb8a413bd77d83d365246beba56a6d3ab745a296bb3119dd1c4844e7e2`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 13.6 MB (13640494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c81720a5bbf56ccfa06979187dbca8afa1859fb3d323625fe188373b9a06ed`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8fb25f24bc12988d302f27fbc0c27090c75c814e4f8dcb4396e125eafae7cb`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 21.5 MB (21493036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b67d63641d3800bf94c0e5eb453a80e9e00ec38acbc41e8b2dbe883e470dd6d`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821e028fb8ab3dacea139b63763d5d53b2d0981367d47fcd3f94182a0a2ac456`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 20.2 KB (20182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1119f1ba214f23f34c82cc094cd0e38eb36a07f01af7a3a2c1c889ee61a77db3`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 34.4 MB (34436698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e31d6c9586eea6c3de20adb86bf981bec9980b3172386076809f101620c92a`  
		Last Modified: Wed, 11 Jun 2025 01:14:21 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c939d938a848601c211ad3b2c18ae5a586f353150d3c2da6e15d0e16b07b3c32`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 989.7 KB (989719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3eff2062ef4c05ca74719dbdada1fc575f4ac3c462dc93f769ec0616dcd340a`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641cbabe81032e6beede3a4dc850d1fc1e44443f97c49a628393301c1f428062`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:7d715ef7738b0addf94a6781ff48dd6078ae85b0d26bb40e418fee4ee6627d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ad46144f5e50e5457bb9e9f8a06ba8c4851e3779a2576ec37d2a824736899e`

```dockerfile
```

-	Layers:
	-	`sha256:dedc8c889585c446bbb163d8a5210d74c241aa533895ab3cdc6bd610464d0580`  
		Last Modified: Wed, 11 Jun 2025 04:14:03 GMT  
		Size: 2.2 MB (2175115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63769367fa7293dabf75d47f54c596d481a9f54afae2ca939ff141f974997deb`  
		Last Modified: Wed, 11 Jun 2025 04:14:04 GMT  
		Size: 30.7 KB (30671 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; ppc64le

```console
$ docker pull composer@sha256:1fd39a59baae0a3da27befe8bbadd4914f23443cbc9b4159fd5ce829359875b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79150787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d400cc0b9a64ff3231bde898eadea11b3ce8dd9a1c531a8bd2f31230edd3dd94`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeaaf729ae44f9ac3f9b3f4551595556a417993152b53954f6f6a89f90a4954`  
		Last Modified: Wed, 11 Jun 2025 09:12:57 GMT  
		Size: 13.6 MB (13640505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928f2bed6e9375b5161e1fcbc32d598a194fc67da4a537c5d6a3aaab21aa3d0`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f75742ee54512415191653f6d3e2b7b2a4ff66bc4dcc60a24c12d00a0db76`  
		Last Modified: Wed, 11 Jun 2025 09:12:58 GMT  
		Size: 21.9 MB (21874047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189ddb23dd34f7e52d4b584e89ed11029f27d1dee76f138e62d772e61c75c0b6`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c88f7798e99a903cbf372177b9f7b8f2c70690f8dac0d589ec956038b045f`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a315ceb76a2ac2dda2c8bd167ee4d021a2f0885e86b42406a0c9eb02fb75b9e`  
		Last Modified: Wed, 11 Jun 2025 19:17:11 GMT  
		Size: 35.3 MB (35278992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197c9bbd782fcb082df2515b2222b6e5b48b183fca060886fc83d969d7daf6a`  
		Last Modified: Wed, 11 Jun 2025 19:17:08 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8e973c99bbdd714f82e6ab04b25a7dcef834cd2d7bbb384a34f1c65a900780`  
		Last Modified: Wed, 11 Jun 2025 19:18:36 GMT  
		Size: 983.1 KB (983051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a391ffa32455d41b4896457555da8b12cb549ec69ec4c078c83aed5823bc98cb`  
		Last Modified: Wed, 11 Jun 2025 19:18:36 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8229b8e376ebcbfbbfcf1c18e022a5c236be96f045dd864dea42549f79848976`  
		Last Modified: Wed, 11 Jun 2025 19:18:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:78143bd363e9e068532e34388330ac247f22cee1de541766d34a94b1e9427b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a231199ec7a4eb832715c76662085ff303c353d133f8ca2aef387491d0d58281`

```dockerfile
```

-	Layers:
	-	`sha256:f11d69a5442a1a8dab33f2a614e72c72fc13dd8bb29efbb534497f6d84ec21f2`  
		Last Modified: Wed, 11 Jun 2025 22:13:45 GMT  
		Size: 2.2 MB (2173895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f24043697a6971ebf4ad46f5f85045dbf9bd92262b3e3e81b15d8b2cb68270f`  
		Last Modified: Wed, 11 Jun 2025 22:13:46 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; riscv64

```console
$ docker pull composer@sha256:095cf4a1a75e00a43f5e7312124aca62aba0904617cd7ed2fd1a3391b5eb9946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73253045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43eaf5201b1e5bf4f61358597bacf05cd564df9f76e290fef6c22d6a4c2d8fdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba389b9b1d6d27f7a263c92d52685675ded66f85f52a097bec1b658400eebc5`  
		Last Modified: Wed, 11 Jun 2025 02:39:58 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb4f8cea261544e7d849e5aa9581396ef8d4bd1b7c14ceb536acc047c9ff257`  
		Last Modified: Wed, 11 Jun 2025 02:40:00 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d9086703155ae9ef802a8a0d3e98de9aabdf18c7eb07d7758e92bef886259`  
		Last Modified: Wed, 11 Jun 2025 14:10:42 GMT  
		Size: 31.1 MB (31107690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b0b41c4564a3bd6fb68327d016b7b9e8acab85e9d3bf36c289ab0ca8ce1509`  
		Last Modified: Wed, 11 Jun 2025 14:10:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8c46aaff4fe26053289768a5165cca4fede2adcef172239064e710c0501d6a`  
		Last Modified: Wed, 11 Jun 2025 14:20:44 GMT  
		Size: 974.2 KB (974233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65f1c78f1dd61273b3e7fac034634cb1238a7d1363adbd117fb741a1ea095f8`  
		Last Modified: Wed, 11 Jun 2025 14:20:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781fec4df0b23993d663bf76d5c1d53827797435ab4f54367dd5645f77be1cc1`  
		Last Modified: Wed, 11 Jun 2025 14:20:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:622db2049cbf42407d2cc1d70399fde106734b5092fd3d9d5a163930104b13bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5237221f89c8021500be82942f1cf01305d44181e6aa30c8fe2a4fbbcb84694c`

```dockerfile
```

-	Layers:
	-	`sha256:40022f797a7ac516632052656e2b4741d3ce6dbac1117ea76623f1e7c87599d6`  
		Last Modified: Wed, 11 Jun 2025 16:14:36 GMT  
		Size: 2.2 MB (2172162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b53e4a9418a6015beae947fe3ac8fbd8d384abb338aa90b797e82fbd8dc846f`  
		Last Modified: Wed, 11 Jun 2025 16:14:37 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; s390x

```console
$ docker pull composer@sha256:7d27600ab67cfc6c40ea5fd1af1ea73dded84af12bb5e5b1a9118da4369fb824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75277343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd39398b87aa3b3309d23d5fd809f569f2a0aff333203baa1ef91633f510cf12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035d42a37d5be6b1617300170ead6ce8970a5e2e4154fe287efc8af1e2f7441`  
		Last Modified: Wed, 11 Jun 2025 08:13:18 GMT  
		Size: 13.6 MB (13640519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca62563344c489947dce07a51fbce42cb5c2f338f525f3dc64a869bb23eea05`  
		Last Modified: Wed, 11 Jun 2025 06:17:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12b2d32a5b3932415a1a3b75f1dce848914c79f4be0b381c79061048ef8945`  
		Last Modified: Wed, 11 Jun 2025 10:56:19 GMT  
		Size: 21.4 MB (21446797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13957f45dfaafb933ab00f3283ea48d057cd2179a84687ebe45ad163f535de`  
		Last Modified: Wed, 11 Jun 2025 06:17:35 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48dd1edbbaf646c03ef3f286cc921fbc422e665578b988b9d03d890364f0d5`  
		Last Modified: Wed, 11 Jun 2025 07:14:21 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7301cbc0841ac3202a1b74a41aa6043f1d38879737a0da5c17da8e63aa32c2`  
		Last Modified: Wed, 11 Jun 2025 11:04:18 GMT  
		Size: 31.8 MB (31839063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae5612a3f46089fbce6bbf1de47ad49c5c4c6be46ad9e038f366a967187ab7`  
		Last Modified: Wed, 11 Jun 2025 11:04:10 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36388a5f9c7916974f5cf3654e81ca2bc90cb34ffb6a658bf7d6584d7d1e5c6`  
		Last Modified: Wed, 11 Jun 2025 11:05:52 GMT  
		Size: 979.6 KB (979592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11693de6db036153784208d91f2a3ad3ababdeed6f12cb07075c734ff290b80`  
		Last Modified: Wed, 11 Jun 2025 11:05:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18732189f7f9d716f90279e3b63ead59c1bd5bf286e3d75453eb893472e7420e`  
		Last Modified: Wed, 11 Jun 2025 11:05:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:18842ac7bb6a77638947fad992e2138a19a8ea04f1cee94797521afd0865df51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6455776eabb0daabfa5ff498dc09f7041dc7823d04bed8961bcbc7ad54689dd2`

```dockerfile
```

-	Layers:
	-	`sha256:1db08bc0f34e2331cd5923ad8217fe1fece1225931e22ef20464a13a1929e974`  
		Last Modified: Wed, 11 Jun 2025 13:13:52 GMT  
		Size: 2.2 MB (2171944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7682273cff8d79d7d74b49145ecdece43133c158854bd9dd21a5030563f9afb3`  
		Last Modified: Wed, 11 Jun 2025 13:13:53 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8.9`

```console
$ docker pull composer@sha256:eec936bdc4364a9f3f5984ef8764f10f67a5c4ffb127ac7d151d651b3611b4a8
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

### `composer:2.8.9` - linux; amd64

```console
$ docker pull composer@sha256:018ee8a1b80d8a42a6db5059b17b32009f0520248d4ca4ac5cea362650b0e452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76805423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89499392c7c0f772f148806eeb7d8177e801124b561c04da6d3515c0dd28ac9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41ed00f4f69f9b33b5e886fedfa6143b6e95cd34c48de5a67dfca449d27075`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 3.5 MB (3468342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3dd3a928e1a1d32cf4174792bbec9d7d27add5d439d1765653b7fc22f66b92`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0721ec88e7a2844011b208a2272d18e4e309abd51c06c8e85a7fd685455524c`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f084ac2a53f05708a861a663438bea25fa87e41a10129b5c0a01e67aed1432c`  
		Last Modified: Wed, 11 Jun 2025 01:13:20 GMT  
		Size: 13.6 MB (13640521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87939f6f4e61218155cd7a88d809fc899e6d6a2b413033839baacad75def377a`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07468323dd1f0b8efa9f6be2eaf69811d60fee46c187e62fc1b05bd2bd100fa`  
		Last Modified: Wed, 11 Jun 2025 01:13:18 GMT  
		Size: 21.0 MB (20969804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d64e952347861cf8f1c360fcf1984249571751d095594a156d453d4cb4ec8b`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f854fc0d234074345274bcbda7bb11f7295b4bae6d7d400dcbe3bd892683a59`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7aa3b0bb08cff094c890c8f9bd94d1242d8e4eecc66695b56cf0b71486bfdd`  
		Last Modified: Wed, 11 Jun 2025 01:14:39 GMT  
		Size: 33.9 MB (33928445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4004cd9be3af376ad1def28d7db8a22858965bcd6aabcb6389c7b356e3975`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275f621c47ad6f7e352d718837b79434a5bf362a7338d9131c9708977015fad3`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 976.4 KB (976410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8d98e8d78d1f43122ec0387f46a806641cb2d802951aa0ffecee3114bacc7d`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac122cbf35bfacbe46e1db0cf0b0e168d63b2f524e502932abd69bae48da849`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:e3c78b7bbcaa7aea33836758c8b9297dc69e88ada9dcf94a219e83a015c48eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3f6a2abbcf87370cfc2126f9525aa69638db268a01997e2937720170aac18a`

```dockerfile
```

-	Layers:
	-	`sha256:a4349da333f6fb53bdfe252104e833e07a89b4bec877467a87db370af1fd23ad`  
		Last Modified: Wed, 11 Jun 2025 04:13:49 GMT  
		Size: 2.2 MB (2175332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0ff13651ccad2a566eb25c6f530e75b55bdc5271773b6597b1742a8794872b`  
		Last Modified: Wed, 11 Jun 2025 04:13:49 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.9` - linux; arm variant v6

```console
$ docker pull composer@sha256:cabd4f8b3fa60afcf17a1d2f439a04f5b18930b89f774227d79c7ec0e5196bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74474043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e33ae9428155f4f4eed862cc84c35990e94b325d9eac5bd6852b530e3468672`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d738e6a7e1662efb7b90b7f0a4b2cce2f9247f395ab8c1924148a0d2dde272c3`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 13.6 MB (13640499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeec31f51dc18a99c6251ab6abd48a6b17b9bd04c498ca1ce606fbe0119a506`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a9bea01d63368fc6a169811ad55c9f7baf8d06c4a3c909bea5606bf5d161c`  
		Last Modified: Tue, 10 Jun 2025 23:54:15 GMT  
		Size: 19.1 MB (19091501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab1a6cbed4c7bce681ea2c1ba6335b04364d328abb8504ac38b7cb01546c1e`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7ac6548196a7241e2ff5aeb2ebaa92bd912151a57decbc09707501826e55d`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 20.0 KB (19986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a52088bfe28e3394348499664afc0150422c289f500eeb5736a846fb654a75`  
		Last Modified: Wed, 11 Jun 2025 01:34:01 GMT  
		Size: 33.8 MB (33807058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfadb48984526f1d970423f530584b05a533cf586b26af60f4077fe0d75af65`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6d0b23171c56910ae6db9d8b6fbf79c0503339a96ab31fc527f9a6092cfad8`  
		Last Modified: Wed, 11 Jun 2025 01:46:48 GMT  
		Size: 976.8 KB (976760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1af69bdf34fca59d7eb30b0f9edddd220ae82577ff30612722efcaccd1b88b0`  
		Last Modified: Fri, 06 Jun 2025 18:42:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0441808df82eb88aa8599d9a72092fed54d4074aa052e4fe1aa44d650d466752`  
		Last Modified: Wed, 11 Jun 2025 01:46:54 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:4ae2055f652cf96d80673ff0c82c642b9fe193093bbadeed702a46c8c7abc211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f498a213c449143c593b740936c06c1a30c28c0d681279674dfc37963deaf3bc`

```dockerfile
```

-	Layers:
	-	`sha256:edcb3fe774625cf135154b452fccdedc661e27ac48b3ef0c34f6210991443adf`  
		Last Modified: Wed, 11 Jun 2025 04:13:54 GMT  
		Size: 30.6 KB (30593 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.9` - linux; arm variant v7

```console
$ docker pull composer@sha256:48e7ae6497265451eeebf1afb34eb14d45dc622a97cf0616cdbb4dfed65f4964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71235844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4d4c70ce2e197972a272c79e1de0a223700e919ac7e20e3e042ed6af9edeb1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc30cbedbf54d9515871da07398fab0a70176613fac2230d3b598dd61f7dea64`  
		Last Modified: Wed, 11 Jun 2025 11:39:15 GMT  
		Size: 13.6 MB (13640514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ce30718845b98da85d3f2d4b2a979b2c4c9a318019ee4c5a3897dbb7a35b7`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788f675ffad6ad044155d5d8863ebb06f9142fe48298e02c274f65b961260418`  
		Last Modified: Wed, 11 Jun 2025 11:39:16 GMT  
		Size: 18.1 MB (18066806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2746b1c3debbab52b7827813726cffe0c2a6316b37ceefd0c7c7085cb9219577`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60271e3bc7668883349e90adf3ad21e0a859246f2f3d1430bd66ba8532b8cc1`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 20.0 KB (19984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bab94d85f8d4b9a1b97076f46ba751dc69827e8eaeb013290df1d46760098`  
		Last Modified: Wed, 11 Jun 2025 19:24:25 GMT  
		Size: 32.1 MB (32069944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d696523fff13201849f3282a4e284e28727f89ba185ff8bdb03a58fc314ccb55`  
		Last Modified: Wed, 11 Jun 2025 18:47:28 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1819f872292f162c5379693691995426aacfa08ced25e4fd27a7ef43bb70147e`  
		Last Modified: Wed, 11 Jun 2025 18:21:50 GMT  
		Size: 967.1 KB (967091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c70e26991c83798cff0473fb35dff58387d2282ab12408ad15c3d469049331`  
		Last Modified: Wed, 11 Jun 2025 18:21:50 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9619b4783886f7500963c4f9dda9a0b1ef6d8d2901a870df7fcf054f2977af9`  
		Last Modified: Wed, 11 Jun 2025 18:21:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:94b06f9d43410646d3710eebd61f14bfaa661a19b74568998125cd7805f89ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd587ba7c7d03810b426db14935e43d11776b7b25b4fb5bc04ca10a7d2aa98`

```dockerfile
```

-	Layers:
	-	`sha256:6a6062bb951a633715a67b8f08256496b7c24f71c8f9a44aa4dd6a44816e62d7`  
		Last Modified: Wed, 11 Jun 2025 19:13:41 GMT  
		Size: 2.2 MB (2175656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895f61efaeb21f18b801c568f7d0cc74cc84baf4aaef9cd4658e9b7e1f6140d0`  
		Last Modified: Wed, 11 Jun 2025 19:13:42 GMT  
		Size: 30.8 KB (30809 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.9` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:e58df78ba28a1c71954c3845a0a87bd0d0e9cc88f3e14bd3c658d0b20f6a0ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76777731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f8d65691d8f2daf38f59650b5ace82ee4a24b8238dab957493be3c7f09608c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e263556d24cfaaa81ec9153b95e1b25d54abdb35b46c3c74fa988a9f252f3`  
		Last Modified: Wed, 11 Jun 2025 09:16:54 GMT  
		Size: 3.5 MB (3470681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5bea448bb73ac691df99daf5772e7cb7307f122b4e0544c289a55be9ee24`  
		Last Modified: Wed, 11 Jun 2025 09:17:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a64acbbc8d220ea4c16baed763b26899f58299a8b85d3b8513f03b3023893`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123dcf4adf55a39c8cf4f202302f0a9dfd6d576c94bf8db94686e5a5ee1f4cf4`  
		Last Modified: Wed, 11 Jun 2025 09:33:08 GMT  
		Size: 13.6 MB (13640507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff08fc5740a571af506cddc0c38e20506f6151e574d4a10d77b748c7c3bd4b`  
		Last Modified: Wed, 11 Jun 2025 09:08:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc080435edc41cfa70a84f9586ffca3f880a9b4cedccc53c481889b18e1e1c2`  
		Last Modified: Wed, 11 Jun 2025 09:33:10 GMT  
		Size: 20.5 MB (20518887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3995038baa7f047e93509966aa2798fbc7bddf48517c43343b9add69edd5df`  
		Last Modified: Wed, 11 Jun 2025 09:08:59 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae69002966a0d0881786cca5d1dfa7b1fb54c0e7b1e4b6bf9c41f92f6208ec`  
		Last Modified: Wed, 11 Jun 2025 09:17:23 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5db0ec87df386dd8e7ed3e3a943ff4f92de4b419fe7f9bb1b4051dd24a6721`  
		Last Modified: Wed, 11 Jun 2025 15:13:38 GMT  
		Size: 34.0 MB (34010836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae1182fb6a9705ef49f6995317dfcfc6ef3d4b2292bc160d0ba7f8c246dda2e`  
		Last Modified: Wed, 11 Jun 2025 15:13:33 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797f0b16aefb6bb6a7d6af6400cee5b8275b81be5a286e77b19b60bb7069ccb`  
		Last Modified: Wed, 11 Jun 2025 16:14:10 GMT  
		Size: 976.0 KB (976036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb78c70c901a5531ae4ae81501f0dbcae57add862161bc2d6d794228ec77479b`  
		Last Modified: Wed, 11 Jun 2025 15:15:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecc1e772b20c5a6d138ed8532d8899007acf289e3afcc409f9f2dd7b823a3a`  
		Last Modified: Wed, 11 Jun 2025 16:14:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:bf2265f44da3580d35ee4c2c278cefbf8b84fe72cb09fc00c35769f60d2befe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb3cfb1574adf3b66d7d63eaea712bfe54b3ed449c5a4f7d725c6aac9c62637`

```dockerfile
```

-	Layers:
	-	`sha256:c1c94bc49ec527aeadb9fd32cc4e4d6c71f92ccc6bf8378d9e5605b406dea882`  
		Last Modified: Wed, 11 Jun 2025 16:14:27 GMT  
		Size: 2.2 MB (2175484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:160a3cc68b0b43e857b6a305bb01a248206c40228e2706205e52cc4f13d27827`  
		Last Modified: Wed, 11 Jun 2025 16:14:28 GMT  
		Size: 30.8 KB (30841 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.9` - linux; 386

```console
$ docker pull composer@sha256:750071636b642978927235b533d02d608b033945c5033962df7051345c6e71f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77728785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d8f82a6bc78d1d8cafba2f7b0419bf619047ac664f19abd2484cb15db3d62a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298f020aec5b2eb58f3f5d72ed081bd6c76a95799b7e438e4f3384447e42693d`  
		Last Modified: Wed, 11 Jun 2025 01:13:13 GMT  
		Size: 3.5 MB (3527774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ebeb8397f1f59382fb3bd2f49e7ae5aa3c63f7a6f5adde3d5af0fe196ad48`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c3fa431069cd36b1283a6dd73ec3c559701f45df22999775e61dd0dd4d578`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7db0fb8a413bd77d83d365246beba56a6d3ab745a296bb3119dd1c4844e7e2`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 13.6 MB (13640494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c81720a5bbf56ccfa06979187dbca8afa1859fb3d323625fe188373b9a06ed`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8fb25f24bc12988d302f27fbc0c27090c75c814e4f8dcb4396e125eafae7cb`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 21.5 MB (21493036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b67d63641d3800bf94c0e5eb453a80e9e00ec38acbc41e8b2dbe883e470dd6d`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821e028fb8ab3dacea139b63763d5d53b2d0981367d47fcd3f94182a0a2ac456`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 20.2 KB (20182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1119f1ba214f23f34c82cc094cd0e38eb36a07f01af7a3a2c1c889ee61a77db3`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 34.4 MB (34436698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e31d6c9586eea6c3de20adb86bf981bec9980b3172386076809f101620c92a`  
		Last Modified: Wed, 11 Jun 2025 01:14:21 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c939d938a848601c211ad3b2c18ae5a586f353150d3c2da6e15d0e16b07b3c32`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 989.7 KB (989719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3eff2062ef4c05ca74719dbdada1fc575f4ac3c462dc93f769ec0616dcd340a`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641cbabe81032e6beede3a4dc850d1fc1e44443f97c49a628393301c1f428062`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:7d715ef7738b0addf94a6781ff48dd6078ae85b0d26bb40e418fee4ee6627d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ad46144f5e50e5457bb9e9f8a06ba8c4851e3779a2576ec37d2a824736899e`

```dockerfile
```

-	Layers:
	-	`sha256:dedc8c889585c446bbb163d8a5210d74c241aa533895ab3cdc6bd610464d0580`  
		Last Modified: Wed, 11 Jun 2025 04:14:03 GMT  
		Size: 2.2 MB (2175115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63769367fa7293dabf75d47f54c596d481a9f54afae2ca939ff141f974997deb`  
		Last Modified: Wed, 11 Jun 2025 04:14:04 GMT  
		Size: 30.7 KB (30671 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.9` - linux; ppc64le

```console
$ docker pull composer@sha256:1fd39a59baae0a3da27befe8bbadd4914f23443cbc9b4159fd5ce829359875b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79150787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d400cc0b9a64ff3231bde898eadea11b3ce8dd9a1c531a8bd2f31230edd3dd94`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeaaf729ae44f9ac3f9b3f4551595556a417993152b53954f6f6a89f90a4954`  
		Last Modified: Wed, 11 Jun 2025 09:12:57 GMT  
		Size: 13.6 MB (13640505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928f2bed6e9375b5161e1fcbc32d598a194fc67da4a537c5d6a3aaab21aa3d0`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f75742ee54512415191653f6d3e2b7b2a4ff66bc4dcc60a24c12d00a0db76`  
		Last Modified: Wed, 11 Jun 2025 09:12:58 GMT  
		Size: 21.9 MB (21874047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189ddb23dd34f7e52d4b584e89ed11029f27d1dee76f138e62d772e61c75c0b6`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c88f7798e99a903cbf372177b9f7b8f2c70690f8dac0d589ec956038b045f`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a315ceb76a2ac2dda2c8bd167ee4d021a2f0885e86b42406a0c9eb02fb75b9e`  
		Last Modified: Wed, 11 Jun 2025 19:17:11 GMT  
		Size: 35.3 MB (35278992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197c9bbd782fcb082df2515b2222b6e5b48b183fca060886fc83d969d7daf6a`  
		Last Modified: Wed, 11 Jun 2025 19:17:08 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8e973c99bbdd714f82e6ab04b25a7dcef834cd2d7bbb384a34f1c65a900780`  
		Last Modified: Wed, 11 Jun 2025 19:18:36 GMT  
		Size: 983.1 KB (983051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a391ffa32455d41b4896457555da8b12cb549ec69ec4c078c83aed5823bc98cb`  
		Last Modified: Wed, 11 Jun 2025 19:18:36 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8229b8e376ebcbfbbfcf1c18e022a5c236be96f045dd864dea42549f79848976`  
		Last Modified: Wed, 11 Jun 2025 19:18:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:78143bd363e9e068532e34388330ac247f22cee1de541766d34a94b1e9427b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a231199ec7a4eb832715c76662085ff303c353d133f8ca2aef387491d0d58281`

```dockerfile
```

-	Layers:
	-	`sha256:f11d69a5442a1a8dab33f2a614e72c72fc13dd8bb29efbb534497f6d84ec21f2`  
		Last Modified: Wed, 11 Jun 2025 22:13:45 GMT  
		Size: 2.2 MB (2173895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f24043697a6971ebf4ad46f5f85045dbf9bd92262b3e3e81b15d8b2cb68270f`  
		Last Modified: Wed, 11 Jun 2025 22:13:46 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.9` - linux; riscv64

```console
$ docker pull composer@sha256:095cf4a1a75e00a43f5e7312124aca62aba0904617cd7ed2fd1a3391b5eb9946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73253045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43eaf5201b1e5bf4f61358597bacf05cd564df9f76e290fef6c22d6a4c2d8fdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba389b9b1d6d27f7a263c92d52685675ded66f85f52a097bec1b658400eebc5`  
		Last Modified: Wed, 11 Jun 2025 02:39:58 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb4f8cea261544e7d849e5aa9581396ef8d4bd1b7c14ceb536acc047c9ff257`  
		Last Modified: Wed, 11 Jun 2025 02:40:00 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d9086703155ae9ef802a8a0d3e98de9aabdf18c7eb07d7758e92bef886259`  
		Last Modified: Wed, 11 Jun 2025 14:10:42 GMT  
		Size: 31.1 MB (31107690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b0b41c4564a3bd6fb68327d016b7b9e8acab85e9d3bf36c289ab0ca8ce1509`  
		Last Modified: Wed, 11 Jun 2025 14:10:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8c46aaff4fe26053289768a5165cca4fede2adcef172239064e710c0501d6a`  
		Last Modified: Wed, 11 Jun 2025 14:20:44 GMT  
		Size: 974.2 KB (974233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65f1c78f1dd61273b3e7fac034634cb1238a7d1363adbd117fb741a1ea095f8`  
		Last Modified: Wed, 11 Jun 2025 14:20:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781fec4df0b23993d663bf76d5c1d53827797435ab4f54367dd5645f77be1cc1`  
		Last Modified: Wed, 11 Jun 2025 14:20:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:622db2049cbf42407d2cc1d70399fde106734b5092fd3d9d5a163930104b13bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5237221f89c8021500be82942f1cf01305d44181e6aa30c8fe2a4fbbcb84694c`

```dockerfile
```

-	Layers:
	-	`sha256:40022f797a7ac516632052656e2b4741d3ce6dbac1117ea76623f1e7c87599d6`  
		Last Modified: Wed, 11 Jun 2025 16:14:36 GMT  
		Size: 2.2 MB (2172162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b53e4a9418a6015beae947fe3ac8fbd8d384abb338aa90b797e82fbd8dc846f`  
		Last Modified: Wed, 11 Jun 2025 16:14:37 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.9` - linux; s390x

```console
$ docker pull composer@sha256:7d27600ab67cfc6c40ea5fd1af1ea73dded84af12bb5e5b1a9118da4369fb824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75277343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd39398b87aa3b3309d23d5fd809f569f2a0aff333203baa1ef91633f510cf12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035d42a37d5be6b1617300170ead6ce8970a5e2e4154fe287efc8af1e2f7441`  
		Last Modified: Wed, 11 Jun 2025 08:13:18 GMT  
		Size: 13.6 MB (13640519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca62563344c489947dce07a51fbce42cb5c2f338f525f3dc64a869bb23eea05`  
		Last Modified: Wed, 11 Jun 2025 06:17:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12b2d32a5b3932415a1a3b75f1dce848914c79f4be0b381c79061048ef8945`  
		Last Modified: Wed, 11 Jun 2025 10:56:19 GMT  
		Size: 21.4 MB (21446797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13957f45dfaafb933ab00f3283ea48d057cd2179a84687ebe45ad163f535de`  
		Last Modified: Wed, 11 Jun 2025 06:17:35 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48dd1edbbaf646c03ef3f286cc921fbc422e665578b988b9d03d890364f0d5`  
		Last Modified: Wed, 11 Jun 2025 07:14:21 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7301cbc0841ac3202a1b74a41aa6043f1d38879737a0da5c17da8e63aa32c2`  
		Last Modified: Wed, 11 Jun 2025 11:04:18 GMT  
		Size: 31.8 MB (31839063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae5612a3f46089fbce6bbf1de47ad49c5c4c6be46ad9e038f366a967187ab7`  
		Last Modified: Wed, 11 Jun 2025 11:04:10 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36388a5f9c7916974f5cf3654e81ca2bc90cb34ffb6a658bf7d6584d7d1e5c6`  
		Last Modified: Wed, 11 Jun 2025 11:05:52 GMT  
		Size: 979.6 KB (979592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11693de6db036153784208d91f2a3ad3ababdeed6f12cb07075c734ff290b80`  
		Last Modified: Wed, 11 Jun 2025 11:05:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18732189f7f9d716f90279e3b63ead59c1bd5bf286e3d75453eb893472e7420e`  
		Last Modified: Wed, 11 Jun 2025 11:05:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.9` - unknown; unknown

```console
$ docker pull composer@sha256:18842ac7bb6a77638947fad992e2138a19a8ea04f1cee94797521afd0865df51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6455776eabb0daabfa5ff498dc09f7041dc7823d04bed8961bcbc7ad54689dd2`

```dockerfile
```

-	Layers:
	-	`sha256:1db08bc0f34e2331cd5923ad8217fe1fece1225931e22ef20464a13a1929e974`  
		Last Modified: Wed, 11 Jun 2025 13:13:52 GMT  
		Size: 2.2 MB (2171944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7682273cff8d79d7d74b49145ecdece43133c158854bd9dd21a5030563f9afb3`  
		Last Modified: Wed, 11 Jun 2025 13:13:53 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:eec936bdc4364a9f3f5984ef8764f10f67a5c4ffb127ac7d151d651b3611b4a8
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
$ docker pull composer@sha256:018ee8a1b80d8a42a6db5059b17b32009f0520248d4ca4ac5cea362650b0e452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76805423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89499392c7c0f772f148806eeb7d8177e801124b561c04da6d3515c0dd28ac9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41ed00f4f69f9b33b5e886fedfa6143b6e95cd34c48de5a67dfca449d27075`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 3.5 MB (3468342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3dd3a928e1a1d32cf4174792bbec9d7d27add5d439d1765653b7fc22f66b92`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0721ec88e7a2844011b208a2272d18e4e309abd51c06c8e85a7fd685455524c`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f084ac2a53f05708a861a663438bea25fa87e41a10129b5c0a01e67aed1432c`  
		Last Modified: Wed, 11 Jun 2025 01:13:20 GMT  
		Size: 13.6 MB (13640521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87939f6f4e61218155cd7a88d809fc899e6d6a2b413033839baacad75def377a`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07468323dd1f0b8efa9f6be2eaf69811d60fee46c187e62fc1b05bd2bd100fa`  
		Last Modified: Wed, 11 Jun 2025 01:13:18 GMT  
		Size: 21.0 MB (20969804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d64e952347861cf8f1c360fcf1984249571751d095594a156d453d4cb4ec8b`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f854fc0d234074345274bcbda7bb11f7295b4bae6d7d400dcbe3bd892683a59`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7aa3b0bb08cff094c890c8f9bd94d1242d8e4eecc66695b56cf0b71486bfdd`  
		Last Modified: Wed, 11 Jun 2025 01:14:39 GMT  
		Size: 33.9 MB (33928445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4004cd9be3af376ad1def28d7db8a22858965bcd6aabcb6389c7b356e3975`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275f621c47ad6f7e352d718837b79434a5bf362a7338d9131c9708977015fad3`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 976.4 KB (976410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8d98e8d78d1f43122ec0387f46a806641cb2d802951aa0ffecee3114bacc7d`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac122cbf35bfacbe46e1db0cf0b0e168d63b2f524e502932abd69bae48da849`  
		Last Modified: Wed, 11 Jun 2025 01:14:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:e3c78b7bbcaa7aea33836758c8b9297dc69e88ada9dcf94a219e83a015c48eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3f6a2abbcf87370cfc2126f9525aa69638db268a01997e2937720170aac18a`

```dockerfile
```

-	Layers:
	-	`sha256:a4349da333f6fb53bdfe252104e833e07a89b4bec877467a87db370af1fd23ad`  
		Last Modified: Wed, 11 Jun 2025 04:13:49 GMT  
		Size: 2.2 MB (2175332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0ff13651ccad2a566eb25c6f530e75b55bdc5271773b6597b1742a8794872b`  
		Last Modified: Wed, 11 Jun 2025 04:13:49 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:cabd4f8b3fa60afcf17a1d2f439a04f5b18930b89f774227d79c7ec0e5196bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74474043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e33ae9428155f4f4eed862cc84c35990e94b325d9eac5bd6852b530e3468672`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d738e6a7e1662efb7b90b7f0a4b2cce2f9247f395ab8c1924148a0d2dde272c3`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 13.6 MB (13640499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeec31f51dc18a99c6251ab6abd48a6b17b9bd04c498ca1ce606fbe0119a506`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a9bea01d63368fc6a169811ad55c9f7baf8d06c4a3c909bea5606bf5d161c`  
		Last Modified: Tue, 10 Jun 2025 23:54:15 GMT  
		Size: 19.1 MB (19091501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab1a6cbed4c7bce681ea2c1ba6335b04364d328abb8504ac38b7cb01546c1e`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7ac6548196a7241e2ff5aeb2ebaa92bd912151a57decbc09707501826e55d`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 20.0 KB (19986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a52088bfe28e3394348499664afc0150422c289f500eeb5736a846fb654a75`  
		Last Modified: Wed, 11 Jun 2025 01:34:01 GMT  
		Size: 33.8 MB (33807058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfadb48984526f1d970423f530584b05a533cf586b26af60f4077fe0d75af65`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6d0b23171c56910ae6db9d8b6fbf79c0503339a96ab31fc527f9a6092cfad8`  
		Last Modified: Wed, 11 Jun 2025 01:46:48 GMT  
		Size: 976.8 KB (976760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1af69bdf34fca59d7eb30b0f9edddd220ae82577ff30612722efcaccd1b88b0`  
		Last Modified: Fri, 06 Jun 2025 18:42:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0441808df82eb88aa8599d9a72092fed54d4074aa052e4fe1aa44d650d466752`  
		Last Modified: Wed, 11 Jun 2025 01:46:54 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:4ae2055f652cf96d80673ff0c82c642b9fe193093bbadeed702a46c8c7abc211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f498a213c449143c593b740936c06c1a30c28c0d681279674dfc37963deaf3bc`

```dockerfile
```

-	Layers:
	-	`sha256:edcb3fe774625cf135154b452fccdedc661e27ac48b3ef0c34f6210991443adf`  
		Last Modified: Wed, 11 Jun 2025 04:13:54 GMT  
		Size: 30.6 KB (30593 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:48e7ae6497265451eeebf1afb34eb14d45dc622a97cf0616cdbb4dfed65f4964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71235844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4d4c70ce2e197972a272c79e1de0a223700e919ac7e20e3e042ed6af9edeb1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc30cbedbf54d9515871da07398fab0a70176613fac2230d3b598dd61f7dea64`  
		Last Modified: Wed, 11 Jun 2025 11:39:15 GMT  
		Size: 13.6 MB (13640514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ce30718845b98da85d3f2d4b2a979b2c4c9a318019ee4c5a3897dbb7a35b7`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788f675ffad6ad044155d5d8863ebb06f9142fe48298e02c274f65b961260418`  
		Last Modified: Wed, 11 Jun 2025 11:39:16 GMT  
		Size: 18.1 MB (18066806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2746b1c3debbab52b7827813726cffe0c2a6316b37ceefd0c7c7085cb9219577`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60271e3bc7668883349e90adf3ad21e0a859246f2f3d1430bd66ba8532b8cc1`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 20.0 KB (19984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bab94d85f8d4b9a1b97076f46ba751dc69827e8eaeb013290df1d46760098`  
		Last Modified: Wed, 11 Jun 2025 19:24:25 GMT  
		Size: 32.1 MB (32069944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d696523fff13201849f3282a4e284e28727f89ba185ff8bdb03a58fc314ccb55`  
		Last Modified: Wed, 11 Jun 2025 18:47:28 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1819f872292f162c5379693691995426aacfa08ced25e4fd27a7ef43bb70147e`  
		Last Modified: Wed, 11 Jun 2025 18:21:50 GMT  
		Size: 967.1 KB (967091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c70e26991c83798cff0473fb35dff58387d2282ab12408ad15c3d469049331`  
		Last Modified: Wed, 11 Jun 2025 18:21:50 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9619b4783886f7500963c4f9dda9a0b1ef6d8d2901a870df7fcf054f2977af9`  
		Last Modified: Wed, 11 Jun 2025 18:21:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:94b06f9d43410646d3710eebd61f14bfaa661a19b74568998125cd7805f89ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd587ba7c7d03810b426db14935e43d11776b7b25b4fb5bc04ca10a7d2aa98`

```dockerfile
```

-	Layers:
	-	`sha256:6a6062bb951a633715a67b8f08256496b7c24f71c8f9a44aa4dd6a44816e62d7`  
		Last Modified: Wed, 11 Jun 2025 19:13:41 GMT  
		Size: 2.2 MB (2175656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895f61efaeb21f18b801c568f7d0cc74cc84baf4aaef9cd4658e9b7e1f6140d0`  
		Last Modified: Wed, 11 Jun 2025 19:13:42 GMT  
		Size: 30.8 KB (30809 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:e58df78ba28a1c71954c3845a0a87bd0d0e9cc88f3e14bd3c658d0b20f6a0ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76777731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f8d65691d8f2daf38f59650b5ace82ee4a24b8238dab957493be3c7f09608c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e263556d24cfaaa81ec9153b95e1b25d54abdb35b46c3c74fa988a9f252f3`  
		Last Modified: Wed, 11 Jun 2025 09:16:54 GMT  
		Size: 3.5 MB (3470681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5bea448bb73ac691df99daf5772e7cb7307f122b4e0544c289a55be9ee24`  
		Last Modified: Wed, 11 Jun 2025 09:17:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a64acbbc8d220ea4c16baed763b26899f58299a8b85d3b8513f03b3023893`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123dcf4adf55a39c8cf4f202302f0a9dfd6d576c94bf8db94686e5a5ee1f4cf4`  
		Last Modified: Wed, 11 Jun 2025 09:33:08 GMT  
		Size: 13.6 MB (13640507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff08fc5740a571af506cddc0c38e20506f6151e574d4a10d77b748c7c3bd4b`  
		Last Modified: Wed, 11 Jun 2025 09:08:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc080435edc41cfa70a84f9586ffca3f880a9b4cedccc53c481889b18e1e1c2`  
		Last Modified: Wed, 11 Jun 2025 09:33:10 GMT  
		Size: 20.5 MB (20518887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3995038baa7f047e93509966aa2798fbc7bddf48517c43343b9add69edd5df`  
		Last Modified: Wed, 11 Jun 2025 09:08:59 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae69002966a0d0881786cca5d1dfa7b1fb54c0e7b1e4b6bf9c41f92f6208ec`  
		Last Modified: Wed, 11 Jun 2025 09:17:23 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5db0ec87df386dd8e7ed3e3a943ff4f92de4b419fe7f9bb1b4051dd24a6721`  
		Last Modified: Wed, 11 Jun 2025 15:13:38 GMT  
		Size: 34.0 MB (34010836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae1182fb6a9705ef49f6995317dfcfc6ef3d4b2292bc160d0ba7f8c246dda2e`  
		Last Modified: Wed, 11 Jun 2025 15:13:33 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797f0b16aefb6bb6a7d6af6400cee5b8275b81be5a286e77b19b60bb7069ccb`  
		Last Modified: Wed, 11 Jun 2025 16:14:10 GMT  
		Size: 976.0 KB (976036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb78c70c901a5531ae4ae81501f0dbcae57add862161bc2d6d794228ec77479b`  
		Last Modified: Wed, 11 Jun 2025 15:15:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecc1e772b20c5a6d138ed8532d8899007acf289e3afcc409f9f2dd7b823a3a`  
		Last Modified: Wed, 11 Jun 2025 16:14:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:bf2265f44da3580d35ee4c2c278cefbf8b84fe72cb09fc00c35769f60d2befe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb3cfb1574adf3b66d7d63eaea712bfe54b3ed449c5a4f7d725c6aac9c62637`

```dockerfile
```

-	Layers:
	-	`sha256:c1c94bc49ec527aeadb9fd32cc4e4d6c71f92ccc6bf8378d9e5605b406dea882`  
		Last Modified: Wed, 11 Jun 2025 16:14:27 GMT  
		Size: 2.2 MB (2175484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:160a3cc68b0b43e857b6a305bb01a248206c40228e2706205e52cc4f13d27827`  
		Last Modified: Wed, 11 Jun 2025 16:14:28 GMT  
		Size: 30.8 KB (30841 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:750071636b642978927235b533d02d608b033945c5033962df7051345c6e71f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77728785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d8f82a6bc78d1d8cafba2f7b0419bf619047ac664f19abd2484cb15db3d62a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298f020aec5b2eb58f3f5d72ed081bd6c76a95799b7e438e4f3384447e42693d`  
		Last Modified: Wed, 11 Jun 2025 01:13:13 GMT  
		Size: 3.5 MB (3527774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ebeb8397f1f59382fb3bd2f49e7ae5aa3c63f7a6f5adde3d5af0fe196ad48`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c3fa431069cd36b1283a6dd73ec3c559701f45df22999775e61dd0dd4d578`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7db0fb8a413bd77d83d365246beba56a6d3ab745a296bb3119dd1c4844e7e2`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 13.6 MB (13640494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c81720a5bbf56ccfa06979187dbca8afa1859fb3d323625fe188373b9a06ed`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8fb25f24bc12988d302f27fbc0c27090c75c814e4f8dcb4396e125eafae7cb`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 21.5 MB (21493036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b67d63641d3800bf94c0e5eb453a80e9e00ec38acbc41e8b2dbe883e470dd6d`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821e028fb8ab3dacea139b63763d5d53b2d0981367d47fcd3f94182a0a2ac456`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 20.2 KB (20182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1119f1ba214f23f34c82cc094cd0e38eb36a07f01af7a3a2c1c889ee61a77db3`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 34.4 MB (34436698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e31d6c9586eea6c3de20adb86bf981bec9980b3172386076809f101620c92a`  
		Last Modified: Wed, 11 Jun 2025 01:14:21 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c939d938a848601c211ad3b2c18ae5a586f353150d3c2da6e15d0e16b07b3c32`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 989.7 KB (989719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3eff2062ef4c05ca74719dbdada1fc575f4ac3c462dc93f769ec0616dcd340a`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641cbabe81032e6beede3a4dc850d1fc1e44443f97c49a628393301c1f428062`  
		Last Modified: Wed, 11 Jun 2025 01:14:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:7d715ef7738b0addf94a6781ff48dd6078ae85b0d26bb40e418fee4ee6627d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ad46144f5e50e5457bb9e9f8a06ba8c4851e3779a2576ec37d2a824736899e`

```dockerfile
```

-	Layers:
	-	`sha256:dedc8c889585c446bbb163d8a5210d74c241aa533895ab3cdc6bd610464d0580`  
		Last Modified: Wed, 11 Jun 2025 04:14:03 GMT  
		Size: 2.2 MB (2175115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63769367fa7293dabf75d47f54c596d481a9f54afae2ca939ff141f974997deb`  
		Last Modified: Wed, 11 Jun 2025 04:14:04 GMT  
		Size: 30.7 KB (30671 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:1fd39a59baae0a3da27befe8bbadd4914f23443cbc9b4159fd5ce829359875b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79150787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d400cc0b9a64ff3231bde898eadea11b3ce8dd9a1c531a8bd2f31230edd3dd94`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeaaf729ae44f9ac3f9b3f4551595556a417993152b53954f6f6a89f90a4954`  
		Last Modified: Wed, 11 Jun 2025 09:12:57 GMT  
		Size: 13.6 MB (13640505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928f2bed6e9375b5161e1fcbc32d598a194fc67da4a537c5d6a3aaab21aa3d0`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f75742ee54512415191653f6d3e2b7b2a4ff66bc4dcc60a24c12d00a0db76`  
		Last Modified: Wed, 11 Jun 2025 09:12:58 GMT  
		Size: 21.9 MB (21874047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189ddb23dd34f7e52d4b584e89ed11029f27d1dee76f138e62d772e61c75c0b6`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c88f7798e99a903cbf372177b9f7b8f2c70690f8dac0d589ec956038b045f`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a315ceb76a2ac2dda2c8bd167ee4d021a2f0885e86b42406a0c9eb02fb75b9e`  
		Last Modified: Wed, 11 Jun 2025 19:17:11 GMT  
		Size: 35.3 MB (35278992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197c9bbd782fcb082df2515b2222b6e5b48b183fca060886fc83d969d7daf6a`  
		Last Modified: Wed, 11 Jun 2025 19:17:08 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8e973c99bbdd714f82e6ab04b25a7dcef834cd2d7bbb384a34f1c65a900780`  
		Last Modified: Wed, 11 Jun 2025 19:18:36 GMT  
		Size: 983.1 KB (983051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a391ffa32455d41b4896457555da8b12cb549ec69ec4c078c83aed5823bc98cb`  
		Last Modified: Wed, 11 Jun 2025 19:18:36 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8229b8e376ebcbfbbfcf1c18e022a5c236be96f045dd864dea42549f79848976`  
		Last Modified: Wed, 11 Jun 2025 19:18:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:78143bd363e9e068532e34388330ac247f22cee1de541766d34a94b1e9427b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a231199ec7a4eb832715c76662085ff303c353d133f8ca2aef387491d0d58281`

```dockerfile
```

-	Layers:
	-	`sha256:f11d69a5442a1a8dab33f2a614e72c72fc13dd8bb29efbb534497f6d84ec21f2`  
		Last Modified: Wed, 11 Jun 2025 22:13:45 GMT  
		Size: 2.2 MB (2173895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f24043697a6971ebf4ad46f5f85045dbf9bd92262b3e3e81b15d8b2cb68270f`  
		Last Modified: Wed, 11 Jun 2025 22:13:46 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:095cf4a1a75e00a43f5e7312124aca62aba0904617cd7ed2fd1a3391b5eb9946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73253045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43eaf5201b1e5bf4f61358597bacf05cd564df9f76e290fef6c22d6a4c2d8fdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba389b9b1d6d27f7a263c92d52685675ded66f85f52a097bec1b658400eebc5`  
		Last Modified: Wed, 11 Jun 2025 02:39:58 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb4f8cea261544e7d849e5aa9581396ef8d4bd1b7c14ceb536acc047c9ff257`  
		Last Modified: Wed, 11 Jun 2025 02:40:00 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d9086703155ae9ef802a8a0d3e98de9aabdf18c7eb07d7758e92bef886259`  
		Last Modified: Wed, 11 Jun 2025 14:10:42 GMT  
		Size: 31.1 MB (31107690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b0b41c4564a3bd6fb68327d016b7b9e8acab85e9d3bf36c289ab0ca8ce1509`  
		Last Modified: Wed, 11 Jun 2025 14:10:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8c46aaff4fe26053289768a5165cca4fede2adcef172239064e710c0501d6a`  
		Last Modified: Wed, 11 Jun 2025 14:20:44 GMT  
		Size: 974.2 KB (974233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65f1c78f1dd61273b3e7fac034634cb1238a7d1363adbd117fb741a1ea095f8`  
		Last Modified: Wed, 11 Jun 2025 14:20:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781fec4df0b23993d663bf76d5c1d53827797435ab4f54367dd5645f77be1cc1`  
		Last Modified: Wed, 11 Jun 2025 14:20:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:622db2049cbf42407d2cc1d70399fde106734b5092fd3d9d5a163930104b13bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5237221f89c8021500be82942f1cf01305d44181e6aa30c8fe2a4fbbcb84694c`

```dockerfile
```

-	Layers:
	-	`sha256:40022f797a7ac516632052656e2b4741d3ce6dbac1117ea76623f1e7c87599d6`  
		Last Modified: Wed, 11 Jun 2025 16:14:36 GMT  
		Size: 2.2 MB (2172162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b53e4a9418a6015beae947fe3ac8fbd8d384abb338aa90b797e82fbd8dc846f`  
		Last Modified: Wed, 11 Jun 2025 16:14:37 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:7d27600ab67cfc6c40ea5fd1af1ea73dded84af12bb5e5b1a9118da4369fb824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75277343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd39398b87aa3b3309d23d5fd809f569f2a0aff333203baa1ef91633f510cf12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 15 May 2025 07:05:58 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Thu, 15 May 2025 07:05:58 GMT
CMD ["/bin/sh"]
# Thu, 15 May 2025 07:05:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 May 2025 07:05:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 May 2025 07:05:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_VERSION=8.4.8
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Thu, 15 May 2025 07:05:58 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["php" "-a"]
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 15 May 2025 07:05:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 15 May 2025 07:05:58 GMT
ENV COMPOSER_VERSION=2.8.9
# Thu, 15 May 2025 07:05:58 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 15 May 2025 07:05:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 15 May 2025 07:05:58 GMT
WORKDIR /app
# Thu, 15 May 2025 07:05:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 May 2025 07:05:58 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035d42a37d5be6b1617300170ead6ce8970a5e2e4154fe287efc8af1e2f7441`  
		Last Modified: Wed, 11 Jun 2025 08:13:18 GMT  
		Size: 13.6 MB (13640519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca62563344c489947dce07a51fbce42cb5c2f338f525f3dc64a869bb23eea05`  
		Last Modified: Wed, 11 Jun 2025 06:17:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12b2d32a5b3932415a1a3b75f1dce848914c79f4be0b381c79061048ef8945`  
		Last Modified: Wed, 11 Jun 2025 10:56:19 GMT  
		Size: 21.4 MB (21446797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13957f45dfaafb933ab00f3283ea48d057cd2179a84687ebe45ad163f535de`  
		Last Modified: Wed, 11 Jun 2025 06:17:35 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48dd1edbbaf646c03ef3f286cc921fbc422e665578b988b9d03d890364f0d5`  
		Last Modified: Wed, 11 Jun 2025 07:14:21 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7301cbc0841ac3202a1b74a41aa6043f1d38879737a0da5c17da8e63aa32c2`  
		Last Modified: Wed, 11 Jun 2025 11:04:18 GMT  
		Size: 31.8 MB (31839063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae5612a3f46089fbce6bbf1de47ad49c5c4c6be46ad9e038f366a967187ab7`  
		Last Modified: Wed, 11 Jun 2025 11:04:10 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36388a5f9c7916974f5cf3654e81ca2bc90cb34ffb6a658bf7d6584d7d1e5c6`  
		Last Modified: Wed, 11 Jun 2025 11:05:52 GMT  
		Size: 979.6 KB (979592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11693de6db036153784208d91f2a3ad3ababdeed6f12cb07075c734ff290b80`  
		Last Modified: Wed, 11 Jun 2025 11:05:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18732189f7f9d716f90279e3b63ead59c1bd5bf286e3d75453eb893472e7420e`  
		Last Modified: Wed, 11 Jun 2025 11:05:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:18842ac7bb6a77638947fad992e2138a19a8ea04f1cee94797521afd0865df51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6455776eabb0daabfa5ff498dc09f7041dc7823d04bed8961bcbc7ad54689dd2`

```dockerfile
```

-	Layers:
	-	`sha256:1db08bc0f34e2331cd5923ad8217fe1fece1225931e22ef20464a13a1929e974`  
		Last Modified: Wed, 11 Jun 2025 13:13:52 GMT  
		Size: 2.2 MB (2171944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7682273cff8d79d7d74b49145ecdece43133c158854bd9dd21a5030563f9afb3`  
		Last Modified: Wed, 11 Jun 2025 13:13:53 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:lts`

```console
$ docker pull composer@sha256:d1f7d20ea14a08d37a6d5dd4293d78b68b0441737cf0cf3b4a11e9835ed3339f
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
$ docker pull composer@sha256:66c210df6092e9ffd6aae866adda031924eec1463f027158f60be5badfb77c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76649453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274e1a9f42a6603ffb572547fe9ef6f09b2df1a46588a3bd34e375789a761414`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa41ed00f4f69f9b33b5e886fedfa6143b6e95cd34c48de5a67dfca449d27075`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 3.5 MB (3468342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3dd3a928e1a1d32cf4174792bbec9d7d27add5d439d1765653b7fc22f66b92`  
		Last Modified: Wed, 11 Jun 2025 00:03:25 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0721ec88e7a2844011b208a2272d18e4e309abd51c06c8e85a7fd685455524c`  
		Last Modified: Wed, 11 Jun 2025 00:03:26 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f084ac2a53f05708a861a663438bea25fa87e41a10129b5c0a01e67aed1432c`  
		Last Modified: Wed, 11 Jun 2025 01:13:20 GMT  
		Size: 13.6 MB (13640521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87939f6f4e61218155cd7a88d809fc899e6d6a2b413033839baacad75def377a`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07468323dd1f0b8efa9f6be2eaf69811d60fee46c187e62fc1b05bd2bd100fa`  
		Last Modified: Wed, 11 Jun 2025 01:13:18 GMT  
		Size: 21.0 MB (20969804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d64e952347861cf8f1c360fcf1984249571751d095594a156d453d4cb4ec8b`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f854fc0d234074345274bcbda7bb11f7295b4bae6d7d400dcbe3bd892683a59`  
		Last Modified: Wed, 11 Jun 2025 01:13:17 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a983a9e67738612dca1d606b492e33ae4772239864276c2e9bb701fd5ebc24ab`  
		Last Modified: Wed, 11 Jun 2025 01:14:29 GMT  
		Size: 33.9 MB (33928524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4eddb6321370e9aea8f80682132fdc57b74e210ab2efcced5a16afbbea8392`  
		Last Modified: Wed, 11 Jun 2025 01:14:27 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34096107b75deddc3c26ef831ee95ec5d5d90cd5a8a06d16d820b7ccbe12cd2d`  
		Last Modified: Wed, 11 Jun 2025 01:14:28 GMT  
		Size: 820.4 KB (820361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f33c62710586fcee38c006ff77c73c8512ff387a2bc8eb5e1b023a9f98b215e`  
		Last Modified: Wed, 11 Jun 2025 01:14:27 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4c85bab44c6212eef3eeee94969b44f80db62609d8698045bc32bb1a65bb71`  
		Last Modified: Wed, 11 Jun 2025 01:14:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:512324e4110a0bf6414d38b70de4f4a7f2248ff4fc595a5812435dba49691022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04b71eda3eddc033744c6560d8f10f7b0de55b93df4439b9a5e3e1119ce00cc`

```dockerfile
```

-	Layers:
	-	`sha256:ece2f5f71f9f874c22b05c5d9b3c8ce911621f638b9f7ea92949f4763433f11d`  
		Last Modified: Wed, 11 Jun 2025 04:14:00 GMT  
		Size: 2.2 MB (2175038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4137fd02ac043dc683560f7c85ac1dbcb28e9c9f5d5a03600e90f819c0a66961`  
		Last Modified: Wed, 11 Jun 2025 04:14:01 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v6

```console
$ docker pull composer@sha256:b4aa7e8e101938a53e03775f4534ee26dcfb36f70505c18e85bf66d01f9c0ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74317808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ed425857cba64206a646cabe2f9a8d324ec0d8a820783dc4291625118e4339`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d738e6a7e1662efb7b90b7f0a4b2cce2f9247f395ab8c1924148a0d2dde272c3`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 13.6 MB (13640499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeec31f51dc18a99c6251ab6abd48a6b17b9bd04c498ca1ce606fbe0119a506`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4a9bea01d63368fc6a169811ad55c9f7baf8d06c4a3c909bea5606bf5d161c`  
		Last Modified: Tue, 10 Jun 2025 23:54:15 GMT  
		Size: 19.1 MB (19091501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab1a6cbed4c7bce681ea2c1ba6335b04364d328abb8504ac38b7cb01546c1e`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7ac6548196a7241e2ff5aeb2ebaa92bd912151a57decbc09707501826e55d`  
		Last Modified: Tue, 10 Jun 2025 23:54:13 GMT  
		Size: 20.0 KB (19986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a52088bfe28e3394348499664afc0150422c289f500eeb5736a846fb654a75`  
		Last Modified: Wed, 11 Jun 2025 01:34:01 GMT  
		Size: 33.8 MB (33807058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfadb48984526f1d970423f530584b05a533cf586b26af60f4077fe0d75af65`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07dea40c6caddf6bdae192a744e3231fdcca79d1be718ed3bef4de7f8b4fbbf`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 820.5 KB (820524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d457fcbfa723120617f86dcb4efa382bf960cdfc50ac9c337575328a956407f6`  
		Last Modified: Fri, 06 Jun 2025 18:41:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d13ade04f1c3949a7c8fad3b6d3e005313812670a868b8e35c048ff3d3e342f`  
		Last Modified: Wed, 11 Jun 2025 01:33:58 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:64cfcb2cfcd2778f1199141172672925fad657e6dac36c3ea0ca54727b3929b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a9079774811c129322fa73f782aa6eaaca32d9cf62043301abb742e7ca7d62`

```dockerfile
```

-	Layers:
	-	`sha256:7983cb32e3739991648b53a980ad98f5bb4686b536f719a02f9fad1f437649e6`  
		Last Modified: Wed, 11 Jun 2025 04:14:06 GMT  
		Size: 30.3 KB (30282 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v7

```console
$ docker pull composer@sha256:58893f135334ec29555376b95fc04c9862a2f8332e3e6c9046c5815d31d1bd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71079557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c0e947182a4e650b5bf0a550f9161cc3d2754207790a89b482c58ee5824fa0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc30cbedbf54d9515871da07398fab0a70176613fac2230d3b598dd61f7dea64`  
		Last Modified: Wed, 11 Jun 2025 11:39:15 GMT  
		Size: 13.6 MB (13640514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ce30718845b98da85d3f2d4b2a979b2c4c9a318019ee4c5a3897dbb7a35b7`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788f675ffad6ad044155d5d8863ebb06f9142fe48298e02c274f65b961260418`  
		Last Modified: Wed, 11 Jun 2025 11:39:16 GMT  
		Size: 18.1 MB (18066806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2746b1c3debbab52b7827813726cffe0c2a6316b37ceefd0c7c7085cb9219577`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60271e3bc7668883349e90adf3ad21e0a859246f2f3d1430bd66ba8532b8cc1`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 20.0 KB (19984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bab94d85f8d4b9a1b97076f46ba751dc69827e8eaeb013290df1d46760098`  
		Last Modified: Wed, 11 Jun 2025 19:24:25 GMT  
		Size: 32.1 MB (32069944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d696523fff13201849f3282a4e284e28727f89ba185ff8bdb03a58fc314ccb55`  
		Last Modified: Wed, 11 Jun 2025 18:47:28 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb0b283c0550b0d57ccd0a7a90fdd170a824a4fb688f9ca63d43272a0e4a68f`  
		Last Modified: Wed, 11 Jun 2025 18:48:14 GMT  
		Size: 810.8 KB (810804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b29f0dbbbf18851f15f6ca488e3c9c66614a80976f420f840344823dd79f56`  
		Last Modified: Wed, 11 Jun 2025 18:48:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b2d00a029d07cf1009735df624fd16018bc88ec70ce9902ae0b13184835d1d`  
		Last Modified: Wed, 11 Jun 2025 18:48:20 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:7e8eab146f11f853085da9ff953ff9d4ab3c78ddd7288b0bbce287f7428ec379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439f87fb6a2364d089c9a12622c33e05239477d5c171d1b96ff897b3934588ef`

```dockerfile
```

-	Layers:
	-	`sha256:b49cc057be66bf6aa815e35859c7c7ee91dd72e94920c37a7e49c6d4ed1a8f84`  
		Last Modified: Wed, 11 Jun 2025 19:13:49 GMT  
		Size: 2.2 MB (2175354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cca50545151f25b54270eadf543a8ff4824180bb0dfeb6e1051852dc1a3467c`  
		Last Modified: Wed, 11 Jun 2025 19:13:50 GMT  
		Size: 30.5 KB (30497 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:9044a7410ca203d0a6900fe8157d8b61b4689354676c576c59c2ca5d311c2a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76621790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d36340425074e3267adab0200c49b19b26091c03d75492134fe000a5f2c56b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e263556d24cfaaa81ec9153b95e1b25d54abdb35b46c3c74fa988a9f252f3`  
		Last Modified: Wed, 11 Jun 2025 09:16:54 GMT  
		Size: 3.5 MB (3470681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5bea448bb73ac691df99daf5772e7cb7307f122b4e0544c289a55be9ee24`  
		Last Modified: Wed, 11 Jun 2025 09:17:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a64acbbc8d220ea4c16baed763b26899f58299a8b85d3b8513f03b3023893`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123dcf4adf55a39c8cf4f202302f0a9dfd6d576c94bf8db94686e5a5ee1f4cf4`  
		Last Modified: Wed, 11 Jun 2025 09:33:08 GMT  
		Size: 13.6 MB (13640507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff08fc5740a571af506cddc0c38e20506f6151e574d4a10d77b748c7c3bd4b`  
		Last Modified: Wed, 11 Jun 2025 09:08:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc080435edc41cfa70a84f9586ffca3f880a9b4cedccc53c481889b18e1e1c2`  
		Last Modified: Wed, 11 Jun 2025 09:33:10 GMT  
		Size: 20.5 MB (20518887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3995038baa7f047e93509966aa2798fbc7bddf48517c43343b9add69edd5df`  
		Last Modified: Wed, 11 Jun 2025 09:08:59 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae69002966a0d0881786cca5d1dfa7b1fb54c0e7b1e4b6bf9c41f92f6208ec`  
		Last Modified: Wed, 11 Jun 2025 09:17:23 GMT  
		Size: 20.0 KB (19991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5db0ec87df386dd8e7ed3e3a943ff4f92de4b419fe7f9bb1b4051dd24a6721`  
		Last Modified: Wed, 11 Jun 2025 15:13:38 GMT  
		Size: 34.0 MB (34010836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae1182fb6a9705ef49f6995317dfcfc6ef3d4b2292bc160d0ba7f8c246dda2e`  
		Last Modified: Wed, 11 Jun 2025 15:13:33 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dfc85b8d16b0b91207b67136a251d9ce8cb168c850f64361a44b74eb632811`  
		Last Modified: Wed, 11 Jun 2025 15:13:34 GMT  
		Size: 820.1 KB (820096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801a936554b178c085f387589b6ab70e3a77b266c792480de4b102e440b5ec69`  
		Last Modified: Wed, 11 Jun 2025 15:13:34 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfea21537f7903164af0fde73e8af3f3e4bb31c1202f44c707716aa939f99af`  
		Last Modified: Wed, 11 Jun 2025 15:13:34 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:d4ac00e2410ff8bd92a7611f7037d8f15546d354f2c4a2381701593533daac36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb743ca06e77355f35a167507d2ef19a4f8eafffb33dc3953830b73b0e7d7327`

```dockerfile
```

-	Layers:
	-	`sha256:7adbbd77a0986b5f5fdaee5236dd188409aa46b4d1ab6910c8d9e50cf9ba35a0`  
		Last Modified: Wed, 11 Jun 2025 16:16:36 GMT  
		Size: 2.2 MB (2175178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4f36bc05bbc26c871efc8f9fe269ca0e1e870ccf0a8856bb6ef17c7cdb0bf3`  
		Last Modified: Wed, 11 Jun 2025 16:16:36 GMT  
		Size: 30.5 KB (30525 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; 386

```console
$ docker pull composer@sha256:e58c3feb27440e5618d734afd387375c6b5e4349448cad8511c199832dc837c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77573235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2857e9dc2712a9e06ed2418cdac6fc9e27233b5acbd1f75203413982c3edadb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298f020aec5b2eb58f3f5d72ed081bd6c76a95799b7e438e4f3384447e42693d`  
		Last Modified: Wed, 11 Jun 2025 01:13:13 GMT  
		Size: 3.5 MB (3527774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3ebeb8397f1f59382fb3bd2f49e7ae5aa3c63f7a6f5adde3d5af0fe196ad48`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c3fa431069cd36b1283a6dd73ec3c559701f45df22999775e61dd0dd4d578`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7db0fb8a413bd77d83d365246beba56a6d3ab745a296bb3119dd1c4844e7e2`  
		Last Modified: Wed, 11 Jun 2025 01:13:12 GMT  
		Size: 13.6 MB (13640494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c81720a5bbf56ccfa06979187dbca8afa1859fb3d323625fe188373b9a06ed`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8fb25f24bc12988d302f27fbc0c27090c75c814e4f8dcb4396e125eafae7cb`  
		Last Modified: Wed, 11 Jun 2025 01:13:11 GMT  
		Size: 21.5 MB (21493036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b67d63641d3800bf94c0e5eb453a80e9e00ec38acbc41e8b2dbe883e470dd6d`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821e028fb8ab3dacea139b63763d5d53b2d0981367d47fcd3f94182a0a2ac456`  
		Last Modified: Wed, 11 Jun 2025 01:13:10 GMT  
		Size: 20.2 KB (20182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5a5771e66b8b5e97c3a2a977ca7089edbbca018038d8b56551bbbc0a8d6d01`  
		Last Modified: Wed, 11 Jun 2025 01:14:24 GMT  
		Size: 34.4 MB (34436667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d09bf8efac1bb2cb2458be039d96f810d55feb69816e0ae630509068dac26`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1e8618a4823c0932806a1a13fbea222f86845076795faa053ecbec1f0d6faa`  
		Last Modified: Wed, 11 Jun 2025 01:14:24 GMT  
		Size: 834.2 KB (834197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bf71238eca349012bf52da0f1f044400815dc5c63c3e0d0288129c0099d23c`  
		Last Modified: Wed, 11 Jun 2025 01:14:24 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387efffd50fee23b95960319fa3959d346523333031fe1d80e9259d8eaa96a01`  
		Last Modified: Wed, 11 Jun 2025 01:14:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:3291d3d1223e7ff57f0794dac617e0a065379495827e752dc779fc6b9adfb2b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d841ab56e87fbb2face98ec347c5d4c254578da7ff3da9f83ef7e2374c43f3e7`

```dockerfile
```

-	Layers:
	-	`sha256:f4b5321199f919e712820423725d97f48a66609b51ef20a0a0653f7922f39d1d`  
		Last Modified: Wed, 11 Jun 2025 04:14:19 GMT  
		Size: 2.2 MB (2174826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462b55391ee34015a5c4784b415a263c63d3f8b068f1b00fe9a649b3c0cb16ca`  
		Last Modified: Wed, 11 Jun 2025 04:14:19 GMT  
		Size: 30.4 KB (30372 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; ppc64le

```console
$ docker pull composer@sha256:71aa4fb51ed8eb9644b328c54c8dbd79b62fc9e1a2a49d05ffbda05e0aaa5359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78994764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f211c2e27a87bc96d094c6ccb729242c29d0744ca672f3092c687e605a14f648`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeaaf729ae44f9ac3f9b3f4551595556a417993152b53954f6f6a89f90a4954`  
		Last Modified: Wed, 11 Jun 2025 09:12:57 GMT  
		Size: 13.6 MB (13640505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5928f2bed6e9375b5161e1fcbc32d598a194fc67da4a537c5d6a3aaab21aa3d0`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f75742ee54512415191653f6d3e2b7b2a4ff66bc4dcc60a24c12d00a0db76`  
		Last Modified: Wed, 11 Jun 2025 09:12:58 GMT  
		Size: 21.9 MB (21874047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189ddb23dd34f7e52d4b584e89ed11029f27d1dee76f138e62d772e61c75c0b6`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2c88f7798e99a903cbf372177b9f7b8f2c70690f8dac0d589ec956038b045f`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a315ceb76a2ac2dda2c8bd167ee4d021a2f0885e86b42406a0c9eb02fb75b9e`  
		Last Modified: Wed, 11 Jun 2025 19:17:11 GMT  
		Size: 35.3 MB (35278992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197c9bbd782fcb082df2515b2222b6e5b48b183fca060886fc83d969d7daf6a`  
		Last Modified: Wed, 11 Jun 2025 19:17:08 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47adf6bb7b9725c3f35a917e6a4788e15e78e2d5f2c6c85b8519cd883a6c868`  
		Last Modified: Wed, 11 Jun 2025 19:17:09 GMT  
		Size: 827.0 KB (827027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0370e10fb9013c22215e0a1c53730207f82dbcf7c04bfc697979d4d2c23c672`  
		Last Modified: Wed, 11 Jun 2025 19:17:10 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b04a1f8b11ff0e8bffdcfb54d185f40d9ce0064b3e530f991ab7e45d3a2502`  
		Last Modified: Wed, 11 Jun 2025 19:17:10 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:109ce7c6ad825e2f9db75f1454aa4eee4c1f8410800be5f83dac44f96929d961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029ad0a254e8c664e15a883aee697a19477f33b01a2138dd82265136223f95b0`

```dockerfile
```

-	Layers:
	-	`sha256:186b2b238a8d42cb52d9062db2c413f6d9b50458fa75bd34dac85458f0b686ec`  
		Last Modified: Wed, 11 Jun 2025 22:13:55 GMT  
		Size: 2.2 MB (2173595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0618ed7cbb2b799975882052f2b94e8ab513868dc41d8345cb8b958cdb373cfe`  
		Last Modified: Wed, 11 Jun 2025 22:13:56 GMT  
		Size: 30.4 KB (30444 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; riscv64

```console
$ docker pull composer@sha256:bfe80827bc9e5b2930762190b55732402255b8a181f8df2b5fdd63364720454a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73096995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b61a446bf05f8cf261e8b5ca68a500ea349fb70f01ac94af71786e9c7b5f1e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0224769088850e26eb3ba2638a8a3febc4b65991ac8cc63dc3f29cf199070`  
		Last Modified: Wed, 11 Jun 2025 05:05:11 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a45f979f3844cfaf9ad9f1a00668b3bb56bc478c711f2d939a7dba0c2ed6e1`  
		Last Modified: Wed, 11 Jun 2025 02:39:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b864e2d5fb63463e7b594794f1b0077ef70793371e80280a29b09008bb9771a`  
		Last Modified: Wed, 11 Jun 2025 05:05:14 GMT  
		Size: 20.4 MB (20388593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba389b9b1d6d27f7a263c92d52685675ded66f85f52a097bec1b658400eebc5`  
		Last Modified: Wed, 11 Jun 2025 02:39:58 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb4f8cea261544e7d849e5aa9581396ef8d4bd1b7c14ceb536acc047c9ff257`  
		Last Modified: Wed, 11 Jun 2025 02:40:00 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d9086703155ae9ef802a8a0d3e98de9aabdf18c7eb07d7758e92bef886259`  
		Last Modified: Wed, 11 Jun 2025 14:10:42 GMT  
		Size: 31.1 MB (31107690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b0b41c4564a3bd6fb68327d016b7b9e8acab85e9d3bf36c289ab0ca8ce1509`  
		Last Modified: Wed, 11 Jun 2025 14:10:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd07fd0d74a58ec594fbc8a688e3b05865a7f96d929c001758e8500260f120d0`  
		Last Modified: Wed, 11 Jun 2025 14:10:32 GMT  
		Size: 818.2 KB (818183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb153d0ff046a6570955b52d245bb74ed310886b1b41d7f1276a94be51d1651e`  
		Last Modified: Wed, 11 Jun 2025 14:10:32 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0107a874ee1b41715b767b7e76f9c687e4103a990e1ad58a680f956b3a6a8e6`  
		Last Modified: Wed, 11 Jun 2025 14:10:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:5ebb7ee2da696e426e23ef9915deab697fdf041040ef86646a171fc28290d6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3878fc9b762a647ee250302ecbd413ba31f025c2aa113487791b6993e2d722b8`

```dockerfile
```

-	Layers:
	-	`sha256:8eb63f1ce3f7eee516d9412f330b8f069a2aa8f274b19d2e5159366987013326`  
		Last Modified: Wed, 11 Jun 2025 16:16:49 GMT  
		Size: 2.2 MB (2171862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ee7486ca8791bfa6fef745038a5ce0428eaad643e8ec60b82c8c3c429dc415`  
		Last Modified: Wed, 11 Jun 2025 16:16:50 GMT  
		Size: 30.4 KB (30443 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; s390x

```console
$ docker pull composer@sha256:eb73759c697f34583db9b7494c7e3ede0cab059e5b1ecb3284e8b669556ac825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75121248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16813e2e25d58914b7f1eef4abf346a0c5c5e2a8fca7a5e73979a19adbd18bd2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 12 May 2025 11:49:32 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Mon, 12 May 2025 11:49:32 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 11:49:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 12 May 2025 11:49:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 12 May 2025 11:49:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_VERSION=8.4.8
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["php" "-a"]
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 12 May 2025 11:49:32 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 12 May 2025 11:49:32 GMT
WORKDIR /app
# Mon, 12 May 2025 11:49:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 12 May 2025 11:49:32 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035d42a37d5be6b1617300170ead6ce8970a5e2e4154fe287efc8af1e2f7441`  
		Last Modified: Wed, 11 Jun 2025 08:13:18 GMT  
		Size: 13.6 MB (13640519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca62563344c489947dce07a51fbce42cb5c2f338f525f3dc64a869bb23eea05`  
		Last Modified: Wed, 11 Jun 2025 06:17:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b12b2d32a5b3932415a1a3b75f1dce848914c79f4be0b381c79061048ef8945`  
		Last Modified: Wed, 11 Jun 2025 10:56:19 GMT  
		Size: 21.4 MB (21446797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13957f45dfaafb933ab00f3283ea48d057cd2179a84687ebe45ad163f535de`  
		Last Modified: Wed, 11 Jun 2025 06:17:35 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48dd1edbbaf646c03ef3f286cc921fbc422e665578b988b9d03d890364f0d5`  
		Last Modified: Wed, 11 Jun 2025 07:14:21 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7301cbc0841ac3202a1b74a41aa6043f1d38879737a0da5c17da8e63aa32c2`  
		Last Modified: Wed, 11 Jun 2025 11:04:18 GMT  
		Size: 31.8 MB (31839063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae5612a3f46089fbce6bbf1de47ad49c5c4c6be46ad9e038f366a967187ab7`  
		Last Modified: Wed, 11 Jun 2025 11:04:10 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70afb032b9f3ac1656f5cca28aa6ec4c1623d47b8430c88d251746f6984495ae`  
		Last Modified: Wed, 11 Jun 2025 11:04:11 GMT  
		Size: 823.5 KB (823498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1267181c9b46b09997bd9cce442e3bac321de699df11a589af306e7a077084`  
		Last Modified: Wed, 11 Jun 2025 11:04:12 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f7264726be68bf863c89466f20b9622a3f4ea819a2af3233e3a056c28d822f`  
		Last Modified: Wed, 11 Jun 2025 11:04:12 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:a00f107a9222298d04a4296d68b654eda679f38487306c5030196a196197e226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63a1562e3a671aa92d1395152adb5b0079f86770497164b6b2ad4dcad16fe6e`

```dockerfile
```

-	Layers:
	-	`sha256:404683acfdb9dcf447ee6e137627e78d91adcaece87a371f891eb286377dbef3`  
		Last Modified: Wed, 11 Jun 2025 13:13:55 GMT  
		Size: 2.2 MB (2171650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4d2f8be03d02a58b777e3161bd961cf75269a73ae8d084cfabe949c7b04a3a`  
		Last Modified: Wed, 11 Jun 2025 13:13:56 GMT  
		Size: 30.4 KB (30402 bytes)  
		MIME: application/vnd.in-toto+json
