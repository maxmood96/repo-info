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
$ docker pull composer@sha256:a2afe7a2f5bf47bbed994191ed96beb5d36af3e8f78c6268fbff13f0bcade52c
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
$ docker pull composer@sha256:89c78fda6439a73ea0fe55f5dacbc08c8721e7367cab185bb41b8e1e9d3ca652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77583081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bfe538f7b1771e7cb89600dc4fa2a392fa2a3d69d8f3c5cbb0cd875573fe43`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd2e180aa89ecb0845d1628b35579e1eb961f47975c3bc5a05ede5b6d47cb58`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 5.6 MB (5629137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d695b6cf2c8c3fcda26df544b054468a24be6cd41394db0208e3a333f18822f3`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7a3d474383ce078a67dbd96e1b61dc0d0b1fe673292ddc8d689e44c69655c2`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7370e670250547c9c1b145d13d02d6fa20bab3226e296408d9031c6a495186b6`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 13.6 MB (13609848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877e753ed32393f8eb06b7cf17507f31ab0f3db652e55c55ab86c82c3df4bf55`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d0fa737a71d88d348cb60ef0ff16ef4df36a45dddcd8bfe55e07d84f69a6a`  
		Last Modified: Fri, 14 Feb 2025 04:09:21 GMT  
		Size: 21.4 MB (21352652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf998db890f8e3ee8a94d02d3ea220e376efdd8371bffcc8379ce3ed9eee6e`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280727407916ee60ca49cf4ea07ef8f4b509704188598c3a99b973502ec133e3`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 20.1 KB (20058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d1ac227a2abc7451ff1ba44084161fdc97e0fd637a541506f29a6e04bd2617`  
		Last Modified: Fri, 14 Feb 2025 05:15:16 GMT  
		Size: 31.9 MB (31907430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26911d9a068609f04639f02836da2c8f3ffe7e740e2392cc7087732446bb7012`  
		Last Modified: Fri, 14 Feb 2025 05:15:14 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d2d59f49fd5f9ccbb78a72ac4061ac163a49203fd83856de27e769a96568dd`  
		Last Modified: Fri, 14 Feb 2025 05:15:16 GMT  
		Size: 1.4 MB (1417386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c4bdca85c0297d85aeaaa9acfbc142b0b6cdf89c35d060d82f47da0d553390`  
		Last Modified: Fri, 14 Feb 2025 05:15:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624f18a9bde02f497deb425a36d553c558471f355cba5653d43be83dd0e04e6a`  
		Last Modified: Fri, 14 Feb 2025 04:11:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:09c4adb5436b4530d27add05e4a5eadd0787da17926170aa3009e8addbdd0bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af42e342bfb0d0d385da9c3e1046f7e95f5b2c6a95e5c33e28a8f595062d357`

```dockerfile
```

-	Layers:
	-	`sha256:875494bec533267312793179ce376e5a54e9b9b6c71af43068480772cf8065eb`  
		Last Modified: Fri, 14 Feb 2025 05:13:35 GMT  
		Size: 2.2 MB (2157759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:862a21ebaa75a8534fa5226110f8353d8ca52a296c2ce1583d88b9a9d23d37d4`  
		Last Modified: Fri, 14 Feb 2025 05:13:35 GMT  
		Size: 30.4 KB (30420 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:a150485d52bfe0dddac59c11af2a759512ee9e3bf9ea23f5c7740f6d0213e0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75792714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9c79feb5ac9907bf09e52b98c076aa532a620159d2728e5cd5f4e446fd89a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 15 Jan 2025 01:25:26 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 15 Jan 2025 08:46:52 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 15 Jan 2025 08:46:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f6b305cd77dc6b597a3169970fd07b292703741539eaded2551c0d9a9a3ce2`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 13.6 MB (13609882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45767d1a2e12eb03ad18b9a7888cfb876903b7b27f5e22317a9a419e6c9357a4`  
		Last Modified: Fri, 14 Feb 2025 02:36:56 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b187df6e200be4ae6d666ab1d197a76dab384b63436f2df83f864d48fc6190f`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 22.4 MB (22402333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15e817c4c3f6223fc729a85f3b2dc3fa7ea9c2a3bf884f218dee6205043c6cf`  
		Last Modified: Fri, 14 Feb 2025 02:36:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45820a47f5394522a107e4a692c1e0d3689a29363793dbbf16751ed29bade6`  
		Last Modified: Fri, 14 Feb 2025 05:14:24 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07fdd9ff35b65c886cb11f76394f3a6058bcc6ffe163f41c4b09e0855ae0`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 31.6 MB (31601043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0554a9e2a4103b0bc17495a139a3314d3e4b40b4bc9ac6728a33ff747fe0226a`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b896ec9eaa77d9c05563e35253a48470aaae191c869961f4aeec44e6b1b6c888`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 1.5 MB (1490347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71788a201fd4484623058492eba6fc6241bfb6f5ca90f5eb131a2c29ec530377`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfd11890e74352f27cb92d1ca7523bdccc6e056291e507fc8d7cee80e3190c6`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:2d5a38cff7db945dc384c3c2fb8d9cdcab28ac49fb3a38448d64dbaaa2a6bea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988a18b5d47c028c68300ab40772f2201b839036c7c7403077d49c6fd58f660f`

```dockerfile
```

-	Layers:
	-	`sha256:36a53d4e8d65c6a567729d400b3ca0fe89e7adc8f96c1d230a6b7b59d6fdbf67`  
		Last Modified: Fri, 14 Feb 2025 05:13:37 GMT  
		Size: 30.3 KB (30299 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:71e98f991d1a52342ce89445c5e16b58c74117680e5b295dddf9a5e52626139b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69234309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34b176fa58957b0e7dbcf8e4fb1b298dd12b3c98705373773007ffdb0bb5de8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 15 Jan 2025 00:28:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 21:24:38 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 21:24:39 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 21:24:35 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b02f56cd79bb67b2e6a8c6a2926c13febe08627a14d51ac60cca77caa0bd9b`  
		Last Modified: Tue, 04 Feb 2025 15:48:01 GMT  
		Size: 30.2 MB (30150807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a36ded2ef8fef32700c53fb042e1d25e6c4b243e0eaa2fa4c9987aa4de12ad9`  
		Last Modified: Tue, 04 Feb 2025 16:45:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb36c56770ad29b53f6869471657e9474c199dfe3564967fd19ca11bd3366a5`  
		Last Modified: Wed, 05 Feb 2025 19:48:56 GMT  
		Size: 1.2 MB (1246037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b1e47e36ad2039a96855b35aa652d898b92a26e1c6c7eee5d4903e150c489a`  
		Last Modified: Mon, 03 Feb 2025 20:27:36 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d404a176f307405e948ed6b62f2968d8a5dd2fc85dbe2f21abee69cffbc415cf`  
		Last Modified: Wed, 05 Feb 2025 19:48:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:53e501cae7d9472a2a76988b1828f6aeb92e98e35c7f7312dd805c23cbeac79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05f81ae33c6783a9d1c2f6a35daee7ba87f8860e8bf10eb791c9dfba79b5ffc`

```dockerfile
```

-	Layers:
	-	`sha256:2c5f9f98bd06fe880dcc8314697b193b5fff605294579c76f03ec7a7e0a6f98d`  
		Last Modified: Fri, 14 Feb 2025 05:13:39 GMT  
		Size: 2.2 MB (2158075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:326b816a54e2dd57d56f53e0a264a2cab278b2d9bfb68c8d7fc3e702a801959d`  
		Last Modified: Fri, 14 Feb 2025 05:13:39 GMT  
		Size: 30.5 KB (30514 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:30c48973f0dd5e950d9795b36a9596cb28ec9f0bcac7bad860410be2632a1dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78862207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a57571662b820df3636935072533f5d98a59074e505d8051a533f7e79a9c19`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Tue, 14 Jan 2025 20:34:52 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Tue, 14 Jan 2025 20:34:51 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf60bd0bee7688614b1af07694e9e862a6e468345b4d8c1274b901e3308d850`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 13.6 MB (13609906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5935d74cc4f8900f9fe931cf198c384636eccfe5b27fcf8222bad1a34adc3c`  
		Last Modified: Fri, 14 Feb 2025 03:03:44 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3dd78614141a7cf92fd59b8e7fccf1f50faaef52fe4a0a661d5b0d846a4ea`  
		Last Modified: Fri, 14 Feb 2025 05:14:49 GMT  
		Size: 24.4 MB (24449108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eb61917bf0624ecf3420f926f6053b48728486c0188ada2088cb4c8939857e`  
		Last Modified: Fri, 14 Feb 2025 05:12:47 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc28a76fb7622bd8689c33b509f275a2d2558a77eccd18f266bc3ce660c7deb6`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7df60278df6c56d8ef9b2df595e68e15a33c291bf23b297f3ebb680a74161f`  
		Last Modified: Fri, 14 Feb 2025 05:14:54 GMT  
		Size: 32.0 MB (32009162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24085d57bfcbbba22355b95422cdf2ec94dde42b3fed500ec739e6f28f614030`  
		Last Modified: Fri, 14 Feb 2025 05:14:39 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb41014c418713cf7a78b82f17d137451b22af48c99c2d77553f985dce68f054`  
		Last Modified: Fri, 14 Feb 2025 05:26:09 GMT  
		Size: 1.4 MB (1449250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b05b997b07dc8f77af9151439c16c2ea8fad59e9b5d7cebebcf4cf115ed279`  
		Last Modified: Fri, 14 Feb 2025 05:26:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e11873c3cb1ffd7ec97c973f381f94a9ae954ace6058a427ac2c94d3651ee4`  
		Last Modified: Fri, 14 Feb 2025 05:26:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:d5285e5db7648af9bdf1839ab38bf3577cce0e63f80c3c000288ccbd35f311f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95033207bc5cf6917602de71a9a2516a141208aa093ab207198f0b1c732da2be`

```dockerfile
```

-	Layers:
	-	`sha256:b8590f554c9ce9740018238bd52fd812f6d6b2d17bb96ec92b697c65ba2eb75e`  
		Last Modified: Fri, 14 Feb 2025 05:13:41 GMT  
		Size: 2.2 MB (2157899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:029a72d217f5af38ed4d1cef16ec25fce065180721e6d388860d8add5cdc6c7b`  
		Last Modified: Fri, 14 Feb 2025 05:13:41 GMT  
		Size: 30.5 KB (30542 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:8f635b56545810b2e999180caa9b9b55882af87e2e0c355b7bc418a48d743ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78283996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6781ff65f70b572fb67027f9371191874e980dda6602883aa0faf6efa20d2b0a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c4f61d7599e7869ad3a9d452f69e9bc3899f18d70701124026229667c57db`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 5.5 MB (5479161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb08d2bfa2365278e7427cd03c6a3b6d0d200bf048c31056c211ff6bd1d83e3f`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ccac1acad29397cc55b48dcff4f9ee2a1ad8bb562aefc4e7345e5ba177ea66`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77470d2cfb3c06673c0297f09fdcfd1debad3d8c75b8f08ee1be3f66d5edfb5`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 13.6 MB (13609860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56194a5a61ce8b305a5554d8aff3980c32fe8df11e9dae038a5c1169482a4dff`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb641c65fcb36b09714fd6d6634df4fa431b7f127829dd93eecb97dc6d4674`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 21.9 MB (21875599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8652ddf39bd8a77eabbc758325596a213cfa201e124d3a8e14c0d3fedbbe920a`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7c976ea7a0a95cb41a13dd1eff7887ba420c913603c766514f637eb3933a56`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd93bacb6d5493996f5c66c144f57c835b61ad61c616f85e4c67f05b4756999`  
		Last Modified: Fri, 14 Feb 2025 04:09:44 GMT  
		Size: 32.4 MB (32391482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307c85cb9cd140a46bbfe9a5836b595d4ac469d955bcf947e382f9caa5fc7084`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c094d28a1f3b8b49e3ebb8109fd30fd8bd4fc6d59ca6fdd66d7bf7e0744e6667`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 1.4 MB (1439842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de5cc60f8a748966dd208e96a6b39ea76dbb2cb0fb74e9d39beec1b0cc0e7de`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f4051ab2bc9b427dbc31f39e35232e46b7de196f743bdaa8cbae6e807bc3e`  
		Last Modified: Fri, 14 Feb 2025 05:08:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:3a37b4832b3ca9c9885c7d32b11ca53226593070d5ba3a5cedd85638a8863bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f44c4c1052cacf34fe16350b6b24e9c9a4057cb397a5582f3b486f738ff2fad`

```dockerfile
```

-	Layers:
	-	`sha256:85b79d12514157d042d80c216a35d436a1b96d8983ee819698f0ddb33d25106f`  
		Last Modified: Fri, 14 Feb 2025 05:13:43 GMT  
		Size: 2.2 MB (2157547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a948bea48791191572cbda7fc7e13ee352678e8ecacd68d72d85e65f36c45f02`  
		Last Modified: Fri, 14 Feb 2025 05:13:43 GMT  
		Size: 30.4 KB (30389 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:c97997e352275960898a3222f0db5c4be4294e6dd6d35a77f590ebc20cf11f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80515647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c83e5072d6a526ed37429ef262ce4b2356263e676e212d0857ab10ab9b6f12c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 15 Jan 2025 04:47:37 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704aa6bd4f8e770473b08a863515e74229b7563d9a2694d4dcffebd63189d5ab`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 13.6 MB (13609905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43c7e0504550dd35c7e6f3c1f5c61ed5db00067d11ffd3741e8f23b0dc16660`  
		Last Modified: Fri, 14 Feb 2025 05:09:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1167c96dbe49f246b96adc095a28edefcc2fe61bdc39108f8050c176699f483b`  
		Last Modified: Fri, 14 Feb 2025 02:47:38 GMT  
		Size: 25.4 MB (25398061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e16862c42f1028fedb8b04c6b22bd4e945a213a3e5a113872b385ee049f719`  
		Last Modified: Fri, 14 Feb 2025 05:10:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10f990e07f31e3d864671985a77e555905c511508a842be3262c8c7b9a96ec9`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 19.9 KB (19884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e260f2e53edd998f9cf2d3ba59929e4a7ff0f39075889a9b99dcb55b35732a9`  
		Last Modified: Fri, 14 Feb 2025 04:28:17 GMT  
		Size: 33.0 MB (32950697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717745514d5555d6812144710631aed2946af2ee5c721b80f8bf0a8b750bd43`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f754f264cd421594b8323374dfcfd9bf76077c4627c541bdb80a4730fb7a60`  
		Last Modified: Fri, 14 Feb 2025 04:29:09 GMT  
		Size: 1.5 MB (1482296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab08887a5d9bbd79a495e606d9d89e959eb261b577a23a2e519795ca9236961`  
		Last Modified: Fri, 14 Feb 2025 04:29:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3481825d9b4a4d2da079a340e064d36042cf1986b82fc42fff571e5570b42571`  
		Last Modified: Fri, 14 Feb 2025 04:29:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:747826bb6d6b8f04807ef15560e97c7da18cafda755fe1847f5ba4645ea7297f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98be37cede8e3d2663db85372a5bad03814548c5bcef46e23042098f208a5f8`

```dockerfile
```

-	Layers:
	-	`sha256:93b0cbeb6f16e9f7dca28274beba03229c4c02ddd8fae05584310d503ea4a08e`  
		Last Modified: Fri, 14 Feb 2025 05:13:45 GMT  
		Size: 2.2 MB (2156316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9272eec9108506c2f41df4ddda3e358ca5837fe37f986ae93b022abbb880c54a`  
		Last Modified: Fri, 14 Feb 2025 05:13:45 GMT  
		Size: 30.5 KB (30462 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:c3c9f3482d12c572d589e18ef215c0f7e056bfb3ae124b8c726bea123adf9e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73035743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1464cc8f38a0eabd86c497babccc6353c206a5b1d55d1bfa83086d33eace4fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 15 Jan 2025 08:47:48 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 15 Jan 2025 03:01:25 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 15 Jan 2025 10:06:18 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 21:25:44 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 21:25:46 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 21:25:42 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df9d36d8de7098821c518291549b46c279424dc339b2da655e42c88a93a214e`  
		Last Modified: Mon, 10 Feb 2025 19:35:11 GMT  
		Size: 31.0 MB (31000989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e43f72402a8544ac8a8358f26a470e096d8b0a4416c1d930f95b5531cbe553`  
		Last Modified: Fri, 07 Feb 2025 22:27:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ca67f8caa2d3709c2cd2b7e7e9a7752581c0dceca488eff9d672f529ed5682`  
		Last Modified: Tue, 21 Jan 2025 23:38:21 GMT  
		Size: 1.3 MB (1290090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855f16e727d48ec3d7581bd9b6bee6db965d81ba5f16da020baac719ce5da371`  
		Last Modified: Tue, 21 Jan 2025 23:38:21 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b888ba3f844d59fc50dcf966337a42325158e35ea08647908a373dc882b5ce2`  
		Last Modified: Tue, 21 Jan 2025 23:38:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:fbe28f7c58d8937ed88b04bfe8c6899c96815c0084cffe96d7b3effe947f1789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8434e79d7f842819526fca445009ad56405ca86530dd22b451734252956e8aa0`

```dockerfile
```

-	Layers:
	-	`sha256:0c0560ab6b068394761652584993f47e1f0596a5b2948832e55fea64e75e4278`  
		Last Modified: Fri, 14 Feb 2025 05:13:47 GMT  
		Size: 2.2 MB (2155258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e50fa0e87f0c01f3a89e74c5a8fa1d999769548a7032982e7aeeb6b16ccb3ba`  
		Last Modified: Fri, 14 Feb 2025 05:13:47 GMT  
		Size: 30.5 KB (30462 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:6863809daf9e402b682da453c91e7185938f0fac786f388800cc7a8cf3b8d289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74994922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8119e3d5557f05e41ee5bb2b3fa590d09f007dc84be7814c6c3a4ca3e8831e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 15 Jan 2025 04:47:39 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 15 Jan 2025 04:47:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 21:26:01 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 21:26:03 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 21:25:59 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0774f657550ec6a831bbd0d72b777f8d8977a4143f082a39f86537a6691b415c`  
		Last Modified: Fri, 07 Feb 2025 22:27:36 GMT  
		Size: 31.7 MB (31677626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f93262ff5f92b789b5e28a5fbc8a229794cf568ee5c1a3fe803f21245857e1`  
		Last Modified: Fri, 07 Feb 2025 22:27:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc786a839d735394743a5eb5630ba3529273688ecfe8ce262710fb57014ae358`  
		Last Modified: Tue, 21 Jan 2025 23:32:26 GMT  
		Size: 1.3 MB (1298940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ebb543a3536234364dfb4e4f4f96fcd01a49e979f2f67b0139ff89ff2b57ab`  
		Last Modified: Tue, 21 Jan 2025 23:32:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166fc7a4788479b5d292be235658e3707989fa94ffe11ed54430db9af363ff1e`  
		Last Modified: Tue, 21 Jan 2025 23:32:26 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:913299d493026fe571d5cf8d6fe0ba8add58b3e772628edb3b01d2e4aa3e6aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78420dc46f8fc1c6b48d9ed023125a8721f0b854706bd09a4a6e26b537ae5420`

```dockerfile
```

-	Layers:
	-	`sha256:093bcd368cdec2123f7405acb7662a12b8326dbf53f1337e2151acfc9a5900f6`  
		Last Modified: Fri, 14 Feb 2025 05:13:49 GMT  
		Size: 2.2 MB (2155044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9eeb30a62a9c40790abbbe0c25e926fe456a612a454a88cfba32a411e345fb`  
		Last Modified: Fri, 14 Feb 2025 05:13:49 GMT  
		Size: 30.4 KB (30420 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:a2afe7a2f5bf47bbed994191ed96beb5d36af3e8f78c6268fbff13f0bcade52c
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
$ docker pull composer@sha256:89c78fda6439a73ea0fe55f5dacbc08c8721e7367cab185bb41b8e1e9d3ca652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77583081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bfe538f7b1771e7cb89600dc4fa2a392fa2a3d69d8f3c5cbb0cd875573fe43`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd2e180aa89ecb0845d1628b35579e1eb961f47975c3bc5a05ede5b6d47cb58`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 5.6 MB (5629137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d695b6cf2c8c3fcda26df544b054468a24be6cd41394db0208e3a333f18822f3`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7a3d474383ce078a67dbd96e1b61dc0d0b1fe673292ddc8d689e44c69655c2`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7370e670250547c9c1b145d13d02d6fa20bab3226e296408d9031c6a495186b6`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 13.6 MB (13609848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877e753ed32393f8eb06b7cf17507f31ab0f3db652e55c55ab86c82c3df4bf55`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d0fa737a71d88d348cb60ef0ff16ef4df36a45dddcd8bfe55e07d84f69a6a`  
		Last Modified: Fri, 14 Feb 2025 04:09:21 GMT  
		Size: 21.4 MB (21352652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf998db890f8e3ee8a94d02d3ea220e376efdd8371bffcc8379ce3ed9eee6e`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280727407916ee60ca49cf4ea07ef8f4b509704188598c3a99b973502ec133e3`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 20.1 KB (20058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d1ac227a2abc7451ff1ba44084161fdc97e0fd637a541506f29a6e04bd2617`  
		Last Modified: Fri, 14 Feb 2025 05:15:16 GMT  
		Size: 31.9 MB (31907430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26911d9a068609f04639f02836da2c8f3ffe7e740e2392cc7087732446bb7012`  
		Last Modified: Fri, 14 Feb 2025 05:15:14 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d2d59f49fd5f9ccbb78a72ac4061ac163a49203fd83856de27e769a96568dd`  
		Last Modified: Fri, 14 Feb 2025 05:15:16 GMT  
		Size: 1.4 MB (1417386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c4bdca85c0297d85aeaaa9acfbc142b0b6cdf89c35d060d82f47da0d553390`  
		Last Modified: Fri, 14 Feb 2025 05:15:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624f18a9bde02f497deb425a36d553c558471f355cba5653d43be83dd0e04e6a`  
		Last Modified: Fri, 14 Feb 2025 04:11:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:09c4adb5436b4530d27add05e4a5eadd0787da17926170aa3009e8addbdd0bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af42e342bfb0d0d385da9c3e1046f7e95f5b2c6a95e5c33e28a8f595062d357`

```dockerfile
```

-	Layers:
	-	`sha256:875494bec533267312793179ce376e5a54e9b9b6c71af43068480772cf8065eb`  
		Last Modified: Fri, 14 Feb 2025 05:13:35 GMT  
		Size: 2.2 MB (2157759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:862a21ebaa75a8534fa5226110f8353d8ca52a296c2ce1583d88b9a9d23d37d4`  
		Last Modified: Fri, 14 Feb 2025 05:13:35 GMT  
		Size: 30.4 KB (30420 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:a150485d52bfe0dddac59c11af2a759512ee9e3bf9ea23f5c7740f6d0213e0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75792714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9c79feb5ac9907bf09e52b98c076aa532a620159d2728e5cd5f4e446fd89a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 15 Jan 2025 01:25:26 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 15 Jan 2025 08:46:52 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 15 Jan 2025 08:46:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f6b305cd77dc6b597a3169970fd07b292703741539eaded2551c0d9a9a3ce2`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 13.6 MB (13609882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45767d1a2e12eb03ad18b9a7888cfb876903b7b27f5e22317a9a419e6c9357a4`  
		Last Modified: Fri, 14 Feb 2025 02:36:56 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b187df6e200be4ae6d666ab1d197a76dab384b63436f2df83f864d48fc6190f`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 22.4 MB (22402333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15e817c4c3f6223fc729a85f3b2dc3fa7ea9c2a3bf884f218dee6205043c6cf`  
		Last Modified: Fri, 14 Feb 2025 02:36:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45820a47f5394522a107e4a692c1e0d3689a29363793dbbf16751ed29bade6`  
		Last Modified: Fri, 14 Feb 2025 05:14:24 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07fdd9ff35b65c886cb11f76394f3a6058bcc6ffe163f41c4b09e0855ae0`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 31.6 MB (31601043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0554a9e2a4103b0bc17495a139a3314d3e4b40b4bc9ac6728a33ff747fe0226a`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b896ec9eaa77d9c05563e35253a48470aaae191c869961f4aeec44e6b1b6c888`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 1.5 MB (1490347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71788a201fd4484623058492eba6fc6241bfb6f5ca90f5eb131a2c29ec530377`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfd11890e74352f27cb92d1ca7523bdccc6e056291e507fc8d7cee80e3190c6`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:2d5a38cff7db945dc384c3c2fb8d9cdcab28ac49fb3a38448d64dbaaa2a6bea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988a18b5d47c028c68300ab40772f2201b839036c7c7403077d49c6fd58f660f`

```dockerfile
```

-	Layers:
	-	`sha256:36a53d4e8d65c6a567729d400b3ca0fe89e7adc8f96c1d230a6b7b59d6fdbf67`  
		Last Modified: Fri, 14 Feb 2025 05:13:37 GMT  
		Size: 30.3 KB (30299 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:71e98f991d1a52342ce89445c5e16b58c74117680e5b295dddf9a5e52626139b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69234309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34b176fa58957b0e7dbcf8e4fb1b298dd12b3c98705373773007ffdb0bb5de8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 15 Jan 2025 00:28:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 21:24:38 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 21:24:39 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 21:24:35 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b02f56cd79bb67b2e6a8c6a2926c13febe08627a14d51ac60cca77caa0bd9b`  
		Last Modified: Tue, 04 Feb 2025 15:48:01 GMT  
		Size: 30.2 MB (30150807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a36ded2ef8fef32700c53fb042e1d25e6c4b243e0eaa2fa4c9987aa4de12ad9`  
		Last Modified: Tue, 04 Feb 2025 16:45:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb36c56770ad29b53f6869471657e9474c199dfe3564967fd19ca11bd3366a5`  
		Last Modified: Wed, 05 Feb 2025 19:48:56 GMT  
		Size: 1.2 MB (1246037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b1e47e36ad2039a96855b35aa652d898b92a26e1c6c7eee5d4903e150c489a`  
		Last Modified: Mon, 03 Feb 2025 20:27:36 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d404a176f307405e948ed6b62f2968d8a5dd2fc85dbe2f21abee69cffbc415cf`  
		Last Modified: Wed, 05 Feb 2025 19:48:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:53e501cae7d9472a2a76988b1828f6aeb92e98e35c7f7312dd805c23cbeac79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05f81ae33c6783a9d1c2f6a35daee7ba87f8860e8bf10eb791c9dfba79b5ffc`

```dockerfile
```

-	Layers:
	-	`sha256:2c5f9f98bd06fe880dcc8314697b193b5fff605294579c76f03ec7a7e0a6f98d`  
		Last Modified: Fri, 14 Feb 2025 05:13:39 GMT  
		Size: 2.2 MB (2158075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:326b816a54e2dd57d56f53e0a264a2cab278b2d9bfb68c8d7fc3e702a801959d`  
		Last Modified: Fri, 14 Feb 2025 05:13:39 GMT  
		Size: 30.5 KB (30514 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:30c48973f0dd5e950d9795b36a9596cb28ec9f0bcac7bad860410be2632a1dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78862207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a57571662b820df3636935072533f5d98a59074e505d8051a533f7e79a9c19`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Tue, 14 Jan 2025 20:34:52 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Tue, 14 Jan 2025 20:34:51 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf60bd0bee7688614b1af07694e9e862a6e468345b4d8c1274b901e3308d850`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 13.6 MB (13609906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5935d74cc4f8900f9fe931cf198c384636eccfe5b27fcf8222bad1a34adc3c`  
		Last Modified: Fri, 14 Feb 2025 03:03:44 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3dd78614141a7cf92fd59b8e7fccf1f50faaef52fe4a0a661d5b0d846a4ea`  
		Last Modified: Fri, 14 Feb 2025 05:14:49 GMT  
		Size: 24.4 MB (24449108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eb61917bf0624ecf3420f926f6053b48728486c0188ada2088cb4c8939857e`  
		Last Modified: Fri, 14 Feb 2025 05:12:47 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc28a76fb7622bd8689c33b509f275a2d2558a77eccd18f266bc3ce660c7deb6`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7df60278df6c56d8ef9b2df595e68e15a33c291bf23b297f3ebb680a74161f`  
		Last Modified: Fri, 14 Feb 2025 05:14:54 GMT  
		Size: 32.0 MB (32009162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24085d57bfcbbba22355b95422cdf2ec94dde42b3fed500ec739e6f28f614030`  
		Last Modified: Fri, 14 Feb 2025 05:14:39 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb41014c418713cf7a78b82f17d137451b22af48c99c2d77553f985dce68f054`  
		Last Modified: Fri, 14 Feb 2025 05:26:09 GMT  
		Size: 1.4 MB (1449250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b05b997b07dc8f77af9151439c16c2ea8fad59e9b5d7cebebcf4cf115ed279`  
		Last Modified: Fri, 14 Feb 2025 05:26:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e11873c3cb1ffd7ec97c973f381f94a9ae954ace6058a427ac2c94d3651ee4`  
		Last Modified: Fri, 14 Feb 2025 05:26:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:d5285e5db7648af9bdf1839ab38bf3577cce0e63f80c3c000288ccbd35f311f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95033207bc5cf6917602de71a9a2516a141208aa093ab207198f0b1c732da2be`

```dockerfile
```

-	Layers:
	-	`sha256:b8590f554c9ce9740018238bd52fd812f6d6b2d17bb96ec92b697c65ba2eb75e`  
		Last Modified: Fri, 14 Feb 2025 05:13:41 GMT  
		Size: 2.2 MB (2157899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:029a72d217f5af38ed4d1cef16ec25fce065180721e6d388860d8add5cdc6c7b`  
		Last Modified: Fri, 14 Feb 2025 05:13:41 GMT  
		Size: 30.5 KB (30542 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:8f635b56545810b2e999180caa9b9b55882af87e2e0c355b7bc418a48d743ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78283996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6781ff65f70b572fb67027f9371191874e980dda6602883aa0faf6efa20d2b0a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c4f61d7599e7869ad3a9d452f69e9bc3899f18d70701124026229667c57db`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 5.5 MB (5479161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb08d2bfa2365278e7427cd03c6a3b6d0d200bf048c31056c211ff6bd1d83e3f`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ccac1acad29397cc55b48dcff4f9ee2a1ad8bb562aefc4e7345e5ba177ea66`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77470d2cfb3c06673c0297f09fdcfd1debad3d8c75b8f08ee1be3f66d5edfb5`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 13.6 MB (13609860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56194a5a61ce8b305a5554d8aff3980c32fe8df11e9dae038a5c1169482a4dff`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb641c65fcb36b09714fd6d6634df4fa431b7f127829dd93eecb97dc6d4674`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 21.9 MB (21875599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8652ddf39bd8a77eabbc758325596a213cfa201e124d3a8e14c0d3fedbbe920a`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7c976ea7a0a95cb41a13dd1eff7887ba420c913603c766514f637eb3933a56`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd93bacb6d5493996f5c66c144f57c835b61ad61c616f85e4c67f05b4756999`  
		Last Modified: Fri, 14 Feb 2025 04:09:44 GMT  
		Size: 32.4 MB (32391482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307c85cb9cd140a46bbfe9a5836b595d4ac469d955bcf947e382f9caa5fc7084`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c094d28a1f3b8b49e3ebb8109fd30fd8bd4fc6d59ca6fdd66d7bf7e0744e6667`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 1.4 MB (1439842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de5cc60f8a748966dd208e96a6b39ea76dbb2cb0fb74e9d39beec1b0cc0e7de`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f4051ab2bc9b427dbc31f39e35232e46b7de196f743bdaa8cbae6e807bc3e`  
		Last Modified: Fri, 14 Feb 2025 05:08:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:3a37b4832b3ca9c9885c7d32b11ca53226593070d5ba3a5cedd85638a8863bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f44c4c1052cacf34fe16350b6b24e9c9a4057cb397a5582f3b486f738ff2fad`

```dockerfile
```

-	Layers:
	-	`sha256:85b79d12514157d042d80c216a35d436a1b96d8983ee819698f0ddb33d25106f`  
		Last Modified: Fri, 14 Feb 2025 05:13:43 GMT  
		Size: 2.2 MB (2157547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a948bea48791191572cbda7fc7e13ee352678e8ecacd68d72d85e65f36c45f02`  
		Last Modified: Fri, 14 Feb 2025 05:13:43 GMT  
		Size: 30.4 KB (30389 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:c97997e352275960898a3222f0db5c4be4294e6dd6d35a77f590ebc20cf11f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80515647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c83e5072d6a526ed37429ef262ce4b2356263e676e212d0857ab10ab9b6f12c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 15 Jan 2025 04:47:37 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704aa6bd4f8e770473b08a863515e74229b7563d9a2694d4dcffebd63189d5ab`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 13.6 MB (13609905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43c7e0504550dd35c7e6f3c1f5c61ed5db00067d11ffd3741e8f23b0dc16660`  
		Last Modified: Fri, 14 Feb 2025 05:09:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1167c96dbe49f246b96adc095a28edefcc2fe61bdc39108f8050c176699f483b`  
		Last Modified: Fri, 14 Feb 2025 02:47:38 GMT  
		Size: 25.4 MB (25398061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e16862c42f1028fedb8b04c6b22bd4e945a213a3e5a113872b385ee049f719`  
		Last Modified: Fri, 14 Feb 2025 05:10:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10f990e07f31e3d864671985a77e555905c511508a842be3262c8c7b9a96ec9`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 19.9 KB (19884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e260f2e53edd998f9cf2d3ba59929e4a7ff0f39075889a9b99dcb55b35732a9`  
		Last Modified: Fri, 14 Feb 2025 04:28:17 GMT  
		Size: 33.0 MB (32950697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717745514d5555d6812144710631aed2946af2ee5c721b80f8bf0a8b750bd43`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f754f264cd421594b8323374dfcfd9bf76077c4627c541bdb80a4730fb7a60`  
		Last Modified: Fri, 14 Feb 2025 04:29:09 GMT  
		Size: 1.5 MB (1482296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab08887a5d9bbd79a495e606d9d89e959eb261b577a23a2e519795ca9236961`  
		Last Modified: Fri, 14 Feb 2025 04:29:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3481825d9b4a4d2da079a340e064d36042cf1986b82fc42fff571e5570b42571`  
		Last Modified: Fri, 14 Feb 2025 04:29:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:747826bb6d6b8f04807ef15560e97c7da18cafda755fe1847f5ba4645ea7297f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98be37cede8e3d2663db85372a5bad03814548c5bcef46e23042098f208a5f8`

```dockerfile
```

-	Layers:
	-	`sha256:93b0cbeb6f16e9f7dca28274beba03229c4c02ddd8fae05584310d503ea4a08e`  
		Last Modified: Fri, 14 Feb 2025 05:13:45 GMT  
		Size: 2.2 MB (2156316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9272eec9108506c2f41df4ddda3e358ca5837fe37f986ae93b022abbb880c54a`  
		Last Modified: Fri, 14 Feb 2025 05:13:45 GMT  
		Size: 30.5 KB (30462 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:c3c9f3482d12c572d589e18ef215c0f7e056bfb3ae124b8c726bea123adf9e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73035743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1464cc8f38a0eabd86c497babccc6353c206a5b1d55d1bfa83086d33eace4fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 15 Jan 2025 08:47:48 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 15 Jan 2025 03:01:25 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 15 Jan 2025 10:06:18 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 21:25:44 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 21:25:46 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 21:25:42 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df9d36d8de7098821c518291549b46c279424dc339b2da655e42c88a93a214e`  
		Last Modified: Mon, 10 Feb 2025 19:35:11 GMT  
		Size: 31.0 MB (31000989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e43f72402a8544ac8a8358f26a470e096d8b0a4416c1d930f95b5531cbe553`  
		Last Modified: Fri, 07 Feb 2025 22:27:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ca67f8caa2d3709c2cd2b7e7e9a7752581c0dceca488eff9d672f529ed5682`  
		Last Modified: Tue, 21 Jan 2025 23:38:21 GMT  
		Size: 1.3 MB (1290090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855f16e727d48ec3d7581bd9b6bee6db965d81ba5f16da020baac719ce5da371`  
		Last Modified: Tue, 21 Jan 2025 23:38:21 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b888ba3f844d59fc50dcf966337a42325158e35ea08647908a373dc882b5ce2`  
		Last Modified: Tue, 21 Jan 2025 23:38:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:fbe28f7c58d8937ed88b04bfe8c6899c96815c0084cffe96d7b3effe947f1789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8434e79d7f842819526fca445009ad56405ca86530dd22b451734252956e8aa0`

```dockerfile
```

-	Layers:
	-	`sha256:0c0560ab6b068394761652584993f47e1f0596a5b2948832e55fea64e75e4278`  
		Last Modified: Fri, 14 Feb 2025 05:13:47 GMT  
		Size: 2.2 MB (2155258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e50fa0e87f0c01f3a89e74c5a8fa1d999769548a7032982e7aeeb6b16ccb3ba`  
		Last Modified: Fri, 14 Feb 2025 05:13:47 GMT  
		Size: 30.5 KB (30462 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:6863809daf9e402b682da453c91e7185938f0fac786f388800cc7a8cf3b8d289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74994922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8119e3d5557f05e41ee5bb2b3fa590d09f007dc84be7814c6c3a4ca3e8831e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 15 Jan 2025 04:47:39 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 15 Jan 2025 04:47:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 21:26:01 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 21:26:03 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 21:25:59 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0774f657550ec6a831bbd0d72b777f8d8977a4143f082a39f86537a6691b415c`  
		Last Modified: Fri, 07 Feb 2025 22:27:36 GMT  
		Size: 31.7 MB (31677626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f93262ff5f92b789b5e28a5fbc8a229794cf568ee5c1a3fe803f21245857e1`  
		Last Modified: Fri, 07 Feb 2025 22:27:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc786a839d735394743a5eb5630ba3529273688ecfe8ce262710fb57014ae358`  
		Last Modified: Tue, 21 Jan 2025 23:32:26 GMT  
		Size: 1.3 MB (1298940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ebb543a3536234364dfb4e4f4f96fcd01a49e979f2f67b0139ff89ff2b57ab`  
		Last Modified: Tue, 21 Jan 2025 23:32:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166fc7a4788479b5d292be235658e3707989fa94ffe11ed54430db9af363ff1e`  
		Last Modified: Tue, 21 Jan 2025 23:32:26 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:913299d493026fe571d5cf8d6fe0ba8add58b3e772628edb3b01d2e4aa3e6aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78420dc46f8fc1c6b48d9ed023125a8721f0b854706bd09a4a6e26b537ae5420`

```dockerfile
```

-	Layers:
	-	`sha256:093bcd368cdec2123f7405acb7662a12b8326dbf53f1337e2151acfc9a5900f6`  
		Last Modified: Fri, 14 Feb 2025 05:13:49 GMT  
		Size: 2.2 MB (2155044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9eeb30a62a9c40790abbbe0c25e926fe456a612a454a88cfba32a411e345fb`  
		Last Modified: Fri, 14 Feb 2025 05:13:49 GMT  
		Size: 30.4 KB (30420 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:a2afe7a2f5bf47bbed994191ed96beb5d36af3e8f78c6268fbff13f0bcade52c
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
$ docker pull composer@sha256:89c78fda6439a73ea0fe55f5dacbc08c8721e7367cab185bb41b8e1e9d3ca652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77583081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bfe538f7b1771e7cb89600dc4fa2a392fa2a3d69d8f3c5cbb0cd875573fe43`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd2e180aa89ecb0845d1628b35579e1eb961f47975c3bc5a05ede5b6d47cb58`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 5.6 MB (5629137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d695b6cf2c8c3fcda26df544b054468a24be6cd41394db0208e3a333f18822f3`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7a3d474383ce078a67dbd96e1b61dc0d0b1fe673292ddc8d689e44c69655c2`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7370e670250547c9c1b145d13d02d6fa20bab3226e296408d9031c6a495186b6`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 13.6 MB (13609848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877e753ed32393f8eb06b7cf17507f31ab0f3db652e55c55ab86c82c3df4bf55`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d0fa737a71d88d348cb60ef0ff16ef4df36a45dddcd8bfe55e07d84f69a6a`  
		Last Modified: Fri, 14 Feb 2025 04:09:21 GMT  
		Size: 21.4 MB (21352652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf998db890f8e3ee8a94d02d3ea220e376efdd8371bffcc8379ce3ed9eee6e`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280727407916ee60ca49cf4ea07ef8f4b509704188598c3a99b973502ec133e3`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 20.1 KB (20058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d1ac227a2abc7451ff1ba44084161fdc97e0fd637a541506f29a6e04bd2617`  
		Last Modified: Fri, 14 Feb 2025 05:15:16 GMT  
		Size: 31.9 MB (31907430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26911d9a068609f04639f02836da2c8f3ffe7e740e2392cc7087732446bb7012`  
		Last Modified: Fri, 14 Feb 2025 05:15:14 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d2d59f49fd5f9ccbb78a72ac4061ac163a49203fd83856de27e769a96568dd`  
		Last Modified: Fri, 14 Feb 2025 05:15:16 GMT  
		Size: 1.4 MB (1417386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c4bdca85c0297d85aeaaa9acfbc142b0b6cdf89c35d060d82f47da0d553390`  
		Last Modified: Fri, 14 Feb 2025 05:15:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624f18a9bde02f497deb425a36d553c558471f355cba5653d43be83dd0e04e6a`  
		Last Modified: Fri, 14 Feb 2025 04:11:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:09c4adb5436b4530d27add05e4a5eadd0787da17926170aa3009e8addbdd0bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af42e342bfb0d0d385da9c3e1046f7e95f5b2c6a95e5c33e28a8f595062d357`

```dockerfile
```

-	Layers:
	-	`sha256:875494bec533267312793179ce376e5a54e9b9b6c71af43068480772cf8065eb`  
		Last Modified: Fri, 14 Feb 2025 05:13:35 GMT  
		Size: 2.2 MB (2157759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:862a21ebaa75a8534fa5226110f8353d8ca52a296c2ce1583d88b9a9d23d37d4`  
		Last Modified: Fri, 14 Feb 2025 05:13:35 GMT  
		Size: 30.4 KB (30420 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v6

```console
$ docker pull composer@sha256:a150485d52bfe0dddac59c11af2a759512ee9e3bf9ea23f5c7740f6d0213e0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75792714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9c79feb5ac9907bf09e52b98c076aa532a620159d2728e5cd5f4e446fd89a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 15 Jan 2025 01:25:26 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 15 Jan 2025 08:46:52 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 15 Jan 2025 08:46:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f6b305cd77dc6b597a3169970fd07b292703741539eaded2551c0d9a9a3ce2`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 13.6 MB (13609882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45767d1a2e12eb03ad18b9a7888cfb876903b7b27f5e22317a9a419e6c9357a4`  
		Last Modified: Fri, 14 Feb 2025 02:36:56 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b187df6e200be4ae6d666ab1d197a76dab384b63436f2df83f864d48fc6190f`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 22.4 MB (22402333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15e817c4c3f6223fc729a85f3b2dc3fa7ea9c2a3bf884f218dee6205043c6cf`  
		Last Modified: Fri, 14 Feb 2025 02:36:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45820a47f5394522a107e4a692c1e0d3689a29363793dbbf16751ed29bade6`  
		Last Modified: Fri, 14 Feb 2025 05:14:24 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07fdd9ff35b65c886cb11f76394f3a6058bcc6ffe163f41c4b09e0855ae0`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 31.6 MB (31601043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0554a9e2a4103b0bc17495a139a3314d3e4b40b4bc9ac6728a33ff747fe0226a`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b896ec9eaa77d9c05563e35253a48470aaae191c869961f4aeec44e6b1b6c888`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 1.5 MB (1490347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71788a201fd4484623058492eba6fc6241bfb6f5ca90f5eb131a2c29ec530377`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfd11890e74352f27cb92d1ca7523bdccc6e056291e507fc8d7cee80e3190c6`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:2d5a38cff7db945dc384c3c2fb8d9cdcab28ac49fb3a38448d64dbaaa2a6bea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988a18b5d47c028c68300ab40772f2201b839036c7c7403077d49c6fd58f660f`

```dockerfile
```

-	Layers:
	-	`sha256:36a53d4e8d65c6a567729d400b3ca0fe89e7adc8f96c1d230a6b7b59d6fdbf67`  
		Last Modified: Fri, 14 Feb 2025 05:13:37 GMT  
		Size: 30.3 KB (30299 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v7

```console
$ docker pull composer@sha256:71e98f991d1a52342ce89445c5e16b58c74117680e5b295dddf9a5e52626139b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69234309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34b176fa58957b0e7dbcf8e4fb1b298dd12b3c98705373773007ffdb0bb5de8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 15 Jan 2025 00:28:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 21:24:38 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 21:24:39 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 21:24:35 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b02f56cd79bb67b2e6a8c6a2926c13febe08627a14d51ac60cca77caa0bd9b`  
		Last Modified: Tue, 04 Feb 2025 15:48:01 GMT  
		Size: 30.2 MB (30150807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a36ded2ef8fef32700c53fb042e1d25e6c4b243e0eaa2fa4c9987aa4de12ad9`  
		Last Modified: Tue, 04 Feb 2025 16:45:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb36c56770ad29b53f6869471657e9474c199dfe3564967fd19ca11bd3366a5`  
		Last Modified: Wed, 05 Feb 2025 19:48:56 GMT  
		Size: 1.2 MB (1246037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b1e47e36ad2039a96855b35aa652d898b92a26e1c6c7eee5d4903e150c489a`  
		Last Modified: Mon, 03 Feb 2025 20:27:36 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d404a176f307405e948ed6b62f2968d8a5dd2fc85dbe2f21abee69cffbc415cf`  
		Last Modified: Wed, 05 Feb 2025 19:48:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:53e501cae7d9472a2a76988b1828f6aeb92e98e35c7f7312dd805c23cbeac79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05f81ae33c6783a9d1c2f6a35daee7ba87f8860e8bf10eb791c9dfba79b5ffc`

```dockerfile
```

-	Layers:
	-	`sha256:2c5f9f98bd06fe880dcc8314697b193b5fff605294579c76f03ec7a7e0a6f98d`  
		Last Modified: Fri, 14 Feb 2025 05:13:39 GMT  
		Size: 2.2 MB (2158075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:326b816a54e2dd57d56f53e0a264a2cab278b2d9bfb68c8d7fc3e702a801959d`  
		Last Modified: Fri, 14 Feb 2025 05:13:39 GMT  
		Size: 30.5 KB (30514 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:30c48973f0dd5e950d9795b36a9596cb28ec9f0bcac7bad860410be2632a1dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78862207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a57571662b820df3636935072533f5d98a59074e505d8051a533f7e79a9c19`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Tue, 14 Jan 2025 20:34:52 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Tue, 14 Jan 2025 20:34:51 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf60bd0bee7688614b1af07694e9e862a6e468345b4d8c1274b901e3308d850`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 13.6 MB (13609906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5935d74cc4f8900f9fe931cf198c384636eccfe5b27fcf8222bad1a34adc3c`  
		Last Modified: Fri, 14 Feb 2025 03:03:44 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3dd78614141a7cf92fd59b8e7fccf1f50faaef52fe4a0a661d5b0d846a4ea`  
		Last Modified: Fri, 14 Feb 2025 05:14:49 GMT  
		Size: 24.4 MB (24449108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eb61917bf0624ecf3420f926f6053b48728486c0188ada2088cb4c8939857e`  
		Last Modified: Fri, 14 Feb 2025 05:12:47 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc28a76fb7622bd8689c33b509f275a2d2558a77eccd18f266bc3ce660c7deb6`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7df60278df6c56d8ef9b2df595e68e15a33c291bf23b297f3ebb680a74161f`  
		Last Modified: Fri, 14 Feb 2025 05:14:54 GMT  
		Size: 32.0 MB (32009162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24085d57bfcbbba22355b95422cdf2ec94dde42b3fed500ec739e6f28f614030`  
		Last Modified: Fri, 14 Feb 2025 05:14:39 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb41014c418713cf7a78b82f17d137451b22af48c99c2d77553f985dce68f054`  
		Last Modified: Fri, 14 Feb 2025 05:26:09 GMT  
		Size: 1.4 MB (1449250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b05b997b07dc8f77af9151439c16c2ea8fad59e9b5d7cebebcf4cf115ed279`  
		Last Modified: Fri, 14 Feb 2025 05:26:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e11873c3cb1ffd7ec97c973f381f94a9ae954ace6058a427ac2c94d3651ee4`  
		Last Modified: Fri, 14 Feb 2025 05:26:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:d5285e5db7648af9bdf1839ab38bf3577cce0e63f80c3c000288ccbd35f311f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95033207bc5cf6917602de71a9a2516a141208aa093ab207198f0b1c732da2be`

```dockerfile
```

-	Layers:
	-	`sha256:b8590f554c9ce9740018238bd52fd812f6d6b2d17bb96ec92b697c65ba2eb75e`  
		Last Modified: Fri, 14 Feb 2025 05:13:41 GMT  
		Size: 2.2 MB (2157899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:029a72d217f5af38ed4d1cef16ec25fce065180721e6d388860d8add5cdc6c7b`  
		Last Modified: Fri, 14 Feb 2025 05:13:41 GMT  
		Size: 30.5 KB (30542 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; 386

```console
$ docker pull composer@sha256:8f635b56545810b2e999180caa9b9b55882af87e2e0c355b7bc418a48d743ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78283996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6781ff65f70b572fb67027f9371191874e980dda6602883aa0faf6efa20d2b0a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c4f61d7599e7869ad3a9d452f69e9bc3899f18d70701124026229667c57db`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 5.5 MB (5479161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb08d2bfa2365278e7427cd03c6a3b6d0d200bf048c31056c211ff6bd1d83e3f`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ccac1acad29397cc55b48dcff4f9ee2a1ad8bb562aefc4e7345e5ba177ea66`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77470d2cfb3c06673c0297f09fdcfd1debad3d8c75b8f08ee1be3f66d5edfb5`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 13.6 MB (13609860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56194a5a61ce8b305a5554d8aff3980c32fe8df11e9dae038a5c1169482a4dff`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb641c65fcb36b09714fd6d6634df4fa431b7f127829dd93eecb97dc6d4674`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 21.9 MB (21875599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8652ddf39bd8a77eabbc758325596a213cfa201e124d3a8e14c0d3fedbbe920a`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7c976ea7a0a95cb41a13dd1eff7887ba420c913603c766514f637eb3933a56`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd93bacb6d5493996f5c66c144f57c835b61ad61c616f85e4c67f05b4756999`  
		Last Modified: Fri, 14 Feb 2025 04:09:44 GMT  
		Size: 32.4 MB (32391482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307c85cb9cd140a46bbfe9a5836b595d4ac469d955bcf947e382f9caa5fc7084`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c094d28a1f3b8b49e3ebb8109fd30fd8bd4fc6d59ca6fdd66d7bf7e0744e6667`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 1.4 MB (1439842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de5cc60f8a748966dd208e96a6b39ea76dbb2cb0fb74e9d39beec1b0cc0e7de`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f4051ab2bc9b427dbc31f39e35232e46b7de196f743bdaa8cbae6e807bc3e`  
		Last Modified: Fri, 14 Feb 2025 05:08:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:3a37b4832b3ca9c9885c7d32b11ca53226593070d5ba3a5cedd85638a8863bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f44c4c1052cacf34fe16350b6b24e9c9a4057cb397a5582f3b486f738ff2fad`

```dockerfile
```

-	Layers:
	-	`sha256:85b79d12514157d042d80c216a35d436a1b96d8983ee819698f0ddb33d25106f`  
		Last Modified: Fri, 14 Feb 2025 05:13:43 GMT  
		Size: 2.2 MB (2157547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a948bea48791191572cbda7fc7e13ee352678e8ecacd68d72d85e65f36c45f02`  
		Last Modified: Fri, 14 Feb 2025 05:13:43 GMT  
		Size: 30.4 KB (30389 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; ppc64le

```console
$ docker pull composer@sha256:c97997e352275960898a3222f0db5c4be4294e6dd6d35a77f590ebc20cf11f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80515647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c83e5072d6a526ed37429ef262ce4b2356263e676e212d0857ab10ab9b6f12c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 15 Jan 2025 04:47:37 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704aa6bd4f8e770473b08a863515e74229b7563d9a2694d4dcffebd63189d5ab`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 13.6 MB (13609905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43c7e0504550dd35c7e6f3c1f5c61ed5db00067d11ffd3741e8f23b0dc16660`  
		Last Modified: Fri, 14 Feb 2025 05:09:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1167c96dbe49f246b96adc095a28edefcc2fe61bdc39108f8050c176699f483b`  
		Last Modified: Fri, 14 Feb 2025 02:47:38 GMT  
		Size: 25.4 MB (25398061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e16862c42f1028fedb8b04c6b22bd4e945a213a3e5a113872b385ee049f719`  
		Last Modified: Fri, 14 Feb 2025 05:10:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10f990e07f31e3d864671985a77e555905c511508a842be3262c8c7b9a96ec9`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 19.9 KB (19884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e260f2e53edd998f9cf2d3ba59929e4a7ff0f39075889a9b99dcb55b35732a9`  
		Last Modified: Fri, 14 Feb 2025 04:28:17 GMT  
		Size: 33.0 MB (32950697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717745514d5555d6812144710631aed2946af2ee5c721b80f8bf0a8b750bd43`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f754f264cd421594b8323374dfcfd9bf76077c4627c541bdb80a4730fb7a60`  
		Last Modified: Fri, 14 Feb 2025 04:29:09 GMT  
		Size: 1.5 MB (1482296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab08887a5d9bbd79a495e606d9d89e959eb261b577a23a2e519795ca9236961`  
		Last Modified: Fri, 14 Feb 2025 04:29:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3481825d9b4a4d2da079a340e064d36042cf1986b82fc42fff571e5570b42571`  
		Last Modified: Fri, 14 Feb 2025 04:29:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:747826bb6d6b8f04807ef15560e97c7da18cafda755fe1847f5ba4645ea7297f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98be37cede8e3d2663db85372a5bad03814548c5bcef46e23042098f208a5f8`

```dockerfile
```

-	Layers:
	-	`sha256:93b0cbeb6f16e9f7dca28274beba03229c4c02ddd8fae05584310d503ea4a08e`  
		Last Modified: Fri, 14 Feb 2025 05:13:45 GMT  
		Size: 2.2 MB (2156316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9272eec9108506c2f41df4ddda3e358ca5837fe37f986ae93b022abbb880c54a`  
		Last Modified: Fri, 14 Feb 2025 05:13:45 GMT  
		Size: 30.5 KB (30462 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; riscv64

```console
$ docker pull composer@sha256:c3c9f3482d12c572d589e18ef215c0f7e056bfb3ae124b8c726bea123adf9e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73035743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1464cc8f38a0eabd86c497babccc6353c206a5b1d55d1bfa83086d33eace4fde`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 15 Jan 2025 08:47:48 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 15 Jan 2025 03:01:25 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 15 Jan 2025 10:06:18 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 21:25:44 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 21:25:46 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 21:25:42 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df9d36d8de7098821c518291549b46c279424dc339b2da655e42c88a93a214e`  
		Last Modified: Mon, 10 Feb 2025 19:35:11 GMT  
		Size: 31.0 MB (31000989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e43f72402a8544ac8a8358f26a470e096d8b0a4416c1d930f95b5531cbe553`  
		Last Modified: Fri, 07 Feb 2025 22:27:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ca67f8caa2d3709c2cd2b7e7e9a7752581c0dceca488eff9d672f529ed5682`  
		Last Modified: Tue, 21 Jan 2025 23:38:21 GMT  
		Size: 1.3 MB (1290090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855f16e727d48ec3d7581bd9b6bee6db965d81ba5f16da020baac719ce5da371`  
		Last Modified: Tue, 21 Jan 2025 23:38:21 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b888ba3f844d59fc50dcf966337a42325158e35ea08647908a373dc882b5ce2`  
		Last Modified: Tue, 21 Jan 2025 23:38:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:fbe28f7c58d8937ed88b04bfe8c6899c96815c0084cffe96d7b3effe947f1789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8434e79d7f842819526fca445009ad56405ca86530dd22b451734252956e8aa0`

```dockerfile
```

-	Layers:
	-	`sha256:0c0560ab6b068394761652584993f47e1f0596a5b2948832e55fea64e75e4278`  
		Last Modified: Fri, 14 Feb 2025 05:13:47 GMT  
		Size: 2.2 MB (2155258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e50fa0e87f0c01f3a89e74c5a8fa1d999769548a7032982e7aeeb6b16ccb3ba`  
		Last Modified: Fri, 14 Feb 2025 05:13:47 GMT  
		Size: 30.5 KB (30462 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; s390x

```console
$ docker pull composer@sha256:6863809daf9e402b682da453c91e7185938f0fac786f388800cc7a8cf3b8d289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74994922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8119e3d5557f05e41ee5bb2b3fa590d09f007dc84be7814c6c3a4ca3e8831e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 15 Jan 2025 04:47:39 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 15 Jan 2025 04:47:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 21:26:01 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 21:26:03 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 21:25:59 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0774f657550ec6a831bbd0d72b777f8d8977a4143f082a39f86537a6691b415c`  
		Last Modified: Fri, 07 Feb 2025 22:27:36 GMT  
		Size: 31.7 MB (31677626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f93262ff5f92b789b5e28a5fbc8a229794cf568ee5c1a3fe803f21245857e1`  
		Last Modified: Fri, 07 Feb 2025 22:27:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc786a839d735394743a5eb5630ba3529273688ecfe8ce262710fb57014ae358`  
		Last Modified: Tue, 21 Jan 2025 23:32:26 GMT  
		Size: 1.3 MB (1298940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ebb543a3536234364dfb4e4f4f96fcd01a49e979f2f67b0139ff89ff2b57ab`  
		Last Modified: Tue, 21 Jan 2025 23:32:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166fc7a4788479b5d292be235658e3707989fa94ffe11ed54430db9af363ff1e`  
		Last Modified: Tue, 21 Jan 2025 23:32:26 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:913299d493026fe571d5cf8d6fe0ba8add58b3e772628edb3b01d2e4aa3e6aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78420dc46f8fc1c6b48d9ed023125a8721f0b854706bd09a4a6e26b537ae5420`

```dockerfile
```

-	Layers:
	-	`sha256:093bcd368cdec2123f7405acb7662a12b8326dbf53f1337e2151acfc9a5900f6`  
		Last Modified: Fri, 14 Feb 2025 05:13:49 GMT  
		Size: 2.2 MB (2155044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9eeb30a62a9c40790abbbe0c25e926fe456a612a454a88cfba32a411e345fb`  
		Last Modified: Fri, 14 Feb 2025 05:13:49 GMT  
		Size: 30.4 KB (30420 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:4e931c046b91c45dfadb9b00a7ffd540cc75e579700718c122450d0a22d4525a
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
$ docker pull composer@sha256:98c3dbf57e4159b38905f4b8c2814c1fc31e7462087f0329848d90df359eaaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77810713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdedb63128b75c5194577b44d938b7536cf1b39c47e7dce2f4d8f2eda01c0288`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd2e180aa89ecb0845d1628b35579e1eb961f47975c3bc5a05ede5b6d47cb58`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 5.6 MB (5629137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d695b6cf2c8c3fcda26df544b054468a24be6cd41394db0208e3a333f18822f3`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7a3d474383ce078a67dbd96e1b61dc0d0b1fe673292ddc8d689e44c69655c2`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7370e670250547c9c1b145d13d02d6fa20bab3226e296408d9031c6a495186b6`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 13.6 MB (13609848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877e753ed32393f8eb06b7cf17507f31ab0f3db652e55c55ab86c82c3df4bf55`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d0fa737a71d88d348cb60ef0ff16ef4df36a45dddcd8bfe55e07d84f69a6a`  
		Last Modified: Fri, 14 Feb 2025 04:09:21 GMT  
		Size: 21.4 MB (21352652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf998db890f8e3ee8a94d02d3ea220e376efdd8371bffcc8379ce3ed9eee6e`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280727407916ee60ca49cf4ea07ef8f4b509704188598c3a99b973502ec133e3`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 20.1 KB (20058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4a85286c44cd7ccfe425a6f93c7d0554dc42bbedacec0451d7bfd33c04b19f`  
		Last Modified: Fri, 14 Feb 2025 05:08:28 GMT  
		Size: 31.9 MB (31907453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d650030e45e31239c615919ce51e844144a1710157eab8b6d2c1d14231b2b04`  
		Last Modified: Fri, 14 Feb 2025 05:08:27 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33ba8f5460e6cfb8b7879005fdac9e3a232bd59cd576f65021db114a9c7a9d5`  
		Last Modified: Fri, 14 Feb 2025 05:08:26 GMT  
		Size: 1.6 MB (1644985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e1d6d950ac72d921b31aa38a9bd355a127e7e28383aa07cb7011e2744e9224`  
		Last Modified: Fri, 14 Feb 2025 05:08:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386be936fe6e1133d7e69972d64ac992c9941bf1c7bff9fc5d2a5bdaffb20452`  
		Last Modified: Fri, 14 Feb 2025 05:08:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:0722f68eb3a20f8db15be53fcc10b0b74bbbde583039272d7cb7acf4f5478408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a324644870e5d4ce9d68b379fb5c3253df720706ab3f074189c907254c6d0f`

```dockerfile
```

-	Layers:
	-	`sha256:3f69c0b6c741ae5e0e0a00b8e26516f95eeabe727b031359e0d8d79b5d130564`  
		Last Modified: Fri, 14 Feb 2025 05:13:58 GMT  
		Size: 2.2 MB (2159253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0039cc6ead448a857c25b5cf521d153b13478cced1fa26be93b5497905f28cd7`  
		Last Modified: Fri, 14 Feb 2025 05:13:59 GMT  
		Size: 30.7 KB (30710 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:7c0eaa29ce8bb36c4865ab49d91a70a201cf20dc88f2cb980dfc195e1365b3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76018343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580c3e1bae7598f5d0083008438223589d64b33c1780d81dbab29e50e80e6d6a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 15 Jan 2025 01:25:26 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 15 Jan 2025 08:46:52 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 15 Jan 2025 08:46:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f6b305cd77dc6b597a3169970fd07b292703741539eaded2551c0d9a9a3ce2`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 13.6 MB (13609882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45767d1a2e12eb03ad18b9a7888cfb876903b7b27f5e22317a9a419e6c9357a4`  
		Last Modified: Fri, 14 Feb 2025 02:36:56 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b187df6e200be4ae6d666ab1d197a76dab384b63436f2df83f864d48fc6190f`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 22.4 MB (22402333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15e817c4c3f6223fc729a85f3b2dc3fa7ea9c2a3bf884f218dee6205043c6cf`  
		Last Modified: Fri, 14 Feb 2025 02:36:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45820a47f5394522a107e4a692c1e0d3689a29363793dbbf16751ed29bade6`  
		Last Modified: Fri, 14 Feb 2025 05:14:24 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07fdd9ff35b65c886cb11f76394f3a6058bcc6ffe163f41c4b09e0855ae0`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 31.6 MB (31601043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0554a9e2a4103b0bc17495a139a3314d3e4b40b4bc9ac6728a33ff747fe0226a`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e83fb5e8622068c07f88d893f9d43182717a2f86103513c505fdf0ff4a733f`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 1.7 MB (1715966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e07fcb8f2908d1ea5b2f87eff807dea12a006b5de0d58af277c954b96f3aea`  
		Last Modified: Fri, 14 Feb 2025 05:09:29 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4ef668ae27cb0fd96e1c2056708e1a33f0ed030cf02a01af62d279000076d8`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:48e33a3a101e81bd492b82957c1c8eaf21a41b4d7b3a9a2c7e3db656e3936333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed27818420ff5f18b10d2c38849ef1903ef7be61a5e63cd703017196e3567a66`

```dockerfile
```

-	Layers:
	-	`sha256:c1b97655659ad1d250704281928f1212fbc8f9cee8ffe53d11e173cc72a1dfe2`  
		Last Modified: Fri, 14 Feb 2025 05:14:00 GMT  
		Size: 30.6 KB (30597 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:c0bc01156691c66e7911e95e38cc0131d5214505b8a95d765cc344f4827eed5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69464673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17134b2d5c1fdf6dac461ba4851cae923b1496e80506bc776363379193f0f20c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 15 Jan 2025 00:28:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 21:24:38 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 21:24:39 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 21:24:35 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b02f56cd79bb67b2e6a8c6a2926c13febe08627a14d51ac60cca77caa0bd9b`  
		Last Modified: Tue, 04 Feb 2025 15:48:01 GMT  
		Size: 30.2 MB (30150807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a36ded2ef8fef32700c53fb042e1d25e6c4b243e0eaa2fa4c9987aa4de12ad9`  
		Last Modified: Tue, 04 Feb 2025 16:45:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832eb27d7c64b0492c397833cc42d8260f45e451a55c853f598dd256b23548ea`  
		Last Modified: Wed, 05 Feb 2025 22:29:43 GMT  
		Size: 1.5 MB (1476391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1201604993e876f18b05ecf6abdff45d0476cf834899dbbe856643b481b76ce0`  
		Last Modified: Tue, 04 Feb 2025 11:24:02 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd458b10679ce2ec3630036a732d04eff3d74b07347c47634f74b21951aa4b0`  
		Last Modified: Wed, 05 Feb 2025 22:29:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:3e7d90af0511190788cb60baa68fc96ea1f82e2957ea0f116cc80bdb80e0321e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2badf45813c77ff22edcb9cd526bfffa5d475bc354124f0ebca3f11d6f90412`

```dockerfile
```

-	Layers:
	-	`sha256:ba4cc6b7c6aaee6213cd6f5d9409ec9fa1cc3e58446889c8c3b3b14aca8501da`  
		Last Modified: Fri, 07 Feb 2025 22:26:56 GMT  
		Size: 2.2 MB (2159577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d75f5f35b12b24b66c33e580aeca9cbf6b2c45b4a29f0326d9e718d9842e7d2`  
		Last Modified: Fri, 07 Feb 2025 22:26:56 GMT  
		Size: 30.8 KB (30812 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:5966e1cb67473a4f2a0eed9cec403084706fd11b05d558cf7856f5454e7c44a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79090094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571c134f609235f6475d296087830826b5dc471665429151fc8207155e7fab0a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Tue, 14 Jan 2025 20:34:52 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Tue, 14 Jan 2025 20:34:51 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf60bd0bee7688614b1af07694e9e862a6e468345b4d8c1274b901e3308d850`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 13.6 MB (13609906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5935d74cc4f8900f9fe931cf198c384636eccfe5b27fcf8222bad1a34adc3c`  
		Last Modified: Fri, 14 Feb 2025 03:03:44 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3dd78614141a7cf92fd59b8e7fccf1f50faaef52fe4a0a661d5b0d846a4ea`  
		Last Modified: Fri, 14 Feb 2025 05:14:49 GMT  
		Size: 24.4 MB (24449108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eb61917bf0624ecf3420f926f6053b48728486c0188ada2088cb4c8939857e`  
		Last Modified: Fri, 14 Feb 2025 05:12:47 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc28a76fb7622bd8689c33b509f275a2d2558a77eccd18f266bc3ce660c7deb6`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7df60278df6c56d8ef9b2df595e68e15a33c291bf23b297f3ebb680a74161f`  
		Last Modified: Fri, 14 Feb 2025 05:14:54 GMT  
		Size: 32.0 MB (32009162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24085d57bfcbbba22355b95422cdf2ec94dde42b3fed500ec739e6f28f614030`  
		Last Modified: Fri, 14 Feb 2025 05:14:39 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5780913f5327a65eaa08945878e133be406b2c997920b9bdc907ab9510f195d1`  
		Last Modified: Fri, 14 Feb 2025 05:14:47 GMT  
		Size: 1.7 MB (1677125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f15c3f82485f4525b92f91cb033d47c7a19bae4309fed26f3b5a1afb85b52`  
		Last Modified: Fri, 14 Feb 2025 05:12:50 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2520aed179c04104eeed784905fb04adcf98131bd84fcffc0f9c6c586b8096`  
		Last Modified: Fri, 14 Feb 2025 05:14:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:9030171990a9d8540de8c28915a0303bd98497a6dd28e236b41ccb1361383970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cba49e4a776da5d5e8cbfd4ba34a837adafaed41e63376cbc41b805a6e49be`

```dockerfile
```

-	Layers:
	-	`sha256:2d2ee95b8c9c2dadcb15898b1759559454a4f086bbe31a0b49407824c5e9e59e`  
		Last Modified: Fri, 14 Feb 2025 05:14:03 GMT  
		Size: 2.2 MB (2159405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5d0a7330c42062fe1edeb831cfc8b22a74c1d5bf81bcad0f3eeb008ce1bf07`  
		Last Modified: Fri, 14 Feb 2025 05:14:03 GMT  
		Size: 30.8 KB (30843 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:08355227fff4dd024f6581b8e4f8541e85e8d4b941238617fda2a17eaf813d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78509299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8332bfe7eb8d1a21458a7bd2a7297b4c6f3bd3484d40b55872e54d47d8011446`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c4f61d7599e7869ad3a9d452f69e9bc3899f18d70701124026229667c57db`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 5.5 MB (5479161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb08d2bfa2365278e7427cd03c6a3b6d0d200bf048c31056c211ff6bd1d83e3f`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ccac1acad29397cc55b48dcff4f9ee2a1ad8bb562aefc4e7345e5ba177ea66`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77470d2cfb3c06673c0297f09fdcfd1debad3d8c75b8f08ee1be3f66d5edfb5`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 13.6 MB (13609860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56194a5a61ce8b305a5554d8aff3980c32fe8df11e9dae038a5c1169482a4dff`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb641c65fcb36b09714fd6d6634df4fa431b7f127829dd93eecb97dc6d4674`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 21.9 MB (21875599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8652ddf39bd8a77eabbc758325596a213cfa201e124d3a8e14c0d3fedbbe920a`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7c976ea7a0a95cb41a13dd1eff7887ba420c913603c766514f637eb3933a56`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb6eafacb1f15fd12bd7bcf6493945cb15347ce13399873ee2a41fa97d49cff`  
		Last Modified: Fri, 14 Feb 2025 05:08:46 GMT  
		Size: 32.4 MB (32391459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97aaf4f7252c27f8cf968b89e5b0ecafcc390c2ef0d24ad4da6331436e6d82a7`  
		Last Modified: Fri, 14 Feb 2025 05:08:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356c18fd62985f302d2320070ad2ae27ffc266dd31376242baead03cdb4d843`  
		Last Modified: Fri, 14 Feb 2025 05:08:44 GMT  
		Size: 1.7 MB (1665158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30078a4cf8eb3b57398ebe7bdb98b7968f346e86e35c11f18f88f86b5627002f`  
		Last Modified: Fri, 14 Feb 2025 04:09:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f4051ab2bc9b427dbc31f39e35232e46b7de196f743bdaa8cbae6e807bc3e`  
		Last Modified: Fri, 14 Feb 2025 05:08:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:b82a57e8798a6cb97e0344644ffd81d80ae1c3af3ca150c3d29bd1421dc6a93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99298ea41039982ecee0dd21aadc4fa520b9e87f2178f5f23150a92357875db2`

```dockerfile
```

-	Layers:
	-	`sha256:1f211dc3f8e2a130cda31988f71789007d829d2b41e0f689d19dce4638397932`  
		Last Modified: Fri, 14 Feb 2025 05:14:05 GMT  
		Size: 2.2 MB (2159036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af56ea76f873f21852ad49dc4284d8b333f62f544cdbc528202a4344b04b51f8`  
		Last Modified: Fri, 14 Feb 2025 05:14:05 GMT  
		Size: 30.7 KB (30674 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:a09de83280ca038e135b44a4607d8389183c7fd0823a4032e310069333e59d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80744150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10d87b0a8782e3163fa9eea183f45888d8813ec516bde12da44f0e9a32a8239`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 15 Jan 2025 04:47:37 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704aa6bd4f8e770473b08a863515e74229b7563d9a2694d4dcffebd63189d5ab`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 13.6 MB (13609905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43c7e0504550dd35c7e6f3c1f5c61ed5db00067d11ffd3741e8f23b0dc16660`  
		Last Modified: Fri, 14 Feb 2025 05:09:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1167c96dbe49f246b96adc095a28edefcc2fe61bdc39108f8050c176699f483b`  
		Last Modified: Fri, 14 Feb 2025 02:47:38 GMT  
		Size: 25.4 MB (25398061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e16862c42f1028fedb8b04c6b22bd4e945a213a3e5a113872b385ee049f719`  
		Last Modified: Fri, 14 Feb 2025 05:10:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10f990e07f31e3d864671985a77e555905c511508a842be3262c8c7b9a96ec9`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 19.9 KB (19884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e260f2e53edd998f9cf2d3ba59929e4a7ff0f39075889a9b99dcb55b35732a9`  
		Last Modified: Fri, 14 Feb 2025 04:28:17 GMT  
		Size: 33.0 MB (32950697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717745514d5555d6812144710631aed2946af2ee5c721b80f8bf0a8b750bd43`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f14f9920e5bfe51f6d8808a523894518e858f697a3281f8e9517226ca0d5e13`  
		Last Modified: Fri, 14 Feb 2025 04:30:23 GMT  
		Size: 1.7 MB (1710788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7015ed3bdb11921234a436d525ca99e38f61a051eae27121d690c066c4c9236`  
		Last Modified: Fri, 14 Feb 2025 05:10:02 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992a149056344d183825544650b2929a59f83b5452c0fdd8fabf867596c0501e`  
		Last Modified: Fri, 14 Feb 2025 04:30:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:72c14f99f64f8fc43b543d46de0163d84b192d43146e499790ac387687816171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7089099d6b172fcdf57bc94469e526e42360d85acd4207ee0f7691b58bf22338`

```dockerfile
```

-	Layers:
	-	`sha256:90618ab6c2c49038e5501c01c4db3c116df47812a94026f3de986c1b6fe8b5a0`  
		Last Modified: Fri, 14 Feb 2025 05:14:07 GMT  
		Size: 2.2 MB (2157816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b38932949716320124314187b77759e67c643bebe1168bda822d1eb03eeb0112`  
		Last Modified: Fri, 14 Feb 2025 05:14:07 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:1251e7574e214e7b7022475238cc4527c28826e8c2c07204647735316cfd7c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73264136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e55cf7ec6b8902a45b5c36f9043f70f41816a7753d07438eb34fcabe2ff0eca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 15 Jan 2025 08:47:48 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 15 Jan 2025 03:01:25 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 15 Jan 2025 10:06:18 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 21:25:44 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 21:25:46 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 21:25:42 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df9d36d8de7098821c518291549b46c279424dc339b2da655e42c88a93a214e`  
		Last Modified: Mon, 10 Feb 2025 19:35:11 GMT  
		Size: 31.0 MB (31000989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e43f72402a8544ac8a8358f26a470e096d8b0a4416c1d930f95b5531cbe553`  
		Last Modified: Fri, 07 Feb 2025 22:27:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48910cdc7c38676ed7d29cd41f54ee4ed652c0aca4f5dc6fd36fc0ba57e72ce6`  
		Last Modified: Fri, 07 Feb 2025 22:27:31 GMT  
		Size: 1.5 MB (1518474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dac6612285e15c9017337237de7aaeea8529a6bf8e4525205f29f12a2fbb1b`  
		Last Modified: Mon, 10 Feb 2025 19:35:08 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756a5fae31e1504c538a672d57d4ff44b48aa821391488ebb9982cabb6e6ea1e`  
		Last Modified: Fri, 07 Feb 2025 22:27:33 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:f5e6f63e08366e67f549de343bf09f9d591a98753ec860b818f2fda598a53916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0135a1f3aa7c46d0b4c5cec112b52e3b13d708cfe8a49b8306621fb9cad4a4e3`

```dockerfile
```

-	Layers:
	-	`sha256:b079cd3d901a783779cda17e3e2b07831ee2ad8976830e6756e92eea5d81ef4b`  
		Last Modified: Mon, 10 Feb 2025 19:35:12 GMT  
		Size: 2.2 MB (2156758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c42dfd8576186600f64611749e8918fd7b70fd53a5ca693088199ba932473a`  
		Last Modified: Fri, 07 Feb 2025 22:27:33 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:3de176ce49537f78983acb45f370eec1465f56e0253789881ccd6d4dda1c7ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75221980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6d751203d1b8e3ed6e5c6905791abfa78579ba4daeb1b7e3d17f4ac45482ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 15 Jan 2025 04:47:39 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 15 Jan 2025 04:47:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 21:26:01 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 21:26:03 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 21:25:59 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0774f657550ec6a831bbd0d72b777f8d8977a4143f082a39f86537a6691b415c`  
		Last Modified: Fri, 07 Feb 2025 22:27:36 GMT  
		Size: 31.7 MB (31677626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f93262ff5f92b789b5e28a5fbc8a229794cf568ee5c1a3fe803f21245857e1`  
		Last Modified: Fri, 07 Feb 2025 22:27:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5621a0404c4346630297b77ccb90ad199ec5969a33b7cae2c363c4800af9f1`  
		Last Modified: Fri, 07 Feb 2025 14:50:22 GMT  
		Size: 1.5 MB (1525986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1201604993e876f18b05ecf6abdff45d0476cf834899dbbe856643b481b76ce0`  
		Last Modified: Tue, 04 Feb 2025 11:24:02 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b6314112280f82f9a8c69377889d4e36d84d4abd16495353f6c66167f17921`  
		Last Modified: Fri, 07 Feb 2025 22:27:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:9b8e5897e6a59e0262f3c8f7577aeb09cfe9a12c0555758adafd59c03838b005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104537f60dbca84d4e20fd79f14b37e49746c45e815c2ac6a909ce6f313987af`

```dockerfile
```

-	Layers:
	-	`sha256:dd79fd0604808059960a43f80aa3a7559a240f1818a73375ddd02b8bac73ea0b`  
		Last Modified: Fri, 07 Feb 2025 22:27:39 GMT  
		Size: 2.2 MB (2156538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8cc3506acaa83ed74f21f0a15ad7aec58699e896de7e0467599825de60d1358`  
		Last Modified: Mon, 10 Feb 2025 19:35:19 GMT  
		Size: 30.7 KB (30709 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:532a83f21938e68debf6efe20ef8852e3871478f3ac660dc5e2a6ac3ae35f6bd
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
$ docker pull composer@sha256:f0c4aa14d051615778cb4725e661a77798ef33527c85a645558ab311b5738afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77669012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5dbbf54b41745e4ee6205c3dfc9a63ccf51c15387ec9eca04ca8dfca900857`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd2e180aa89ecb0845d1628b35579e1eb961f47975c3bc5a05ede5b6d47cb58`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 5.6 MB (5629137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d695b6cf2c8c3fcda26df544b054468a24be6cd41394db0208e3a333f18822f3`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7a3d474383ce078a67dbd96e1b61dc0d0b1fe673292ddc8d689e44c69655c2`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7370e670250547c9c1b145d13d02d6fa20bab3226e296408d9031c6a495186b6`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 13.6 MB (13609848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877e753ed32393f8eb06b7cf17507f31ab0f3db652e55c55ab86c82c3df4bf55`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d0fa737a71d88d348cb60ef0ff16ef4df36a45dddcd8bfe55e07d84f69a6a`  
		Last Modified: Fri, 14 Feb 2025 04:09:21 GMT  
		Size: 21.4 MB (21352652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf998db890f8e3ee8a94d02d3ea220e376efdd8371bffcc8379ce3ed9eee6e`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280727407916ee60ca49cf4ea07ef8f4b509704188598c3a99b973502ec133e3`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 20.1 KB (20058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b2652210424f810ea67526bf4062b1a031c969b4f4c54ce1528605f2464fb3`  
		Last Modified: Fri, 14 Feb 2025 05:14:42 GMT  
		Size: 31.9 MB (31907474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2809196acc2a093ba933a0704d761289634b1c288685c331846b161047c7b8b9`  
		Last Modified: Fri, 14 Feb 2025 05:14:41 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f36432fc0ed7d14bddcc5646cec2b1a4235444a8e2a153e74ef66b1f8c07bce`  
		Last Modified: Fri, 14 Feb 2025 05:14:41 GMT  
		Size: 1.5 MB (1503263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a76d6110d4b8009bf12ad19b123915dbc8fc904b7807f53cd517e2828c2017c`  
		Last Modified: Fri, 14 Feb 2025 04:10:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a308aa26c90af5e9ab5ce1383dc8f8979d843bea9235b3686d4936b5500f3c46`  
		Last Modified: Fri, 14 Feb 2025 05:14:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:4f1dadd55e175019d7cc711173b386040bb8b2859bd746c9938db919c7d995d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea24f23da4df8cd4440549a9c6fb99274c0926e94db8753f310043c6ef45bf7`

```dockerfile
```

-	Layers:
	-	`sha256:af3877ad7e6f0510d91d1a90015586580cb1575eb6a6c0b42c39ee471d5ad5db`  
		Last Modified: Fri, 14 Feb 2025 05:14:19 GMT  
		Size: 2.2 MB (2158959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5862b4ee9f0ab5e70d59074f775367b3668ff1494fe3ce8b8df3c3be5486827c`  
		Last Modified: Fri, 14 Feb 2025 05:14:19 GMT  
		Size: 30.4 KB (30406 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:fd8cdedc4172e0957aba29baf887f821a48d0361c6c160379e04f4f6ddc28683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75878817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b343a1ac5a7156be409d4a847d9ff224d87a19234ff1bc58f507ea4aafc9d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 15 Jan 2025 01:25:26 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 15 Jan 2025 08:46:52 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 15 Jan 2025 08:46:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f6b305cd77dc6b597a3169970fd07b292703741539eaded2551c0d9a9a3ce2`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 13.6 MB (13609882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45767d1a2e12eb03ad18b9a7888cfb876903b7b27f5e22317a9a419e6c9357a4`  
		Last Modified: Fri, 14 Feb 2025 02:36:56 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b187df6e200be4ae6d666ab1d197a76dab384b63436f2df83f864d48fc6190f`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 22.4 MB (22402333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15e817c4c3f6223fc729a85f3b2dc3fa7ea9c2a3bf884f218dee6205043c6cf`  
		Last Modified: Fri, 14 Feb 2025 02:36:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45820a47f5394522a107e4a692c1e0d3689a29363793dbbf16751ed29bade6`  
		Last Modified: Fri, 14 Feb 2025 05:14:24 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07fdd9ff35b65c886cb11f76394f3a6058bcc6ffe163f41c4b09e0855ae0`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 31.6 MB (31601043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0554a9e2a4103b0bc17495a139a3314d3e4b40b4bc9ac6728a33ff747fe0226a`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2c6d22e6cb45ad8fe1e004994403d03184c67120c910fe417858670f6f2c44`  
		Last Modified: Fri, 14 Feb 2025 05:14:51 GMT  
		Size: 1.6 MB (1576438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99643eeadc4d99bb5e6a1301f4dc21f9e56d921ef5997336e27c86e87d0f9ecc`  
		Last Modified: Fri, 14 Feb 2025 05:14:51 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b676d253fd81445f66316f17638c8535f5f6e70b4bac3ebc82a2fac5ea8e42`  
		Last Modified: Fri, 14 Feb 2025 05:14:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:4afa1b5b0646a1e830a9c645095200552e09cc4de5c431dd1ce96b96cd433f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ad16d5a22c906e234ed6e72952e446422d345c669b0bf4828d82d2fcf3d08c`

```dockerfile
```

-	Layers:
	-	`sha256:57672a6d7573431a39531c673049efe82d0d61c33b76981b609ee01490ed71e7`  
		Last Modified: Fri, 14 Feb 2025 05:14:21 GMT  
		Size: 30.3 KB (30285 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:69262ed536c424bf35b643cc1218bd871f6cac924fa7bd336cb602b88de738db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69325138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ad888b3d1c457c7ae159a5e3c4f7416925809f872276700bcd435dca7e444f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 15 Jan 2025 00:28:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 21:24:38 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 21:24:39 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 21:24:35 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b02f56cd79bb67b2e6a8c6a2926c13febe08627a14d51ac60cca77caa0bd9b`  
		Last Modified: Tue, 04 Feb 2025 15:48:01 GMT  
		Size: 30.2 MB (30150807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a36ded2ef8fef32700c53fb042e1d25e6c4b243e0eaa2fa4c9987aa4de12ad9`  
		Last Modified: Tue, 04 Feb 2025 16:45:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8877520556df2c3c03fddc4c926da1061cc2bf6a1ed40860757b3fbc67043aab`  
		Last Modified: Tue, 21 Jan 2025 23:27:58 GMT  
		Size: 1.3 MB (1336858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4585a7c436930e2831d2f35f65ecc2b0fe98f70f8bf63d7a021e5d3dc038119b`  
		Last Modified: Tue, 21 Jan 2025 23:27:58 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c25a086e5da415d9eef81f7323ed71254509a257d27a35807dd779a852941d`  
		Last Modified: Tue, 21 Jan 2025 23:27:59 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:d4b78f6324390ee58fb4aa2856ba0e42e4fe4941c11e8c32b78c5665e61d7ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e11de3c0c6051bd089bee76130d9859f57ef90701d22d4024c443c55e6d973`

```dockerfile
```

-	Layers:
	-	`sha256:5d3c340a4b67be3704f9f08b01d9b8dfa9aa11dfcc9c489e675873bc190baa8a`  
		Last Modified: Fri, 14 Feb 2025 05:14:22 GMT  
		Size: 2.2 MB (2159275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d172b3fc0308d5d978f7250a8f84c1b2060da92060b6406e0cb6cde75c892a2c`  
		Last Modified: Fri, 14 Feb 2025 05:14:23 GMT  
		Size: 30.5 KB (30500 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:8206dde757aed98a686f4711ce738df19fba91095d7f839b49ef4221eca3c903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78947087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207ee801aafca6b6b728e0d87a301ead2a7d14f45b0b9ac6a903ca017929c3e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Tue, 14 Jan 2025 20:34:52 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Tue, 14 Jan 2025 20:34:51 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf60bd0bee7688614b1af07694e9e862a6e468345b4d8c1274b901e3308d850`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 13.6 MB (13609906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5935d74cc4f8900f9fe931cf198c384636eccfe5b27fcf8222bad1a34adc3c`  
		Last Modified: Fri, 14 Feb 2025 03:03:44 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3dd78614141a7cf92fd59b8e7fccf1f50faaef52fe4a0a661d5b0d846a4ea`  
		Last Modified: Fri, 14 Feb 2025 05:14:49 GMT  
		Size: 24.4 MB (24449108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eb61917bf0624ecf3420f926f6053b48728486c0188ada2088cb4c8939857e`  
		Last Modified: Fri, 14 Feb 2025 05:12:47 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc28a76fb7622bd8689c33b509f275a2d2558a77eccd18f266bc3ce660c7deb6`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7df60278df6c56d8ef9b2df595e68e15a33c291bf23b297f3ebb680a74161f`  
		Last Modified: Fri, 14 Feb 2025 05:14:54 GMT  
		Size: 32.0 MB (32009162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24085d57bfcbbba22355b95422cdf2ec94dde42b3fed500ec739e6f28f614030`  
		Last Modified: Fri, 14 Feb 2025 05:14:39 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48d27b78cc2eb4a63b29b6626fac324c0f6707164a18b71e55132f54ce24c9d`  
		Last Modified: Fri, 14 Feb 2025 05:20:56 GMT  
		Size: 1.5 MB (1534120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39627df935107010c348c87049d8237cececbdcda0872b9f5d8de2f3b0a37c13`  
		Last Modified: Fri, 14 Feb 2025 05:20:55 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516723aad7f0ef09c8c93c3992c06f09fab814707eb39d564dd12aeda395012f`  
		Last Modified: Fri, 14 Feb 2025 04:43:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:64f990ea8e8379f655a0307013a12b575d30075faab92c030d985298c62d7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2044753fcc5302e04179c5b25764062da71481a56268c93eaabd69e6b081aaf5`

```dockerfile
```

-	Layers:
	-	`sha256:6a92b3addaccbf42e9455a86fa2b8fa606629bcbf42aa3246dbe97cb5885704c`  
		Last Modified: Fri, 14 Feb 2025 05:14:24 GMT  
		Size: 2.2 MB (2159099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cab56e06cacf87bbb81ee2af9cb52a26600ac8ca68546972b3a26e538fcaaa89`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 30.5 KB (30528 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:999c0084291ba62f0f8ca4bbf1e7baa7575140d15953f831d5a1fd1c0ebdee5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78369510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5ec57258189923eb3156405638275f1e0a7891710f0fbb132e988b4d81e017`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c4f61d7599e7869ad3a9d452f69e9bc3899f18d70701124026229667c57db`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 5.5 MB (5479161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb08d2bfa2365278e7427cd03c6a3b6d0d200bf048c31056c211ff6bd1d83e3f`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ccac1acad29397cc55b48dcff4f9ee2a1ad8bb562aefc4e7345e5ba177ea66`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77470d2cfb3c06673c0297f09fdcfd1debad3d8c75b8f08ee1be3f66d5edfb5`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 13.6 MB (13609860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56194a5a61ce8b305a5554d8aff3980c32fe8df11e9dae038a5c1169482a4dff`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb641c65fcb36b09714fd6d6634df4fa431b7f127829dd93eecb97dc6d4674`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 21.9 MB (21875599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8652ddf39bd8a77eabbc758325596a213cfa201e124d3a8e14c0d3fedbbe920a`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7c976ea7a0a95cb41a13dd1eff7887ba420c913603c766514f637eb3933a56`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4c75ab9d6ee0dfba786eef4b37c96f36b47af6393fc9f1ad54103fd0a0401`  
		Last Modified: Fri, 14 Feb 2025 04:09:44 GMT  
		Size: 32.4 MB (32391404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307c85cb9cd140a46bbfe9a5836b595d4ac469d955bcf947e382f9caa5fc7084`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db737518c7a1321b9524cc0c806f0209cf67adcb9fcc4b7217276cbc11757dae`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 1.5 MB (1525424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30078a4cf8eb3b57398ebe7bdb98b7968f346e86e35c11f18f88f86b5627002f`  
		Last Modified: Fri, 14 Feb 2025 04:09:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f4051ab2bc9b427dbc31f39e35232e46b7de196f743bdaa8cbae6e807bc3e`  
		Last Modified: Fri, 14 Feb 2025 05:08:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:714c86b48fc46c11adcbc3be0a341f67988e1926c3bf1ab2a7db467b8ec8da06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c187481d326d5839a57ecdd6925a20fb3453363b9a625e05a7ae18436fb24a3`

```dockerfile
```

-	Layers:
	-	`sha256:c23283967f31fbb19c6378629aa097894d319272ca50bb5fd3b31053706f695e`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 2.2 MB (2158747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfa1bcb19012e00c05e5045b17ccc615bf33c5d0aa49d1ba0c21f7aa8336ee4`  
		Last Modified: Fri, 14 Feb 2025 05:14:27 GMT  
		Size: 30.4 KB (30375 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:743027019d96c877d84aa61c5ce7aef783fd026f77eda0a166fc75522ffcf5ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80605406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c38d47056d72c55662503db96ff53dd2305b537d0431d9ed36cac6409de427`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 15 Jan 2025 04:47:37 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704aa6bd4f8e770473b08a863515e74229b7563d9a2694d4dcffebd63189d5ab`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 13.6 MB (13609905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43c7e0504550dd35c7e6f3c1f5c61ed5db00067d11ffd3741e8f23b0dc16660`  
		Last Modified: Fri, 14 Feb 2025 05:09:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1167c96dbe49f246b96adc095a28edefcc2fe61bdc39108f8050c176699f483b`  
		Last Modified: Fri, 14 Feb 2025 02:47:38 GMT  
		Size: 25.4 MB (25398061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e16862c42f1028fedb8b04c6b22bd4e945a213a3e5a113872b385ee049f719`  
		Last Modified: Fri, 14 Feb 2025 05:10:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10f990e07f31e3d864671985a77e555905c511508a842be3262c8c7b9a96ec9`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 19.9 KB (19884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e260f2e53edd998f9cf2d3ba59929e4a7ff0f39075889a9b99dcb55b35732a9`  
		Last Modified: Fri, 14 Feb 2025 04:28:17 GMT  
		Size: 33.0 MB (32950697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717745514d5555d6812144710631aed2946af2ee5c721b80f8bf0a8b750bd43`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839b07734abbe604a248264e5a9a2d440af3d7f32c9f2928a57847906c8be3ef`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 1.6 MB (1572043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5aa094a9e0da1a27d70cf9067c5ffbf2326afb56c6fa64619136b6a617abf49`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221496d3f16797dd0e2ba7577369c12f200df6ab91b13afc68e0ed7d2e163c96`  
		Last Modified: Fri, 14 Feb 2025 04:28:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:68f0a3d147944d967eb5dee4bfc61d87b40bec3ed6de9f85b95315fd0dcad507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5638e372becc7a921458207568a965b1410ce28fab67b76a96d6f21de2cecbb5`

```dockerfile
```

-	Layers:
	-	`sha256:a679d6f0d86afde37505cbf319062251c0020159c4478c42a816e86c60428ce6`  
		Last Modified: Fri, 14 Feb 2025 05:14:28 GMT  
		Size: 2.2 MB (2157516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc9e965651ca366ccba635569d99334889804e89c90ca37dc792085a67f4b4b`  
		Last Modified: Fri, 14 Feb 2025 05:14:29 GMT  
		Size: 30.4 KB (30448 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:764fe74ca6e879974d10f5b7d3af8beec53548826daddd27e610ae6c42fa19a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73124201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f54e3c0524d785db83b0e4d4801888c184dae4f032d625ca54dce9c63d39c76`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 15 Jan 2025 08:47:48 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 15 Jan 2025 03:01:25 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 15 Jan 2025 10:06:18 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 21:25:44 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 21:25:46 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 21:25:42 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df9d36d8de7098821c518291549b46c279424dc339b2da655e42c88a93a214e`  
		Last Modified: Mon, 10 Feb 2025 19:35:11 GMT  
		Size: 31.0 MB (31000989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e43f72402a8544ac8a8358f26a470e096d8b0a4416c1d930f95b5531cbe553`  
		Last Modified: Fri, 07 Feb 2025 22:27:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da46c3558a85c68b99a1fd16fe1d5e2df313e50486a17d6664eeb9f16ee7ec62`  
		Last Modified: Tue, 21 Jan 2025 23:33:06 GMT  
		Size: 1.4 MB (1378538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282976d95725176508cc2d12b9917b3a676652d8968c63950552f9ed28c2bf10`  
		Last Modified: Tue, 21 Jan 2025 23:33:05 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6827e80ba34f5e7edde2644e1d74019eb42d77685533efb9933bae5de735a14`  
		Last Modified: Tue, 21 Jan 2025 23:33:06 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:897867ea4f27a79d5dde711f6cf259e7a9e6427c72fc4c1afd434182e6dc4bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bc3fe69a3f94ef5f84b8f3c09aa0c99c01966b85836048a8decf8937d27d8b`

```dockerfile
```

-	Layers:
	-	`sha256:6a9105a5b44ae05153ca58d6957c944756b462378ee992f30d257ca4fc574a83`  
		Last Modified: Fri, 14 Feb 2025 05:14:30 GMT  
		Size: 2.2 MB (2156458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8392c83bb5ca74ac2536da484f476060e0576df4291fcf2a36506693e7c16abb`  
		Last Modified: Fri, 14 Feb 2025 05:14:30 GMT  
		Size: 30.4 KB (30448 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:514b1702cd4a4e313e68efb932d1a34e62b5c54c49f0c2465c5dc7fce4994a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf86f0e4de62e927c746bd82826435184b467d536480050009788ae69f9a9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 15 Jan 2025 04:47:39 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 15 Jan 2025 04:47:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 21:26:01 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 21:26:03 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 21:25:59 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0774f657550ec6a831bbd0d72b777f8d8977a4143f082a39f86537a6691b415c`  
		Last Modified: Fri, 07 Feb 2025 22:27:36 GMT  
		Size: 31.7 MB (31677626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f93262ff5f92b789b5e28a5fbc8a229794cf568ee5c1a3fe803f21245857e1`  
		Last Modified: Fri, 07 Feb 2025 22:27:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9b2a0bbea2bb78104414d4305d0086cf64327d3c0a3ac678ac07b3d8afcc7a`  
		Last Modified: Tue, 21 Jan 2025 23:28:29 GMT  
		Size: 1.4 MB (1383351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3588ec3a1e72affeaac950ef30c1d99805230b13e773b9aef96652b945fa2141`  
		Last Modified: Tue, 21 Jan 2025 23:28:29 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b453745dccd0fecb39882a5afda7d8b34c942c7048c521a6513882466445da`  
		Last Modified: Tue, 21 Jan 2025 23:28:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:4fb4eaf35b8643843c6417cae1d72c654de0fbe0df2b7de4035367e4a39a4ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae841eb0ef743268cf2abb58eff2284437ad4a7923cb5f07dc868333bc2ac15`

```dockerfile
```

-	Layers:
	-	`sha256:f2f0d9b799b6bc8b7b0408409d0c4c0472e83ee8a40d324f34f5ae17c2fecd2e`  
		Last Modified: Fri, 14 Feb 2025 05:14:32 GMT  
		Size: 2.2 MB (2156244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be5f436ba87454a77d39c8729483d37c276b96306136d5cd9081d576dc12dae7`  
		Last Modified: Fri, 14 Feb 2025 05:14:32 GMT  
		Size: 30.4 KB (30406 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.25`

```console
$ docker pull composer@sha256:532a83f21938e68debf6efe20ef8852e3871478f3ac660dc5e2a6ac3ae35f6bd
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
$ docker pull composer@sha256:f0c4aa14d051615778cb4725e661a77798ef33527c85a645558ab311b5738afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77669012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5dbbf54b41745e4ee6205c3dfc9a63ccf51c15387ec9eca04ca8dfca900857`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd2e180aa89ecb0845d1628b35579e1eb961f47975c3bc5a05ede5b6d47cb58`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 5.6 MB (5629137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d695b6cf2c8c3fcda26df544b054468a24be6cd41394db0208e3a333f18822f3`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7a3d474383ce078a67dbd96e1b61dc0d0b1fe673292ddc8d689e44c69655c2`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7370e670250547c9c1b145d13d02d6fa20bab3226e296408d9031c6a495186b6`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 13.6 MB (13609848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877e753ed32393f8eb06b7cf17507f31ab0f3db652e55c55ab86c82c3df4bf55`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d0fa737a71d88d348cb60ef0ff16ef4df36a45dddcd8bfe55e07d84f69a6a`  
		Last Modified: Fri, 14 Feb 2025 04:09:21 GMT  
		Size: 21.4 MB (21352652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf998db890f8e3ee8a94d02d3ea220e376efdd8371bffcc8379ce3ed9eee6e`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280727407916ee60ca49cf4ea07ef8f4b509704188598c3a99b973502ec133e3`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 20.1 KB (20058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b2652210424f810ea67526bf4062b1a031c969b4f4c54ce1528605f2464fb3`  
		Last Modified: Fri, 14 Feb 2025 05:14:42 GMT  
		Size: 31.9 MB (31907474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2809196acc2a093ba933a0704d761289634b1c288685c331846b161047c7b8b9`  
		Last Modified: Fri, 14 Feb 2025 05:14:41 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f36432fc0ed7d14bddcc5646cec2b1a4235444a8e2a153e74ef66b1f8c07bce`  
		Last Modified: Fri, 14 Feb 2025 05:14:41 GMT  
		Size: 1.5 MB (1503263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a76d6110d4b8009bf12ad19b123915dbc8fc904b7807f53cd517e2828c2017c`  
		Last Modified: Fri, 14 Feb 2025 04:10:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a308aa26c90af5e9ab5ce1383dc8f8979d843bea9235b3686d4936b5500f3c46`  
		Last Modified: Fri, 14 Feb 2025 05:14:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:4f1dadd55e175019d7cc711173b386040bb8b2859bd746c9938db919c7d995d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea24f23da4df8cd4440549a9c6fb99274c0926e94db8753f310043c6ef45bf7`

```dockerfile
```

-	Layers:
	-	`sha256:af3877ad7e6f0510d91d1a90015586580cb1575eb6a6c0b42c39ee471d5ad5db`  
		Last Modified: Fri, 14 Feb 2025 05:14:19 GMT  
		Size: 2.2 MB (2158959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5862b4ee9f0ab5e70d59074f775367b3668ff1494fe3ce8b8df3c3be5486827c`  
		Last Modified: Fri, 14 Feb 2025 05:14:19 GMT  
		Size: 30.4 KB (30406 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v6

```console
$ docker pull composer@sha256:fd8cdedc4172e0957aba29baf887f821a48d0361c6c160379e04f4f6ddc28683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75878817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b343a1ac5a7156be409d4a847d9ff224d87a19234ff1bc58f507ea4aafc9d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 15 Jan 2025 01:25:26 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 15 Jan 2025 08:46:52 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 15 Jan 2025 08:46:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f6b305cd77dc6b597a3169970fd07b292703741539eaded2551c0d9a9a3ce2`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 13.6 MB (13609882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45767d1a2e12eb03ad18b9a7888cfb876903b7b27f5e22317a9a419e6c9357a4`  
		Last Modified: Fri, 14 Feb 2025 02:36:56 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b187df6e200be4ae6d666ab1d197a76dab384b63436f2df83f864d48fc6190f`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 22.4 MB (22402333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15e817c4c3f6223fc729a85f3b2dc3fa7ea9c2a3bf884f218dee6205043c6cf`  
		Last Modified: Fri, 14 Feb 2025 02:36:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45820a47f5394522a107e4a692c1e0d3689a29363793dbbf16751ed29bade6`  
		Last Modified: Fri, 14 Feb 2025 05:14:24 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07fdd9ff35b65c886cb11f76394f3a6058bcc6ffe163f41c4b09e0855ae0`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 31.6 MB (31601043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0554a9e2a4103b0bc17495a139a3314d3e4b40b4bc9ac6728a33ff747fe0226a`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2c6d22e6cb45ad8fe1e004994403d03184c67120c910fe417858670f6f2c44`  
		Last Modified: Fri, 14 Feb 2025 05:14:51 GMT  
		Size: 1.6 MB (1576438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99643eeadc4d99bb5e6a1301f4dc21f9e56d921ef5997336e27c86e87d0f9ecc`  
		Last Modified: Fri, 14 Feb 2025 05:14:51 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b676d253fd81445f66316f17638c8535f5f6e70b4bac3ebc82a2fac5ea8e42`  
		Last Modified: Fri, 14 Feb 2025 05:14:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:4afa1b5b0646a1e830a9c645095200552e09cc4de5c431dd1ce96b96cd433f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ad16d5a22c906e234ed6e72952e446422d345c669b0bf4828d82d2fcf3d08c`

```dockerfile
```

-	Layers:
	-	`sha256:57672a6d7573431a39531c673049efe82d0d61c33b76981b609ee01490ed71e7`  
		Last Modified: Fri, 14 Feb 2025 05:14:21 GMT  
		Size: 30.3 KB (30285 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v7

```console
$ docker pull composer@sha256:69262ed536c424bf35b643cc1218bd871f6cac924fa7bd336cb602b88de738db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69325138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ad888b3d1c457c7ae159a5e3c4f7416925809f872276700bcd435dca7e444f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 15 Jan 2025 00:28:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 21:24:38 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 21:24:39 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 21:24:35 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b02f56cd79bb67b2e6a8c6a2926c13febe08627a14d51ac60cca77caa0bd9b`  
		Last Modified: Tue, 04 Feb 2025 15:48:01 GMT  
		Size: 30.2 MB (30150807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a36ded2ef8fef32700c53fb042e1d25e6c4b243e0eaa2fa4c9987aa4de12ad9`  
		Last Modified: Tue, 04 Feb 2025 16:45:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8877520556df2c3c03fddc4c926da1061cc2bf6a1ed40860757b3fbc67043aab`  
		Last Modified: Tue, 21 Jan 2025 23:27:58 GMT  
		Size: 1.3 MB (1336858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4585a7c436930e2831d2f35f65ecc2b0fe98f70f8bf63d7a021e5d3dc038119b`  
		Last Modified: Tue, 21 Jan 2025 23:27:58 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c25a086e5da415d9eef81f7323ed71254509a257d27a35807dd779a852941d`  
		Last Modified: Tue, 21 Jan 2025 23:27:59 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:d4b78f6324390ee58fb4aa2856ba0e42e4fe4941c11e8c32b78c5665e61d7ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e11de3c0c6051bd089bee76130d9859f57ef90701d22d4024c443c55e6d973`

```dockerfile
```

-	Layers:
	-	`sha256:5d3c340a4b67be3704f9f08b01d9b8dfa9aa11dfcc9c489e675873bc190baa8a`  
		Last Modified: Fri, 14 Feb 2025 05:14:22 GMT  
		Size: 2.2 MB (2159275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d172b3fc0308d5d978f7250a8f84c1b2060da92060b6406e0cb6cde75c892a2c`  
		Last Modified: Fri, 14 Feb 2025 05:14:23 GMT  
		Size: 30.5 KB (30500 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:8206dde757aed98a686f4711ce738df19fba91095d7f839b49ef4221eca3c903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78947087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207ee801aafca6b6b728e0d87a301ead2a7d14f45b0b9ac6a903ca017929c3e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Tue, 14 Jan 2025 20:34:52 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Tue, 14 Jan 2025 20:34:51 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf60bd0bee7688614b1af07694e9e862a6e468345b4d8c1274b901e3308d850`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 13.6 MB (13609906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5935d74cc4f8900f9fe931cf198c384636eccfe5b27fcf8222bad1a34adc3c`  
		Last Modified: Fri, 14 Feb 2025 03:03:44 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3dd78614141a7cf92fd59b8e7fccf1f50faaef52fe4a0a661d5b0d846a4ea`  
		Last Modified: Fri, 14 Feb 2025 05:14:49 GMT  
		Size: 24.4 MB (24449108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eb61917bf0624ecf3420f926f6053b48728486c0188ada2088cb4c8939857e`  
		Last Modified: Fri, 14 Feb 2025 05:12:47 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc28a76fb7622bd8689c33b509f275a2d2558a77eccd18f266bc3ce660c7deb6`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7df60278df6c56d8ef9b2df595e68e15a33c291bf23b297f3ebb680a74161f`  
		Last Modified: Fri, 14 Feb 2025 05:14:54 GMT  
		Size: 32.0 MB (32009162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24085d57bfcbbba22355b95422cdf2ec94dde42b3fed500ec739e6f28f614030`  
		Last Modified: Fri, 14 Feb 2025 05:14:39 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48d27b78cc2eb4a63b29b6626fac324c0f6707164a18b71e55132f54ce24c9d`  
		Last Modified: Fri, 14 Feb 2025 05:20:56 GMT  
		Size: 1.5 MB (1534120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39627df935107010c348c87049d8237cececbdcda0872b9f5d8de2f3b0a37c13`  
		Last Modified: Fri, 14 Feb 2025 05:20:55 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516723aad7f0ef09c8c93c3992c06f09fab814707eb39d564dd12aeda395012f`  
		Last Modified: Fri, 14 Feb 2025 04:43:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:64f990ea8e8379f655a0307013a12b575d30075faab92c030d985298c62d7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2044753fcc5302e04179c5b25764062da71481a56268c93eaabd69e6b081aaf5`

```dockerfile
```

-	Layers:
	-	`sha256:6a92b3addaccbf42e9455a86fa2b8fa606629bcbf42aa3246dbe97cb5885704c`  
		Last Modified: Fri, 14 Feb 2025 05:14:24 GMT  
		Size: 2.2 MB (2159099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cab56e06cacf87bbb81ee2af9cb52a26600ac8ca68546972b3a26e538fcaaa89`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 30.5 KB (30528 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; 386

```console
$ docker pull composer@sha256:999c0084291ba62f0f8ca4bbf1e7baa7575140d15953f831d5a1fd1c0ebdee5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78369510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5ec57258189923eb3156405638275f1e0a7891710f0fbb132e988b4d81e017`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c4f61d7599e7869ad3a9d452f69e9bc3899f18d70701124026229667c57db`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 5.5 MB (5479161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb08d2bfa2365278e7427cd03c6a3b6d0d200bf048c31056c211ff6bd1d83e3f`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ccac1acad29397cc55b48dcff4f9ee2a1ad8bb562aefc4e7345e5ba177ea66`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77470d2cfb3c06673c0297f09fdcfd1debad3d8c75b8f08ee1be3f66d5edfb5`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 13.6 MB (13609860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56194a5a61ce8b305a5554d8aff3980c32fe8df11e9dae038a5c1169482a4dff`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb641c65fcb36b09714fd6d6634df4fa431b7f127829dd93eecb97dc6d4674`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 21.9 MB (21875599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8652ddf39bd8a77eabbc758325596a213cfa201e124d3a8e14c0d3fedbbe920a`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7c976ea7a0a95cb41a13dd1eff7887ba420c913603c766514f637eb3933a56`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4c75ab9d6ee0dfba786eef4b37c96f36b47af6393fc9f1ad54103fd0a0401`  
		Last Modified: Fri, 14 Feb 2025 04:09:44 GMT  
		Size: 32.4 MB (32391404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307c85cb9cd140a46bbfe9a5836b595d4ac469d955bcf947e382f9caa5fc7084`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db737518c7a1321b9524cc0c806f0209cf67adcb9fcc4b7217276cbc11757dae`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 1.5 MB (1525424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30078a4cf8eb3b57398ebe7bdb98b7968f346e86e35c11f18f88f86b5627002f`  
		Last Modified: Fri, 14 Feb 2025 04:09:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f4051ab2bc9b427dbc31f39e35232e46b7de196f743bdaa8cbae6e807bc3e`  
		Last Modified: Fri, 14 Feb 2025 05:08:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:714c86b48fc46c11adcbc3be0a341f67988e1926c3bf1ab2a7db467b8ec8da06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c187481d326d5839a57ecdd6925a20fb3453363b9a625e05a7ae18436fb24a3`

```dockerfile
```

-	Layers:
	-	`sha256:c23283967f31fbb19c6378629aa097894d319272ca50bb5fd3b31053706f695e`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 2.2 MB (2158747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfa1bcb19012e00c05e5045b17ccc615bf33c5d0aa49d1ba0c21f7aa8336ee4`  
		Last Modified: Fri, 14 Feb 2025 05:14:27 GMT  
		Size: 30.4 KB (30375 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; ppc64le

```console
$ docker pull composer@sha256:743027019d96c877d84aa61c5ce7aef783fd026f77eda0a166fc75522ffcf5ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80605406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c38d47056d72c55662503db96ff53dd2305b537d0431d9ed36cac6409de427`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 15 Jan 2025 04:47:37 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704aa6bd4f8e770473b08a863515e74229b7563d9a2694d4dcffebd63189d5ab`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 13.6 MB (13609905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43c7e0504550dd35c7e6f3c1f5c61ed5db00067d11ffd3741e8f23b0dc16660`  
		Last Modified: Fri, 14 Feb 2025 05:09:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1167c96dbe49f246b96adc095a28edefcc2fe61bdc39108f8050c176699f483b`  
		Last Modified: Fri, 14 Feb 2025 02:47:38 GMT  
		Size: 25.4 MB (25398061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e16862c42f1028fedb8b04c6b22bd4e945a213a3e5a113872b385ee049f719`  
		Last Modified: Fri, 14 Feb 2025 05:10:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10f990e07f31e3d864671985a77e555905c511508a842be3262c8c7b9a96ec9`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 19.9 KB (19884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e260f2e53edd998f9cf2d3ba59929e4a7ff0f39075889a9b99dcb55b35732a9`  
		Last Modified: Fri, 14 Feb 2025 04:28:17 GMT  
		Size: 33.0 MB (32950697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717745514d5555d6812144710631aed2946af2ee5c721b80f8bf0a8b750bd43`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839b07734abbe604a248264e5a9a2d440af3d7f32c9f2928a57847906c8be3ef`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 1.6 MB (1572043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5aa094a9e0da1a27d70cf9067c5ffbf2326afb56c6fa64619136b6a617abf49`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221496d3f16797dd0e2ba7577369c12f200df6ab91b13afc68e0ed7d2e163c96`  
		Last Modified: Fri, 14 Feb 2025 04:28:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:68f0a3d147944d967eb5dee4bfc61d87b40bec3ed6de9f85b95315fd0dcad507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5638e372becc7a921458207568a965b1410ce28fab67b76a96d6f21de2cecbb5`

```dockerfile
```

-	Layers:
	-	`sha256:a679d6f0d86afde37505cbf319062251c0020159c4478c42a816e86c60428ce6`  
		Last Modified: Fri, 14 Feb 2025 05:14:28 GMT  
		Size: 2.2 MB (2157516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc9e965651ca366ccba635569d99334889804e89c90ca37dc792085a67f4b4b`  
		Last Modified: Fri, 14 Feb 2025 05:14:29 GMT  
		Size: 30.4 KB (30448 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; riscv64

```console
$ docker pull composer@sha256:764fe74ca6e879974d10f5b7d3af8beec53548826daddd27e610ae6c42fa19a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73124201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f54e3c0524d785db83b0e4d4801888c184dae4f032d625ca54dce9c63d39c76`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 15 Jan 2025 08:47:48 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 15 Jan 2025 03:01:25 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 15 Jan 2025 10:06:18 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 21:25:44 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 21:25:46 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 21:25:42 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df9d36d8de7098821c518291549b46c279424dc339b2da655e42c88a93a214e`  
		Last Modified: Mon, 10 Feb 2025 19:35:11 GMT  
		Size: 31.0 MB (31000989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e43f72402a8544ac8a8358f26a470e096d8b0a4416c1d930f95b5531cbe553`  
		Last Modified: Fri, 07 Feb 2025 22:27:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da46c3558a85c68b99a1fd16fe1d5e2df313e50486a17d6664eeb9f16ee7ec62`  
		Last Modified: Tue, 21 Jan 2025 23:33:06 GMT  
		Size: 1.4 MB (1378538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282976d95725176508cc2d12b9917b3a676652d8968c63950552f9ed28c2bf10`  
		Last Modified: Tue, 21 Jan 2025 23:33:05 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6827e80ba34f5e7edde2644e1d74019eb42d77685533efb9933bae5de735a14`  
		Last Modified: Tue, 21 Jan 2025 23:33:06 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:897867ea4f27a79d5dde711f6cf259e7a9e6427c72fc4c1afd434182e6dc4bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bc3fe69a3f94ef5f84b8f3c09aa0c99c01966b85836048a8decf8937d27d8b`

```dockerfile
```

-	Layers:
	-	`sha256:6a9105a5b44ae05153ca58d6957c944756b462378ee992f30d257ca4fc574a83`  
		Last Modified: Fri, 14 Feb 2025 05:14:30 GMT  
		Size: 2.2 MB (2156458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8392c83bb5ca74ac2536da484f476060e0576df4291fcf2a36506693e7c16abb`  
		Last Modified: Fri, 14 Feb 2025 05:14:30 GMT  
		Size: 30.4 KB (30448 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; s390x

```console
$ docker pull composer@sha256:514b1702cd4a4e313e68efb932d1a34e62b5c54c49f0c2465c5dc7fce4994a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf86f0e4de62e927c746bd82826435184b467d536480050009788ae69f9a9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 15 Jan 2025 04:47:39 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 15 Jan 2025 04:47:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 21:26:01 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 21:26:03 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 21:25:59 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0774f657550ec6a831bbd0d72b777f8d8977a4143f082a39f86537a6691b415c`  
		Last Modified: Fri, 07 Feb 2025 22:27:36 GMT  
		Size: 31.7 MB (31677626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f93262ff5f92b789b5e28a5fbc8a229794cf568ee5c1a3fe803f21245857e1`  
		Last Modified: Fri, 07 Feb 2025 22:27:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9b2a0bbea2bb78104414d4305d0086cf64327d3c0a3ac678ac07b3d8afcc7a`  
		Last Modified: Tue, 21 Jan 2025 23:28:29 GMT  
		Size: 1.4 MB (1383351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3588ec3a1e72affeaac950ef30c1d99805230b13e773b9aef96652b945fa2141`  
		Last Modified: Tue, 21 Jan 2025 23:28:29 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b453745dccd0fecb39882a5afda7d8b34c942c7048c521a6513882466445da`  
		Last Modified: Tue, 21 Jan 2025 23:28:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:4fb4eaf35b8643843c6417cae1d72c654de0fbe0df2b7de4035367e4a39a4ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae841eb0ef743268cf2abb58eff2284437ad4a7923cb5f07dc868333bc2ac15`

```dockerfile
```

-	Layers:
	-	`sha256:f2f0d9b799b6bc8b7b0408409d0c4c0472e83ee8a40d324f34f5ae17c2fecd2e`  
		Last Modified: Fri, 14 Feb 2025 05:14:32 GMT  
		Size: 2.2 MB (2156244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be5f436ba87454a77d39c8729483d37c276b96306136d5cd9081d576dc12dae7`  
		Last Modified: Fri, 14 Feb 2025 05:14:32 GMT  
		Size: 30.4 KB (30406 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8`

```console
$ docker pull composer@sha256:4e931c046b91c45dfadb9b00a7ffd540cc75e579700718c122450d0a22d4525a
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
$ docker pull composer@sha256:98c3dbf57e4159b38905f4b8c2814c1fc31e7462087f0329848d90df359eaaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77810713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdedb63128b75c5194577b44d938b7536cf1b39c47e7dce2f4d8f2eda01c0288`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd2e180aa89ecb0845d1628b35579e1eb961f47975c3bc5a05ede5b6d47cb58`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 5.6 MB (5629137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d695b6cf2c8c3fcda26df544b054468a24be6cd41394db0208e3a333f18822f3`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7a3d474383ce078a67dbd96e1b61dc0d0b1fe673292ddc8d689e44c69655c2`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7370e670250547c9c1b145d13d02d6fa20bab3226e296408d9031c6a495186b6`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 13.6 MB (13609848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877e753ed32393f8eb06b7cf17507f31ab0f3db652e55c55ab86c82c3df4bf55`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d0fa737a71d88d348cb60ef0ff16ef4df36a45dddcd8bfe55e07d84f69a6a`  
		Last Modified: Fri, 14 Feb 2025 04:09:21 GMT  
		Size: 21.4 MB (21352652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf998db890f8e3ee8a94d02d3ea220e376efdd8371bffcc8379ce3ed9eee6e`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280727407916ee60ca49cf4ea07ef8f4b509704188598c3a99b973502ec133e3`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 20.1 KB (20058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4a85286c44cd7ccfe425a6f93c7d0554dc42bbedacec0451d7bfd33c04b19f`  
		Last Modified: Fri, 14 Feb 2025 05:08:28 GMT  
		Size: 31.9 MB (31907453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d650030e45e31239c615919ce51e844144a1710157eab8b6d2c1d14231b2b04`  
		Last Modified: Fri, 14 Feb 2025 05:08:27 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33ba8f5460e6cfb8b7879005fdac9e3a232bd59cd576f65021db114a9c7a9d5`  
		Last Modified: Fri, 14 Feb 2025 05:08:26 GMT  
		Size: 1.6 MB (1644985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e1d6d950ac72d921b31aa38a9bd355a127e7e28383aa07cb7011e2744e9224`  
		Last Modified: Fri, 14 Feb 2025 05:08:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386be936fe6e1133d7e69972d64ac992c9941bf1c7bff9fc5d2a5bdaffb20452`  
		Last Modified: Fri, 14 Feb 2025 05:08:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:0722f68eb3a20f8db15be53fcc10b0b74bbbde583039272d7cb7acf4f5478408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a324644870e5d4ce9d68b379fb5c3253df720706ab3f074189c907254c6d0f`

```dockerfile
```

-	Layers:
	-	`sha256:3f69c0b6c741ae5e0e0a00b8e26516f95eeabe727b031359e0d8d79b5d130564`  
		Last Modified: Fri, 14 Feb 2025 05:13:58 GMT  
		Size: 2.2 MB (2159253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0039cc6ead448a857c25b5cf521d153b13478cced1fa26be93b5497905f28cd7`  
		Last Modified: Fri, 14 Feb 2025 05:13:59 GMT  
		Size: 30.7 KB (30710 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:7c0eaa29ce8bb36c4865ab49d91a70a201cf20dc88f2cb980dfc195e1365b3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76018343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580c3e1bae7598f5d0083008438223589d64b33c1780d81dbab29e50e80e6d6a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 15 Jan 2025 01:25:26 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 15 Jan 2025 08:46:52 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 15 Jan 2025 08:46:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f6b305cd77dc6b597a3169970fd07b292703741539eaded2551c0d9a9a3ce2`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 13.6 MB (13609882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45767d1a2e12eb03ad18b9a7888cfb876903b7b27f5e22317a9a419e6c9357a4`  
		Last Modified: Fri, 14 Feb 2025 02:36:56 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b187df6e200be4ae6d666ab1d197a76dab384b63436f2df83f864d48fc6190f`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 22.4 MB (22402333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15e817c4c3f6223fc729a85f3b2dc3fa7ea9c2a3bf884f218dee6205043c6cf`  
		Last Modified: Fri, 14 Feb 2025 02:36:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45820a47f5394522a107e4a692c1e0d3689a29363793dbbf16751ed29bade6`  
		Last Modified: Fri, 14 Feb 2025 05:14:24 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07fdd9ff35b65c886cb11f76394f3a6058bcc6ffe163f41c4b09e0855ae0`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 31.6 MB (31601043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0554a9e2a4103b0bc17495a139a3314d3e4b40b4bc9ac6728a33ff747fe0226a`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e83fb5e8622068c07f88d893f9d43182717a2f86103513c505fdf0ff4a733f`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 1.7 MB (1715966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e07fcb8f2908d1ea5b2f87eff807dea12a006b5de0d58af277c954b96f3aea`  
		Last Modified: Fri, 14 Feb 2025 05:09:29 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4ef668ae27cb0fd96e1c2056708e1a33f0ed030cf02a01af62d279000076d8`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:48e33a3a101e81bd492b82957c1c8eaf21a41b4d7b3a9a2c7e3db656e3936333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed27818420ff5f18b10d2c38849ef1903ef7be61a5e63cd703017196e3567a66`

```dockerfile
```

-	Layers:
	-	`sha256:c1b97655659ad1d250704281928f1212fbc8f9cee8ffe53d11e173cc72a1dfe2`  
		Last Modified: Fri, 14 Feb 2025 05:14:00 GMT  
		Size: 30.6 KB (30597 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:c0bc01156691c66e7911e95e38cc0131d5214505b8a95d765cc344f4827eed5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69464673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17134b2d5c1fdf6dac461ba4851cae923b1496e80506bc776363379193f0f20c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 15 Jan 2025 00:28:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 21:24:38 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 21:24:39 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 21:24:35 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b02f56cd79bb67b2e6a8c6a2926c13febe08627a14d51ac60cca77caa0bd9b`  
		Last Modified: Tue, 04 Feb 2025 15:48:01 GMT  
		Size: 30.2 MB (30150807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a36ded2ef8fef32700c53fb042e1d25e6c4b243e0eaa2fa4c9987aa4de12ad9`  
		Last Modified: Tue, 04 Feb 2025 16:45:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832eb27d7c64b0492c397833cc42d8260f45e451a55c853f598dd256b23548ea`  
		Last Modified: Wed, 05 Feb 2025 22:29:43 GMT  
		Size: 1.5 MB (1476391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1201604993e876f18b05ecf6abdff45d0476cf834899dbbe856643b481b76ce0`  
		Last Modified: Tue, 04 Feb 2025 11:24:02 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd458b10679ce2ec3630036a732d04eff3d74b07347c47634f74b21951aa4b0`  
		Last Modified: Wed, 05 Feb 2025 22:29:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:3e7d90af0511190788cb60baa68fc96ea1f82e2957ea0f116cc80bdb80e0321e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2badf45813c77ff22edcb9cd526bfffa5d475bc354124f0ebca3f11d6f90412`

```dockerfile
```

-	Layers:
	-	`sha256:ba4cc6b7c6aaee6213cd6f5d9409ec9fa1cc3e58446889c8c3b3b14aca8501da`  
		Last Modified: Fri, 07 Feb 2025 22:26:56 GMT  
		Size: 2.2 MB (2159577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d75f5f35b12b24b66c33e580aeca9cbf6b2c45b4a29f0326d9e718d9842e7d2`  
		Last Modified: Fri, 07 Feb 2025 22:26:56 GMT  
		Size: 30.8 KB (30812 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:5966e1cb67473a4f2a0eed9cec403084706fd11b05d558cf7856f5454e7c44a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79090094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571c134f609235f6475d296087830826b5dc471665429151fc8207155e7fab0a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Tue, 14 Jan 2025 20:34:52 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Tue, 14 Jan 2025 20:34:51 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf60bd0bee7688614b1af07694e9e862a6e468345b4d8c1274b901e3308d850`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 13.6 MB (13609906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5935d74cc4f8900f9fe931cf198c384636eccfe5b27fcf8222bad1a34adc3c`  
		Last Modified: Fri, 14 Feb 2025 03:03:44 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3dd78614141a7cf92fd59b8e7fccf1f50faaef52fe4a0a661d5b0d846a4ea`  
		Last Modified: Fri, 14 Feb 2025 05:14:49 GMT  
		Size: 24.4 MB (24449108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eb61917bf0624ecf3420f926f6053b48728486c0188ada2088cb4c8939857e`  
		Last Modified: Fri, 14 Feb 2025 05:12:47 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc28a76fb7622bd8689c33b509f275a2d2558a77eccd18f266bc3ce660c7deb6`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7df60278df6c56d8ef9b2df595e68e15a33c291bf23b297f3ebb680a74161f`  
		Last Modified: Fri, 14 Feb 2025 05:14:54 GMT  
		Size: 32.0 MB (32009162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24085d57bfcbbba22355b95422cdf2ec94dde42b3fed500ec739e6f28f614030`  
		Last Modified: Fri, 14 Feb 2025 05:14:39 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5780913f5327a65eaa08945878e133be406b2c997920b9bdc907ab9510f195d1`  
		Last Modified: Fri, 14 Feb 2025 05:14:47 GMT  
		Size: 1.7 MB (1677125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f15c3f82485f4525b92f91cb033d47c7a19bae4309fed26f3b5a1afb85b52`  
		Last Modified: Fri, 14 Feb 2025 05:12:50 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2520aed179c04104eeed784905fb04adcf98131bd84fcffc0f9c6c586b8096`  
		Last Modified: Fri, 14 Feb 2025 05:14:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:9030171990a9d8540de8c28915a0303bd98497a6dd28e236b41ccb1361383970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cba49e4a776da5d5e8cbfd4ba34a837adafaed41e63376cbc41b805a6e49be`

```dockerfile
```

-	Layers:
	-	`sha256:2d2ee95b8c9c2dadcb15898b1759559454a4f086bbe31a0b49407824c5e9e59e`  
		Last Modified: Fri, 14 Feb 2025 05:14:03 GMT  
		Size: 2.2 MB (2159405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5d0a7330c42062fe1edeb831cfc8b22a74c1d5bf81bcad0f3eeb008ce1bf07`  
		Last Modified: Fri, 14 Feb 2025 05:14:03 GMT  
		Size: 30.8 KB (30843 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; 386

```console
$ docker pull composer@sha256:08355227fff4dd024f6581b8e4f8541e85e8d4b941238617fda2a17eaf813d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78509299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8332bfe7eb8d1a21458a7bd2a7297b4c6f3bd3484d40b55872e54d47d8011446`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c4f61d7599e7869ad3a9d452f69e9bc3899f18d70701124026229667c57db`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 5.5 MB (5479161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb08d2bfa2365278e7427cd03c6a3b6d0d200bf048c31056c211ff6bd1d83e3f`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ccac1acad29397cc55b48dcff4f9ee2a1ad8bb562aefc4e7345e5ba177ea66`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77470d2cfb3c06673c0297f09fdcfd1debad3d8c75b8f08ee1be3f66d5edfb5`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 13.6 MB (13609860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56194a5a61ce8b305a5554d8aff3980c32fe8df11e9dae038a5c1169482a4dff`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb641c65fcb36b09714fd6d6634df4fa431b7f127829dd93eecb97dc6d4674`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 21.9 MB (21875599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8652ddf39bd8a77eabbc758325596a213cfa201e124d3a8e14c0d3fedbbe920a`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7c976ea7a0a95cb41a13dd1eff7887ba420c913603c766514f637eb3933a56`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb6eafacb1f15fd12bd7bcf6493945cb15347ce13399873ee2a41fa97d49cff`  
		Last Modified: Fri, 14 Feb 2025 05:08:46 GMT  
		Size: 32.4 MB (32391459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97aaf4f7252c27f8cf968b89e5b0ecafcc390c2ef0d24ad4da6331436e6d82a7`  
		Last Modified: Fri, 14 Feb 2025 05:08:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356c18fd62985f302d2320070ad2ae27ffc266dd31376242baead03cdb4d843`  
		Last Modified: Fri, 14 Feb 2025 05:08:44 GMT  
		Size: 1.7 MB (1665158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30078a4cf8eb3b57398ebe7bdb98b7968f346e86e35c11f18f88f86b5627002f`  
		Last Modified: Fri, 14 Feb 2025 04:09:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f4051ab2bc9b427dbc31f39e35232e46b7de196f743bdaa8cbae6e807bc3e`  
		Last Modified: Fri, 14 Feb 2025 05:08:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:b82a57e8798a6cb97e0344644ffd81d80ae1c3af3ca150c3d29bd1421dc6a93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99298ea41039982ecee0dd21aadc4fa520b9e87f2178f5f23150a92357875db2`

```dockerfile
```

-	Layers:
	-	`sha256:1f211dc3f8e2a130cda31988f71789007d829d2b41e0f689d19dce4638397932`  
		Last Modified: Fri, 14 Feb 2025 05:14:05 GMT  
		Size: 2.2 MB (2159036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af56ea76f873f21852ad49dc4284d8b333f62f544cdbc528202a4344b04b51f8`  
		Last Modified: Fri, 14 Feb 2025 05:14:05 GMT  
		Size: 30.7 KB (30674 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; ppc64le

```console
$ docker pull composer@sha256:a09de83280ca038e135b44a4607d8389183c7fd0823a4032e310069333e59d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80744150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10d87b0a8782e3163fa9eea183f45888d8813ec516bde12da44f0e9a32a8239`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 15 Jan 2025 04:47:37 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704aa6bd4f8e770473b08a863515e74229b7563d9a2694d4dcffebd63189d5ab`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 13.6 MB (13609905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43c7e0504550dd35c7e6f3c1f5c61ed5db00067d11ffd3741e8f23b0dc16660`  
		Last Modified: Fri, 14 Feb 2025 05:09:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1167c96dbe49f246b96adc095a28edefcc2fe61bdc39108f8050c176699f483b`  
		Last Modified: Fri, 14 Feb 2025 02:47:38 GMT  
		Size: 25.4 MB (25398061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e16862c42f1028fedb8b04c6b22bd4e945a213a3e5a113872b385ee049f719`  
		Last Modified: Fri, 14 Feb 2025 05:10:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10f990e07f31e3d864671985a77e555905c511508a842be3262c8c7b9a96ec9`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 19.9 KB (19884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e260f2e53edd998f9cf2d3ba59929e4a7ff0f39075889a9b99dcb55b35732a9`  
		Last Modified: Fri, 14 Feb 2025 04:28:17 GMT  
		Size: 33.0 MB (32950697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717745514d5555d6812144710631aed2946af2ee5c721b80f8bf0a8b750bd43`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f14f9920e5bfe51f6d8808a523894518e858f697a3281f8e9517226ca0d5e13`  
		Last Modified: Fri, 14 Feb 2025 04:30:23 GMT  
		Size: 1.7 MB (1710788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7015ed3bdb11921234a436d525ca99e38f61a051eae27121d690c066c4c9236`  
		Last Modified: Fri, 14 Feb 2025 05:10:02 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992a149056344d183825544650b2929a59f83b5452c0fdd8fabf867596c0501e`  
		Last Modified: Fri, 14 Feb 2025 04:30:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:72c14f99f64f8fc43b543d46de0163d84b192d43146e499790ac387687816171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7089099d6b172fcdf57bc94469e526e42360d85acd4207ee0f7691b58bf22338`

```dockerfile
```

-	Layers:
	-	`sha256:90618ab6c2c49038e5501c01c4db3c116df47812a94026f3de986c1b6fe8b5a0`  
		Last Modified: Fri, 14 Feb 2025 05:14:07 GMT  
		Size: 2.2 MB (2157816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b38932949716320124314187b77759e67c643bebe1168bda822d1eb03eeb0112`  
		Last Modified: Fri, 14 Feb 2025 05:14:07 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; riscv64

```console
$ docker pull composer@sha256:1251e7574e214e7b7022475238cc4527c28826e8c2c07204647735316cfd7c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73264136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e55cf7ec6b8902a45b5c36f9043f70f41816a7753d07438eb34fcabe2ff0eca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 15 Jan 2025 08:47:48 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 15 Jan 2025 03:01:25 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 15 Jan 2025 10:06:18 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 21:25:44 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 21:25:46 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 21:25:42 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df9d36d8de7098821c518291549b46c279424dc339b2da655e42c88a93a214e`  
		Last Modified: Mon, 10 Feb 2025 19:35:11 GMT  
		Size: 31.0 MB (31000989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e43f72402a8544ac8a8358f26a470e096d8b0a4416c1d930f95b5531cbe553`  
		Last Modified: Fri, 07 Feb 2025 22:27:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48910cdc7c38676ed7d29cd41f54ee4ed652c0aca4f5dc6fd36fc0ba57e72ce6`  
		Last Modified: Fri, 07 Feb 2025 22:27:31 GMT  
		Size: 1.5 MB (1518474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dac6612285e15c9017337237de7aaeea8529a6bf8e4525205f29f12a2fbb1b`  
		Last Modified: Mon, 10 Feb 2025 19:35:08 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756a5fae31e1504c538a672d57d4ff44b48aa821391488ebb9982cabb6e6ea1e`  
		Last Modified: Fri, 07 Feb 2025 22:27:33 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:f5e6f63e08366e67f549de343bf09f9d591a98753ec860b818f2fda598a53916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0135a1f3aa7c46d0b4c5cec112b52e3b13d708cfe8a49b8306621fb9cad4a4e3`

```dockerfile
```

-	Layers:
	-	`sha256:b079cd3d901a783779cda17e3e2b07831ee2ad8976830e6756e92eea5d81ef4b`  
		Last Modified: Mon, 10 Feb 2025 19:35:12 GMT  
		Size: 2.2 MB (2156758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c42dfd8576186600f64611749e8918fd7b70fd53a5ca693088199ba932473a`  
		Last Modified: Fri, 07 Feb 2025 22:27:33 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; s390x

```console
$ docker pull composer@sha256:3de176ce49537f78983acb45f370eec1465f56e0253789881ccd6d4dda1c7ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75221980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6d751203d1b8e3ed6e5c6905791abfa78579ba4daeb1b7e3d17f4ac45482ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 15 Jan 2025 04:47:39 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 15 Jan 2025 04:47:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 21:26:01 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 21:26:03 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 21:25:59 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0774f657550ec6a831bbd0d72b777f8d8977a4143f082a39f86537a6691b415c`  
		Last Modified: Fri, 07 Feb 2025 22:27:36 GMT  
		Size: 31.7 MB (31677626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f93262ff5f92b789b5e28a5fbc8a229794cf568ee5c1a3fe803f21245857e1`  
		Last Modified: Fri, 07 Feb 2025 22:27:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5621a0404c4346630297b77ccb90ad199ec5969a33b7cae2c363c4800af9f1`  
		Last Modified: Fri, 07 Feb 2025 14:50:22 GMT  
		Size: 1.5 MB (1525986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1201604993e876f18b05ecf6abdff45d0476cf834899dbbe856643b481b76ce0`  
		Last Modified: Tue, 04 Feb 2025 11:24:02 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b6314112280f82f9a8c69377889d4e36d84d4abd16495353f6c66167f17921`  
		Last Modified: Fri, 07 Feb 2025 22:27:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:9b8e5897e6a59e0262f3c8f7577aeb09cfe9a12c0555758adafd59c03838b005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104537f60dbca84d4e20fd79f14b37e49746c45e815c2ac6a909ce6f313987af`

```dockerfile
```

-	Layers:
	-	`sha256:dd79fd0604808059960a43f80aa3a7559a240f1818a73375ddd02b8bac73ea0b`  
		Last Modified: Fri, 07 Feb 2025 22:27:39 GMT  
		Size: 2.2 MB (2156538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8cc3506acaa83ed74f21f0a15ad7aec58699e896de7e0467599825de60d1358`  
		Last Modified: Mon, 10 Feb 2025 19:35:19 GMT  
		Size: 30.7 KB (30709 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8.5`

```console
$ docker pull composer@sha256:4e931c046b91c45dfadb9b00a7ffd540cc75e579700718c122450d0a22d4525a
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

### `composer:2.8.5` - linux; amd64

```console
$ docker pull composer@sha256:98c3dbf57e4159b38905f4b8c2814c1fc31e7462087f0329848d90df359eaaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77810713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdedb63128b75c5194577b44d938b7536cf1b39c47e7dce2f4d8f2eda01c0288`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd2e180aa89ecb0845d1628b35579e1eb961f47975c3bc5a05ede5b6d47cb58`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 5.6 MB (5629137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d695b6cf2c8c3fcda26df544b054468a24be6cd41394db0208e3a333f18822f3`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7a3d474383ce078a67dbd96e1b61dc0d0b1fe673292ddc8d689e44c69655c2`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7370e670250547c9c1b145d13d02d6fa20bab3226e296408d9031c6a495186b6`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 13.6 MB (13609848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877e753ed32393f8eb06b7cf17507f31ab0f3db652e55c55ab86c82c3df4bf55`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d0fa737a71d88d348cb60ef0ff16ef4df36a45dddcd8bfe55e07d84f69a6a`  
		Last Modified: Fri, 14 Feb 2025 04:09:21 GMT  
		Size: 21.4 MB (21352652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf998db890f8e3ee8a94d02d3ea220e376efdd8371bffcc8379ce3ed9eee6e`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280727407916ee60ca49cf4ea07ef8f4b509704188598c3a99b973502ec133e3`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 20.1 KB (20058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4a85286c44cd7ccfe425a6f93c7d0554dc42bbedacec0451d7bfd33c04b19f`  
		Last Modified: Fri, 14 Feb 2025 05:08:28 GMT  
		Size: 31.9 MB (31907453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d650030e45e31239c615919ce51e844144a1710157eab8b6d2c1d14231b2b04`  
		Last Modified: Fri, 14 Feb 2025 05:08:27 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33ba8f5460e6cfb8b7879005fdac9e3a232bd59cd576f65021db114a9c7a9d5`  
		Last Modified: Fri, 14 Feb 2025 05:08:26 GMT  
		Size: 1.6 MB (1644985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e1d6d950ac72d921b31aa38a9bd355a127e7e28383aa07cb7011e2744e9224`  
		Last Modified: Fri, 14 Feb 2025 05:08:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386be936fe6e1133d7e69972d64ac992c9941bf1c7bff9fc5d2a5bdaffb20452`  
		Last Modified: Fri, 14 Feb 2025 05:08:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.5` - unknown; unknown

```console
$ docker pull composer@sha256:0722f68eb3a20f8db15be53fcc10b0b74bbbde583039272d7cb7acf4f5478408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a324644870e5d4ce9d68b379fb5c3253df720706ab3f074189c907254c6d0f`

```dockerfile
```

-	Layers:
	-	`sha256:3f69c0b6c741ae5e0e0a00b8e26516f95eeabe727b031359e0d8d79b5d130564`  
		Last Modified: Fri, 14 Feb 2025 05:13:58 GMT  
		Size: 2.2 MB (2159253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0039cc6ead448a857c25b5cf521d153b13478cced1fa26be93b5497905f28cd7`  
		Last Modified: Fri, 14 Feb 2025 05:13:59 GMT  
		Size: 30.7 KB (30710 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.5` - linux; arm variant v6

```console
$ docker pull composer@sha256:7c0eaa29ce8bb36c4865ab49d91a70a201cf20dc88f2cb980dfc195e1365b3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76018343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580c3e1bae7598f5d0083008438223589d64b33c1780d81dbab29e50e80e6d6a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 15 Jan 2025 01:25:26 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 15 Jan 2025 08:46:52 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 15 Jan 2025 08:46:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f6b305cd77dc6b597a3169970fd07b292703741539eaded2551c0d9a9a3ce2`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 13.6 MB (13609882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45767d1a2e12eb03ad18b9a7888cfb876903b7b27f5e22317a9a419e6c9357a4`  
		Last Modified: Fri, 14 Feb 2025 02:36:56 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b187df6e200be4ae6d666ab1d197a76dab384b63436f2df83f864d48fc6190f`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 22.4 MB (22402333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15e817c4c3f6223fc729a85f3b2dc3fa7ea9c2a3bf884f218dee6205043c6cf`  
		Last Modified: Fri, 14 Feb 2025 02:36:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45820a47f5394522a107e4a692c1e0d3689a29363793dbbf16751ed29bade6`  
		Last Modified: Fri, 14 Feb 2025 05:14:24 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07fdd9ff35b65c886cb11f76394f3a6058bcc6ffe163f41c4b09e0855ae0`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 31.6 MB (31601043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0554a9e2a4103b0bc17495a139a3314d3e4b40b4bc9ac6728a33ff747fe0226a`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e83fb5e8622068c07f88d893f9d43182717a2f86103513c505fdf0ff4a733f`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 1.7 MB (1715966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e07fcb8f2908d1ea5b2f87eff807dea12a006b5de0d58af277c954b96f3aea`  
		Last Modified: Fri, 14 Feb 2025 05:09:29 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4ef668ae27cb0fd96e1c2056708e1a33f0ed030cf02a01af62d279000076d8`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.5` - unknown; unknown

```console
$ docker pull composer@sha256:48e33a3a101e81bd492b82957c1c8eaf21a41b4d7b3a9a2c7e3db656e3936333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed27818420ff5f18b10d2c38849ef1903ef7be61a5e63cd703017196e3567a66`

```dockerfile
```

-	Layers:
	-	`sha256:c1b97655659ad1d250704281928f1212fbc8f9cee8ffe53d11e173cc72a1dfe2`  
		Last Modified: Fri, 14 Feb 2025 05:14:00 GMT  
		Size: 30.6 KB (30597 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.5` - linux; arm variant v7

```console
$ docker pull composer@sha256:c0bc01156691c66e7911e95e38cc0131d5214505b8a95d765cc344f4827eed5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69464673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17134b2d5c1fdf6dac461ba4851cae923b1496e80506bc776363379193f0f20c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 15 Jan 2025 00:28:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 21:24:38 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 21:24:39 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 21:24:35 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b02f56cd79bb67b2e6a8c6a2926c13febe08627a14d51ac60cca77caa0bd9b`  
		Last Modified: Tue, 04 Feb 2025 15:48:01 GMT  
		Size: 30.2 MB (30150807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a36ded2ef8fef32700c53fb042e1d25e6c4b243e0eaa2fa4c9987aa4de12ad9`  
		Last Modified: Tue, 04 Feb 2025 16:45:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832eb27d7c64b0492c397833cc42d8260f45e451a55c853f598dd256b23548ea`  
		Last Modified: Wed, 05 Feb 2025 22:29:43 GMT  
		Size: 1.5 MB (1476391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1201604993e876f18b05ecf6abdff45d0476cf834899dbbe856643b481b76ce0`  
		Last Modified: Tue, 04 Feb 2025 11:24:02 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd458b10679ce2ec3630036a732d04eff3d74b07347c47634f74b21951aa4b0`  
		Last Modified: Wed, 05 Feb 2025 22:29:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.5` - unknown; unknown

```console
$ docker pull composer@sha256:3e7d90af0511190788cb60baa68fc96ea1f82e2957ea0f116cc80bdb80e0321e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2badf45813c77ff22edcb9cd526bfffa5d475bc354124f0ebca3f11d6f90412`

```dockerfile
```

-	Layers:
	-	`sha256:ba4cc6b7c6aaee6213cd6f5d9409ec9fa1cc3e58446889c8c3b3b14aca8501da`  
		Last Modified: Fri, 07 Feb 2025 22:26:56 GMT  
		Size: 2.2 MB (2159577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d75f5f35b12b24b66c33e580aeca9cbf6b2c45b4a29f0326d9e718d9842e7d2`  
		Last Modified: Fri, 07 Feb 2025 22:26:56 GMT  
		Size: 30.8 KB (30812 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.5` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:5966e1cb67473a4f2a0eed9cec403084706fd11b05d558cf7856f5454e7c44a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79090094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571c134f609235f6475d296087830826b5dc471665429151fc8207155e7fab0a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Tue, 14 Jan 2025 20:34:52 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Tue, 14 Jan 2025 20:34:51 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf60bd0bee7688614b1af07694e9e862a6e468345b4d8c1274b901e3308d850`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 13.6 MB (13609906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5935d74cc4f8900f9fe931cf198c384636eccfe5b27fcf8222bad1a34adc3c`  
		Last Modified: Fri, 14 Feb 2025 03:03:44 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3dd78614141a7cf92fd59b8e7fccf1f50faaef52fe4a0a661d5b0d846a4ea`  
		Last Modified: Fri, 14 Feb 2025 05:14:49 GMT  
		Size: 24.4 MB (24449108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eb61917bf0624ecf3420f926f6053b48728486c0188ada2088cb4c8939857e`  
		Last Modified: Fri, 14 Feb 2025 05:12:47 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc28a76fb7622bd8689c33b509f275a2d2558a77eccd18f266bc3ce660c7deb6`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7df60278df6c56d8ef9b2df595e68e15a33c291bf23b297f3ebb680a74161f`  
		Last Modified: Fri, 14 Feb 2025 05:14:54 GMT  
		Size: 32.0 MB (32009162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24085d57bfcbbba22355b95422cdf2ec94dde42b3fed500ec739e6f28f614030`  
		Last Modified: Fri, 14 Feb 2025 05:14:39 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5780913f5327a65eaa08945878e133be406b2c997920b9bdc907ab9510f195d1`  
		Last Modified: Fri, 14 Feb 2025 05:14:47 GMT  
		Size: 1.7 MB (1677125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f15c3f82485f4525b92f91cb033d47c7a19bae4309fed26f3b5a1afb85b52`  
		Last Modified: Fri, 14 Feb 2025 05:12:50 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2520aed179c04104eeed784905fb04adcf98131bd84fcffc0f9c6c586b8096`  
		Last Modified: Fri, 14 Feb 2025 05:14:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.5` - unknown; unknown

```console
$ docker pull composer@sha256:9030171990a9d8540de8c28915a0303bd98497a6dd28e236b41ccb1361383970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cba49e4a776da5d5e8cbfd4ba34a837adafaed41e63376cbc41b805a6e49be`

```dockerfile
```

-	Layers:
	-	`sha256:2d2ee95b8c9c2dadcb15898b1759559454a4f086bbe31a0b49407824c5e9e59e`  
		Last Modified: Fri, 14 Feb 2025 05:14:03 GMT  
		Size: 2.2 MB (2159405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5d0a7330c42062fe1edeb831cfc8b22a74c1d5bf81bcad0f3eeb008ce1bf07`  
		Last Modified: Fri, 14 Feb 2025 05:14:03 GMT  
		Size: 30.8 KB (30843 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.5` - linux; 386

```console
$ docker pull composer@sha256:08355227fff4dd024f6581b8e4f8541e85e8d4b941238617fda2a17eaf813d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78509299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8332bfe7eb8d1a21458a7bd2a7297b4c6f3bd3484d40b55872e54d47d8011446`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c4f61d7599e7869ad3a9d452f69e9bc3899f18d70701124026229667c57db`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 5.5 MB (5479161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb08d2bfa2365278e7427cd03c6a3b6d0d200bf048c31056c211ff6bd1d83e3f`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ccac1acad29397cc55b48dcff4f9ee2a1ad8bb562aefc4e7345e5ba177ea66`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77470d2cfb3c06673c0297f09fdcfd1debad3d8c75b8f08ee1be3f66d5edfb5`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 13.6 MB (13609860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56194a5a61ce8b305a5554d8aff3980c32fe8df11e9dae038a5c1169482a4dff`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb641c65fcb36b09714fd6d6634df4fa431b7f127829dd93eecb97dc6d4674`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 21.9 MB (21875599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8652ddf39bd8a77eabbc758325596a213cfa201e124d3a8e14c0d3fedbbe920a`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7c976ea7a0a95cb41a13dd1eff7887ba420c913603c766514f637eb3933a56`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb6eafacb1f15fd12bd7bcf6493945cb15347ce13399873ee2a41fa97d49cff`  
		Last Modified: Fri, 14 Feb 2025 05:08:46 GMT  
		Size: 32.4 MB (32391459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97aaf4f7252c27f8cf968b89e5b0ecafcc390c2ef0d24ad4da6331436e6d82a7`  
		Last Modified: Fri, 14 Feb 2025 05:08:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356c18fd62985f302d2320070ad2ae27ffc266dd31376242baead03cdb4d843`  
		Last Modified: Fri, 14 Feb 2025 05:08:44 GMT  
		Size: 1.7 MB (1665158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30078a4cf8eb3b57398ebe7bdb98b7968f346e86e35c11f18f88f86b5627002f`  
		Last Modified: Fri, 14 Feb 2025 04:09:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f4051ab2bc9b427dbc31f39e35232e46b7de196f743bdaa8cbae6e807bc3e`  
		Last Modified: Fri, 14 Feb 2025 05:08:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.5` - unknown; unknown

```console
$ docker pull composer@sha256:b82a57e8798a6cb97e0344644ffd81d80ae1c3af3ca150c3d29bd1421dc6a93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99298ea41039982ecee0dd21aadc4fa520b9e87f2178f5f23150a92357875db2`

```dockerfile
```

-	Layers:
	-	`sha256:1f211dc3f8e2a130cda31988f71789007d829d2b41e0f689d19dce4638397932`  
		Last Modified: Fri, 14 Feb 2025 05:14:05 GMT  
		Size: 2.2 MB (2159036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af56ea76f873f21852ad49dc4284d8b333f62f544cdbc528202a4344b04b51f8`  
		Last Modified: Fri, 14 Feb 2025 05:14:05 GMT  
		Size: 30.7 KB (30674 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.5` - linux; ppc64le

```console
$ docker pull composer@sha256:a09de83280ca038e135b44a4607d8389183c7fd0823a4032e310069333e59d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80744150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10d87b0a8782e3163fa9eea183f45888d8813ec516bde12da44f0e9a32a8239`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 15 Jan 2025 04:47:37 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704aa6bd4f8e770473b08a863515e74229b7563d9a2694d4dcffebd63189d5ab`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 13.6 MB (13609905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43c7e0504550dd35c7e6f3c1f5c61ed5db00067d11ffd3741e8f23b0dc16660`  
		Last Modified: Fri, 14 Feb 2025 05:09:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1167c96dbe49f246b96adc095a28edefcc2fe61bdc39108f8050c176699f483b`  
		Last Modified: Fri, 14 Feb 2025 02:47:38 GMT  
		Size: 25.4 MB (25398061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e16862c42f1028fedb8b04c6b22bd4e945a213a3e5a113872b385ee049f719`  
		Last Modified: Fri, 14 Feb 2025 05:10:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10f990e07f31e3d864671985a77e555905c511508a842be3262c8c7b9a96ec9`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 19.9 KB (19884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e260f2e53edd998f9cf2d3ba59929e4a7ff0f39075889a9b99dcb55b35732a9`  
		Last Modified: Fri, 14 Feb 2025 04:28:17 GMT  
		Size: 33.0 MB (32950697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717745514d5555d6812144710631aed2946af2ee5c721b80f8bf0a8b750bd43`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f14f9920e5bfe51f6d8808a523894518e858f697a3281f8e9517226ca0d5e13`  
		Last Modified: Fri, 14 Feb 2025 04:30:23 GMT  
		Size: 1.7 MB (1710788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7015ed3bdb11921234a436d525ca99e38f61a051eae27121d690c066c4c9236`  
		Last Modified: Fri, 14 Feb 2025 05:10:02 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992a149056344d183825544650b2929a59f83b5452c0fdd8fabf867596c0501e`  
		Last Modified: Fri, 14 Feb 2025 04:30:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.5` - unknown; unknown

```console
$ docker pull composer@sha256:72c14f99f64f8fc43b543d46de0163d84b192d43146e499790ac387687816171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7089099d6b172fcdf57bc94469e526e42360d85acd4207ee0f7691b58bf22338`

```dockerfile
```

-	Layers:
	-	`sha256:90618ab6c2c49038e5501c01c4db3c116df47812a94026f3de986c1b6fe8b5a0`  
		Last Modified: Fri, 14 Feb 2025 05:14:07 GMT  
		Size: 2.2 MB (2157816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b38932949716320124314187b77759e67c643bebe1168bda822d1eb03eeb0112`  
		Last Modified: Fri, 14 Feb 2025 05:14:07 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.5` - linux; riscv64

```console
$ docker pull composer@sha256:1251e7574e214e7b7022475238cc4527c28826e8c2c07204647735316cfd7c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73264136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e55cf7ec6b8902a45b5c36f9043f70f41816a7753d07438eb34fcabe2ff0eca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 15 Jan 2025 08:47:48 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 15 Jan 2025 03:01:25 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 15 Jan 2025 10:06:18 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 21:25:44 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 21:25:46 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 21:25:42 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df9d36d8de7098821c518291549b46c279424dc339b2da655e42c88a93a214e`  
		Last Modified: Mon, 10 Feb 2025 19:35:11 GMT  
		Size: 31.0 MB (31000989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e43f72402a8544ac8a8358f26a470e096d8b0a4416c1d930f95b5531cbe553`  
		Last Modified: Fri, 07 Feb 2025 22:27:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48910cdc7c38676ed7d29cd41f54ee4ed652c0aca4f5dc6fd36fc0ba57e72ce6`  
		Last Modified: Fri, 07 Feb 2025 22:27:31 GMT  
		Size: 1.5 MB (1518474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dac6612285e15c9017337237de7aaeea8529a6bf8e4525205f29f12a2fbb1b`  
		Last Modified: Mon, 10 Feb 2025 19:35:08 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756a5fae31e1504c538a672d57d4ff44b48aa821391488ebb9982cabb6e6ea1e`  
		Last Modified: Fri, 07 Feb 2025 22:27:33 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.5` - unknown; unknown

```console
$ docker pull composer@sha256:f5e6f63e08366e67f549de343bf09f9d591a98753ec860b818f2fda598a53916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0135a1f3aa7c46d0b4c5cec112b52e3b13d708cfe8a49b8306621fb9cad4a4e3`

```dockerfile
```

-	Layers:
	-	`sha256:b079cd3d901a783779cda17e3e2b07831ee2ad8976830e6756e92eea5d81ef4b`  
		Last Modified: Mon, 10 Feb 2025 19:35:12 GMT  
		Size: 2.2 MB (2156758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c42dfd8576186600f64611749e8918fd7b70fd53a5ca693088199ba932473a`  
		Last Modified: Fri, 07 Feb 2025 22:27:33 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.5` - linux; s390x

```console
$ docker pull composer@sha256:3de176ce49537f78983acb45f370eec1465f56e0253789881ccd6d4dda1c7ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75221980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6d751203d1b8e3ed6e5c6905791abfa78579ba4daeb1b7e3d17f4ac45482ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 15 Jan 2025 04:47:39 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 15 Jan 2025 04:47:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 21:26:01 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 21:26:03 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 21:25:59 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0774f657550ec6a831bbd0d72b777f8d8977a4143f082a39f86537a6691b415c`  
		Last Modified: Fri, 07 Feb 2025 22:27:36 GMT  
		Size: 31.7 MB (31677626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f93262ff5f92b789b5e28a5fbc8a229794cf568ee5c1a3fe803f21245857e1`  
		Last Modified: Fri, 07 Feb 2025 22:27:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5621a0404c4346630297b77ccb90ad199ec5969a33b7cae2c363c4800af9f1`  
		Last Modified: Fri, 07 Feb 2025 14:50:22 GMT  
		Size: 1.5 MB (1525986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1201604993e876f18b05ecf6abdff45d0476cf834899dbbe856643b481b76ce0`  
		Last Modified: Tue, 04 Feb 2025 11:24:02 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b6314112280f82f9a8c69377889d4e36d84d4abd16495353f6c66167f17921`  
		Last Modified: Fri, 07 Feb 2025 22:27:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.5` - unknown; unknown

```console
$ docker pull composer@sha256:9b8e5897e6a59e0262f3c8f7577aeb09cfe9a12c0555758adafd59c03838b005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104537f60dbca84d4e20fd79f14b37e49746c45e815c2ac6a909ce6f313987af`

```dockerfile
```

-	Layers:
	-	`sha256:dd79fd0604808059960a43f80aa3a7559a240f1818a73375ddd02b8bac73ea0b`  
		Last Modified: Fri, 07 Feb 2025 22:27:39 GMT  
		Size: 2.2 MB (2156538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8cc3506acaa83ed74f21f0a15ad7aec58699e896de7e0467599825de60d1358`  
		Last Modified: Mon, 10 Feb 2025 19:35:19 GMT  
		Size: 30.7 KB (30709 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:4e931c046b91c45dfadb9b00a7ffd540cc75e579700718c122450d0a22d4525a
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
$ docker pull composer@sha256:98c3dbf57e4159b38905f4b8c2814c1fc31e7462087f0329848d90df359eaaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77810713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdedb63128b75c5194577b44d938b7536cf1b39c47e7dce2f4d8f2eda01c0288`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd2e180aa89ecb0845d1628b35579e1eb961f47975c3bc5a05ede5b6d47cb58`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 5.6 MB (5629137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d695b6cf2c8c3fcda26df544b054468a24be6cd41394db0208e3a333f18822f3`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7a3d474383ce078a67dbd96e1b61dc0d0b1fe673292ddc8d689e44c69655c2`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7370e670250547c9c1b145d13d02d6fa20bab3226e296408d9031c6a495186b6`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 13.6 MB (13609848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877e753ed32393f8eb06b7cf17507f31ab0f3db652e55c55ab86c82c3df4bf55`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d0fa737a71d88d348cb60ef0ff16ef4df36a45dddcd8bfe55e07d84f69a6a`  
		Last Modified: Fri, 14 Feb 2025 04:09:21 GMT  
		Size: 21.4 MB (21352652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf998db890f8e3ee8a94d02d3ea220e376efdd8371bffcc8379ce3ed9eee6e`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280727407916ee60ca49cf4ea07ef8f4b509704188598c3a99b973502ec133e3`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 20.1 KB (20058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4a85286c44cd7ccfe425a6f93c7d0554dc42bbedacec0451d7bfd33c04b19f`  
		Last Modified: Fri, 14 Feb 2025 05:08:28 GMT  
		Size: 31.9 MB (31907453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d650030e45e31239c615919ce51e844144a1710157eab8b6d2c1d14231b2b04`  
		Last Modified: Fri, 14 Feb 2025 05:08:27 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33ba8f5460e6cfb8b7879005fdac9e3a232bd59cd576f65021db114a9c7a9d5`  
		Last Modified: Fri, 14 Feb 2025 05:08:26 GMT  
		Size: 1.6 MB (1644985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e1d6d950ac72d921b31aa38a9bd355a127e7e28383aa07cb7011e2744e9224`  
		Last Modified: Fri, 14 Feb 2025 05:08:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386be936fe6e1133d7e69972d64ac992c9941bf1c7bff9fc5d2a5bdaffb20452`  
		Last Modified: Fri, 14 Feb 2025 05:08:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:0722f68eb3a20f8db15be53fcc10b0b74bbbde583039272d7cb7acf4f5478408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a324644870e5d4ce9d68b379fb5c3253df720706ab3f074189c907254c6d0f`

```dockerfile
```

-	Layers:
	-	`sha256:3f69c0b6c741ae5e0e0a00b8e26516f95eeabe727b031359e0d8d79b5d130564`  
		Last Modified: Fri, 14 Feb 2025 05:13:58 GMT  
		Size: 2.2 MB (2159253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0039cc6ead448a857c25b5cf521d153b13478cced1fa26be93b5497905f28cd7`  
		Last Modified: Fri, 14 Feb 2025 05:13:59 GMT  
		Size: 30.7 KB (30710 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:7c0eaa29ce8bb36c4865ab49d91a70a201cf20dc88f2cb980dfc195e1365b3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76018343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580c3e1bae7598f5d0083008438223589d64b33c1780d81dbab29e50e80e6d6a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 15 Jan 2025 01:25:26 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 15 Jan 2025 08:46:52 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 15 Jan 2025 08:46:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f6b305cd77dc6b597a3169970fd07b292703741539eaded2551c0d9a9a3ce2`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 13.6 MB (13609882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45767d1a2e12eb03ad18b9a7888cfb876903b7b27f5e22317a9a419e6c9357a4`  
		Last Modified: Fri, 14 Feb 2025 02:36:56 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b187df6e200be4ae6d666ab1d197a76dab384b63436f2df83f864d48fc6190f`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 22.4 MB (22402333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15e817c4c3f6223fc729a85f3b2dc3fa7ea9c2a3bf884f218dee6205043c6cf`  
		Last Modified: Fri, 14 Feb 2025 02:36:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45820a47f5394522a107e4a692c1e0d3689a29363793dbbf16751ed29bade6`  
		Last Modified: Fri, 14 Feb 2025 05:14:24 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07fdd9ff35b65c886cb11f76394f3a6058bcc6ffe163f41c4b09e0855ae0`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 31.6 MB (31601043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0554a9e2a4103b0bc17495a139a3314d3e4b40b4bc9ac6728a33ff747fe0226a`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e83fb5e8622068c07f88d893f9d43182717a2f86103513c505fdf0ff4a733f`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 1.7 MB (1715966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e07fcb8f2908d1ea5b2f87eff807dea12a006b5de0d58af277c954b96f3aea`  
		Last Modified: Fri, 14 Feb 2025 05:09:29 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4ef668ae27cb0fd96e1c2056708e1a33f0ed030cf02a01af62d279000076d8`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:48e33a3a101e81bd492b82957c1c8eaf21a41b4d7b3a9a2c7e3db656e3936333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed27818420ff5f18b10d2c38849ef1903ef7be61a5e63cd703017196e3567a66`

```dockerfile
```

-	Layers:
	-	`sha256:c1b97655659ad1d250704281928f1212fbc8f9cee8ffe53d11e173cc72a1dfe2`  
		Last Modified: Fri, 14 Feb 2025 05:14:00 GMT  
		Size: 30.6 KB (30597 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:c0bc01156691c66e7911e95e38cc0131d5214505b8a95d765cc344f4827eed5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69464673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17134b2d5c1fdf6dac461ba4851cae923b1496e80506bc776363379193f0f20c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 15 Jan 2025 00:28:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 21:24:38 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 21:24:39 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 21:24:35 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b02f56cd79bb67b2e6a8c6a2926c13febe08627a14d51ac60cca77caa0bd9b`  
		Last Modified: Tue, 04 Feb 2025 15:48:01 GMT  
		Size: 30.2 MB (30150807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a36ded2ef8fef32700c53fb042e1d25e6c4b243e0eaa2fa4c9987aa4de12ad9`  
		Last Modified: Tue, 04 Feb 2025 16:45:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832eb27d7c64b0492c397833cc42d8260f45e451a55c853f598dd256b23548ea`  
		Last Modified: Wed, 05 Feb 2025 22:29:43 GMT  
		Size: 1.5 MB (1476391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1201604993e876f18b05ecf6abdff45d0476cf834899dbbe856643b481b76ce0`  
		Last Modified: Tue, 04 Feb 2025 11:24:02 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd458b10679ce2ec3630036a732d04eff3d74b07347c47634f74b21951aa4b0`  
		Last Modified: Wed, 05 Feb 2025 22:29:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:3e7d90af0511190788cb60baa68fc96ea1f82e2957ea0f116cc80bdb80e0321e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2badf45813c77ff22edcb9cd526bfffa5d475bc354124f0ebca3f11d6f90412`

```dockerfile
```

-	Layers:
	-	`sha256:ba4cc6b7c6aaee6213cd6f5d9409ec9fa1cc3e58446889c8c3b3b14aca8501da`  
		Last Modified: Fri, 07 Feb 2025 22:26:56 GMT  
		Size: 2.2 MB (2159577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d75f5f35b12b24b66c33e580aeca9cbf6b2c45b4a29f0326d9e718d9842e7d2`  
		Last Modified: Fri, 07 Feb 2025 22:26:56 GMT  
		Size: 30.8 KB (30812 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:5966e1cb67473a4f2a0eed9cec403084706fd11b05d558cf7856f5454e7c44a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79090094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571c134f609235f6475d296087830826b5dc471665429151fc8207155e7fab0a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Tue, 14 Jan 2025 20:34:52 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Tue, 14 Jan 2025 20:34:51 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf60bd0bee7688614b1af07694e9e862a6e468345b4d8c1274b901e3308d850`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 13.6 MB (13609906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5935d74cc4f8900f9fe931cf198c384636eccfe5b27fcf8222bad1a34adc3c`  
		Last Modified: Fri, 14 Feb 2025 03:03:44 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3dd78614141a7cf92fd59b8e7fccf1f50faaef52fe4a0a661d5b0d846a4ea`  
		Last Modified: Fri, 14 Feb 2025 05:14:49 GMT  
		Size: 24.4 MB (24449108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eb61917bf0624ecf3420f926f6053b48728486c0188ada2088cb4c8939857e`  
		Last Modified: Fri, 14 Feb 2025 05:12:47 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc28a76fb7622bd8689c33b509f275a2d2558a77eccd18f266bc3ce660c7deb6`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7df60278df6c56d8ef9b2df595e68e15a33c291bf23b297f3ebb680a74161f`  
		Last Modified: Fri, 14 Feb 2025 05:14:54 GMT  
		Size: 32.0 MB (32009162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24085d57bfcbbba22355b95422cdf2ec94dde42b3fed500ec739e6f28f614030`  
		Last Modified: Fri, 14 Feb 2025 05:14:39 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5780913f5327a65eaa08945878e133be406b2c997920b9bdc907ab9510f195d1`  
		Last Modified: Fri, 14 Feb 2025 05:14:47 GMT  
		Size: 1.7 MB (1677125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f15c3f82485f4525b92f91cb033d47c7a19bae4309fed26f3b5a1afb85b52`  
		Last Modified: Fri, 14 Feb 2025 05:12:50 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2520aed179c04104eeed784905fb04adcf98131bd84fcffc0f9c6c586b8096`  
		Last Modified: Fri, 14 Feb 2025 05:14:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:9030171990a9d8540de8c28915a0303bd98497a6dd28e236b41ccb1361383970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cba49e4a776da5d5e8cbfd4ba34a837adafaed41e63376cbc41b805a6e49be`

```dockerfile
```

-	Layers:
	-	`sha256:2d2ee95b8c9c2dadcb15898b1759559454a4f086bbe31a0b49407824c5e9e59e`  
		Last Modified: Fri, 14 Feb 2025 05:14:03 GMT  
		Size: 2.2 MB (2159405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5d0a7330c42062fe1edeb831cfc8b22a74c1d5bf81bcad0f3eeb008ce1bf07`  
		Last Modified: Fri, 14 Feb 2025 05:14:03 GMT  
		Size: 30.8 KB (30843 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:08355227fff4dd024f6581b8e4f8541e85e8d4b941238617fda2a17eaf813d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78509299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8332bfe7eb8d1a21458a7bd2a7297b4c6f3bd3484d40b55872e54d47d8011446`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c4f61d7599e7869ad3a9d452f69e9bc3899f18d70701124026229667c57db`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 5.5 MB (5479161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb08d2bfa2365278e7427cd03c6a3b6d0d200bf048c31056c211ff6bd1d83e3f`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ccac1acad29397cc55b48dcff4f9ee2a1ad8bb562aefc4e7345e5ba177ea66`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77470d2cfb3c06673c0297f09fdcfd1debad3d8c75b8f08ee1be3f66d5edfb5`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 13.6 MB (13609860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56194a5a61ce8b305a5554d8aff3980c32fe8df11e9dae038a5c1169482a4dff`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb641c65fcb36b09714fd6d6634df4fa431b7f127829dd93eecb97dc6d4674`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 21.9 MB (21875599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8652ddf39bd8a77eabbc758325596a213cfa201e124d3a8e14c0d3fedbbe920a`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7c976ea7a0a95cb41a13dd1eff7887ba420c913603c766514f637eb3933a56`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb6eafacb1f15fd12bd7bcf6493945cb15347ce13399873ee2a41fa97d49cff`  
		Last Modified: Fri, 14 Feb 2025 05:08:46 GMT  
		Size: 32.4 MB (32391459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97aaf4f7252c27f8cf968b89e5b0ecafcc390c2ef0d24ad4da6331436e6d82a7`  
		Last Modified: Fri, 14 Feb 2025 05:08:44 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4356c18fd62985f302d2320070ad2ae27ffc266dd31376242baead03cdb4d843`  
		Last Modified: Fri, 14 Feb 2025 05:08:44 GMT  
		Size: 1.7 MB (1665158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30078a4cf8eb3b57398ebe7bdb98b7968f346e86e35c11f18f88f86b5627002f`  
		Last Modified: Fri, 14 Feb 2025 04:09:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f4051ab2bc9b427dbc31f39e35232e46b7de196f743bdaa8cbae6e807bc3e`  
		Last Modified: Fri, 14 Feb 2025 05:08:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:b82a57e8798a6cb97e0344644ffd81d80ae1c3af3ca150c3d29bd1421dc6a93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99298ea41039982ecee0dd21aadc4fa520b9e87f2178f5f23150a92357875db2`

```dockerfile
```

-	Layers:
	-	`sha256:1f211dc3f8e2a130cda31988f71789007d829d2b41e0f689d19dce4638397932`  
		Last Modified: Fri, 14 Feb 2025 05:14:05 GMT  
		Size: 2.2 MB (2159036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af56ea76f873f21852ad49dc4284d8b333f62f544cdbc528202a4344b04b51f8`  
		Last Modified: Fri, 14 Feb 2025 05:14:05 GMT  
		Size: 30.7 KB (30674 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:a09de83280ca038e135b44a4607d8389183c7fd0823a4032e310069333e59d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80744150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10d87b0a8782e3163fa9eea183f45888d8813ec516bde12da44f0e9a32a8239`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 21 Jan 2025 21:13:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Jan 2025 21:13:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_VERSION=8.4.4
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 21 Jan 2025 21:13:43 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 15 Jan 2025 04:47:37 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704aa6bd4f8e770473b08a863515e74229b7563d9a2694d4dcffebd63189d5ab`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 13.6 MB (13609905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43c7e0504550dd35c7e6f3c1f5c61ed5db00067d11ffd3741e8f23b0dc16660`  
		Last Modified: Fri, 14 Feb 2025 05:09:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1167c96dbe49f246b96adc095a28edefcc2fe61bdc39108f8050c176699f483b`  
		Last Modified: Fri, 14 Feb 2025 02:47:38 GMT  
		Size: 25.4 MB (25398061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e16862c42f1028fedb8b04c6b22bd4e945a213a3e5a113872b385ee049f719`  
		Last Modified: Fri, 14 Feb 2025 05:10:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10f990e07f31e3d864671985a77e555905c511508a842be3262c8c7b9a96ec9`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 19.9 KB (19884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e260f2e53edd998f9cf2d3ba59929e4a7ff0f39075889a9b99dcb55b35732a9`  
		Last Modified: Fri, 14 Feb 2025 04:28:17 GMT  
		Size: 33.0 MB (32950697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717745514d5555d6812144710631aed2946af2ee5c721b80f8bf0a8b750bd43`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f14f9920e5bfe51f6d8808a523894518e858f697a3281f8e9517226ca0d5e13`  
		Last Modified: Fri, 14 Feb 2025 04:30:23 GMT  
		Size: 1.7 MB (1710788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7015ed3bdb11921234a436d525ca99e38f61a051eae27121d690c066c4c9236`  
		Last Modified: Fri, 14 Feb 2025 05:10:02 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992a149056344d183825544650b2929a59f83b5452c0fdd8fabf867596c0501e`  
		Last Modified: Fri, 14 Feb 2025 04:30:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:72c14f99f64f8fc43b543d46de0163d84b192d43146e499790ac387687816171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7089099d6b172fcdf57bc94469e526e42360d85acd4207ee0f7691b58bf22338`

```dockerfile
```

-	Layers:
	-	`sha256:90618ab6c2c49038e5501c01c4db3c116df47812a94026f3de986c1b6fe8b5a0`  
		Last Modified: Fri, 14 Feb 2025 05:14:07 GMT  
		Size: 2.2 MB (2157816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b38932949716320124314187b77759e67c643bebe1168bda822d1eb03eeb0112`  
		Last Modified: Fri, 14 Feb 2025 05:14:07 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:1251e7574e214e7b7022475238cc4527c28826e8c2c07204647735316cfd7c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73264136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e55cf7ec6b8902a45b5c36f9043f70f41816a7753d07438eb34fcabe2ff0eca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 15 Jan 2025 08:47:48 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 15 Jan 2025 03:01:25 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 15 Jan 2025 10:06:18 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 21:25:44 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 21:25:46 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 21:25:42 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df9d36d8de7098821c518291549b46c279424dc339b2da655e42c88a93a214e`  
		Last Modified: Mon, 10 Feb 2025 19:35:11 GMT  
		Size: 31.0 MB (31000989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e43f72402a8544ac8a8358f26a470e096d8b0a4416c1d930f95b5531cbe553`  
		Last Modified: Fri, 07 Feb 2025 22:27:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48910cdc7c38676ed7d29cd41f54ee4ed652c0aca4f5dc6fd36fc0ba57e72ce6`  
		Last Modified: Fri, 07 Feb 2025 22:27:31 GMT  
		Size: 1.5 MB (1518474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dac6612285e15c9017337237de7aaeea8529a6bf8e4525205f29f12a2fbb1b`  
		Last Modified: Mon, 10 Feb 2025 19:35:08 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756a5fae31e1504c538a672d57d4ff44b48aa821391488ebb9982cabb6e6ea1e`  
		Last Modified: Fri, 07 Feb 2025 22:27:33 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:f5e6f63e08366e67f549de343bf09f9d591a98753ec860b818f2fda598a53916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0135a1f3aa7c46d0b4c5cec112b52e3b13d708cfe8a49b8306621fb9cad4a4e3`

```dockerfile
```

-	Layers:
	-	`sha256:b079cd3d901a783779cda17e3e2b07831ee2ad8976830e6756e92eea5d81ef4b`  
		Last Modified: Mon, 10 Feb 2025 19:35:12 GMT  
		Size: 2.2 MB (2156758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c42dfd8576186600f64611749e8918fd7b70fd53a5ca693088199ba932473a`  
		Last Modified: Fri, 07 Feb 2025 22:27:33 GMT  
		Size: 30.8 KB (30758 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:3de176ce49537f78983acb45f370eec1465f56e0253789881ccd6d4dda1c7ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75221980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6d751203d1b8e3ed6e5c6905791abfa78579ba4daeb1b7e3d17f4ac45482ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php" "-a"]
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 21 Jan 2025 21:13:43 GMT
ENV COMPOSER_VERSION=2.8.5
# Tue, 21 Jan 2025 21:13:43 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 21:13:43 GMT
WORKDIR /app
# Tue, 21 Jan 2025 21:13:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 21:13:43 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 15 Jan 2025 04:47:39 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 15 Jan 2025 04:47:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 21:26:01 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 21:26:03 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 21:25:59 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0774f657550ec6a831bbd0d72b777f8d8977a4143f082a39f86537a6691b415c`  
		Last Modified: Fri, 07 Feb 2025 22:27:36 GMT  
		Size: 31.7 MB (31677626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f93262ff5f92b789b5e28a5fbc8a229794cf568ee5c1a3fe803f21245857e1`  
		Last Modified: Fri, 07 Feb 2025 22:27:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5621a0404c4346630297b77ccb90ad199ec5969a33b7cae2c363c4800af9f1`  
		Last Modified: Fri, 07 Feb 2025 14:50:22 GMT  
		Size: 1.5 MB (1525986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1201604993e876f18b05ecf6abdff45d0476cf834899dbbe856643b481b76ce0`  
		Last Modified: Tue, 04 Feb 2025 11:24:02 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b6314112280f82f9a8c69377889d4e36d84d4abd16495353f6c66167f17921`  
		Last Modified: Fri, 07 Feb 2025 22:27:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:9b8e5897e6a59e0262f3c8f7577aeb09cfe9a12c0555758adafd59c03838b005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104537f60dbca84d4e20fd79f14b37e49746c45e815c2ac6a909ce6f313987af`

```dockerfile
```

-	Layers:
	-	`sha256:dd79fd0604808059960a43f80aa3a7559a240f1818a73375ddd02b8bac73ea0b`  
		Last Modified: Fri, 07 Feb 2025 22:27:39 GMT  
		Size: 2.2 MB (2156538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8cc3506acaa83ed74f21f0a15ad7aec58699e896de7e0467599825de60d1358`  
		Last Modified: Mon, 10 Feb 2025 19:35:19 GMT  
		Size: 30.7 KB (30709 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:lts`

```console
$ docker pull composer@sha256:532a83f21938e68debf6efe20ef8852e3871478f3ac660dc5e2a6ac3ae35f6bd
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
$ docker pull composer@sha256:f0c4aa14d051615778cb4725e661a77798ef33527c85a645558ab311b5738afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77669012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5dbbf54b41745e4ee6205c3dfc9a63ccf51c15387ec9eca04ca8dfca900857`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd2e180aa89ecb0845d1628b35579e1eb961f47975c3bc5a05ede5b6d47cb58`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 5.6 MB (5629137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d695b6cf2c8c3fcda26df544b054468a24be6cd41394db0208e3a333f18822f3`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7a3d474383ce078a67dbd96e1b61dc0d0b1fe673292ddc8d689e44c69655c2`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7370e670250547c9c1b145d13d02d6fa20bab3226e296408d9031c6a495186b6`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 13.6 MB (13609848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877e753ed32393f8eb06b7cf17507f31ab0f3db652e55c55ab86c82c3df4bf55`  
		Last Modified: Fri, 14 Feb 2025 04:09:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d0fa737a71d88d348cb60ef0ff16ef4df36a45dddcd8bfe55e07d84f69a6a`  
		Last Modified: Fri, 14 Feb 2025 04:09:21 GMT  
		Size: 21.4 MB (21352652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bf998db890f8e3ee8a94d02d3ea220e376efdd8371bffcc8379ce3ed9eee6e`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280727407916ee60ca49cf4ea07ef8f4b509704188598c3a99b973502ec133e3`  
		Last Modified: Fri, 14 Feb 2025 04:09:19 GMT  
		Size: 20.1 KB (20058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b2652210424f810ea67526bf4062b1a031c969b4f4c54ce1528605f2464fb3`  
		Last Modified: Fri, 14 Feb 2025 05:14:42 GMT  
		Size: 31.9 MB (31907474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2809196acc2a093ba933a0704d761289634b1c288685c331846b161047c7b8b9`  
		Last Modified: Fri, 14 Feb 2025 05:14:41 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f36432fc0ed7d14bddcc5646cec2b1a4235444a8e2a153e74ef66b1f8c07bce`  
		Last Modified: Fri, 14 Feb 2025 05:14:41 GMT  
		Size: 1.5 MB (1503263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a76d6110d4b8009bf12ad19b123915dbc8fc904b7807f53cd517e2828c2017c`  
		Last Modified: Fri, 14 Feb 2025 04:10:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a308aa26c90af5e9ab5ce1383dc8f8979d843bea9235b3686d4936b5500f3c46`  
		Last Modified: Fri, 14 Feb 2025 05:14:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:4f1dadd55e175019d7cc711173b386040bb8b2859bd746c9938db919c7d995d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea24f23da4df8cd4440549a9c6fb99274c0926e94db8753f310043c6ef45bf7`

```dockerfile
```

-	Layers:
	-	`sha256:af3877ad7e6f0510d91d1a90015586580cb1575eb6a6c0b42c39ee471d5ad5db`  
		Last Modified: Fri, 14 Feb 2025 05:14:19 GMT  
		Size: 2.2 MB (2158959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5862b4ee9f0ab5e70d59074f775367b3668ff1494fe3ce8b8df3c3be5486827c`  
		Last Modified: Fri, 14 Feb 2025 05:14:19 GMT  
		Size: 30.4 KB (30406 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v6

```console
$ docker pull composer@sha256:fd8cdedc4172e0957aba29baf887f821a48d0361c6c160379e04f4f6ddc28683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75878817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b343a1ac5a7156be409d4a847d9ff224d87a19234ff1bc58f507ea4aafc9d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 15 Jan 2025 01:25:26 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 15 Jan 2025 08:46:52 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 15 Jan 2025 08:46:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f6b305cd77dc6b597a3169970fd07b292703741539eaded2551c0d9a9a3ce2`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 13.6 MB (13609882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45767d1a2e12eb03ad18b9a7888cfb876903b7b27f5e22317a9a419e6c9357a4`  
		Last Modified: Fri, 14 Feb 2025 02:36:56 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b187df6e200be4ae6d666ab1d197a76dab384b63436f2df83f864d48fc6190f`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 22.4 MB (22402333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15e817c4c3f6223fc729a85f3b2dc3fa7ea9c2a3bf884f218dee6205043c6cf`  
		Last Modified: Fri, 14 Feb 2025 02:36:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45820a47f5394522a107e4a692c1e0d3689a29363793dbbf16751ed29bade6`  
		Last Modified: Fri, 14 Feb 2025 05:14:24 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc07fdd9ff35b65c886cb11f76394f3a6058bcc6ffe163f41c4b09e0855ae0`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 31.6 MB (31601043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0554a9e2a4103b0bc17495a139a3314d3e4b40b4bc9ac6728a33ff747fe0226a`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2c6d22e6cb45ad8fe1e004994403d03184c67120c910fe417858670f6f2c44`  
		Last Modified: Fri, 14 Feb 2025 05:14:51 GMT  
		Size: 1.6 MB (1576438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99643eeadc4d99bb5e6a1301f4dc21f9e56d921ef5997336e27c86e87d0f9ecc`  
		Last Modified: Fri, 14 Feb 2025 05:14:51 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b676d253fd81445f66316f17638c8535f5f6e70b4bac3ebc82a2fac5ea8e42`  
		Last Modified: Fri, 14 Feb 2025 05:14:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:4afa1b5b0646a1e830a9c645095200552e09cc4de5c431dd1ce96b96cd433f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ad16d5a22c906e234ed6e72952e446422d345c669b0bf4828d82d2fcf3d08c`

```dockerfile
```

-	Layers:
	-	`sha256:57672a6d7573431a39531c673049efe82d0d61c33b76981b609ee01490ed71e7`  
		Last Modified: Fri, 14 Feb 2025 05:14:21 GMT  
		Size: 30.3 KB (30285 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v7

```console
$ docker pull composer@sha256:69262ed536c424bf35b643cc1218bd871f6cac924fa7bd336cb602b88de738db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69325138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ad888b3d1c457c7ae159a5e3c4f7416925809f872276700bcd435dca7e444f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 15 Jan 2025 00:28:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 21:24:38 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 21:24:39 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 21:24:35 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b02f56cd79bb67b2e6a8c6a2926c13febe08627a14d51ac60cca77caa0bd9b`  
		Last Modified: Tue, 04 Feb 2025 15:48:01 GMT  
		Size: 30.2 MB (30150807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a36ded2ef8fef32700c53fb042e1d25e6c4b243e0eaa2fa4c9987aa4de12ad9`  
		Last Modified: Tue, 04 Feb 2025 16:45:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8877520556df2c3c03fddc4c926da1061cc2bf6a1ed40860757b3fbc67043aab`  
		Last Modified: Tue, 21 Jan 2025 23:27:58 GMT  
		Size: 1.3 MB (1336858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4585a7c436930e2831d2f35f65ecc2b0fe98f70f8bf63d7a021e5d3dc038119b`  
		Last Modified: Tue, 21 Jan 2025 23:27:58 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c25a086e5da415d9eef81f7323ed71254509a257d27a35807dd779a852941d`  
		Last Modified: Tue, 21 Jan 2025 23:27:59 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:d4b78f6324390ee58fb4aa2856ba0e42e4fe4941c11e8c32b78c5665e61d7ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e11de3c0c6051bd089bee76130d9859f57ef90701d22d4024c443c55e6d973`

```dockerfile
```

-	Layers:
	-	`sha256:5d3c340a4b67be3704f9f08b01d9b8dfa9aa11dfcc9c489e675873bc190baa8a`  
		Last Modified: Fri, 14 Feb 2025 05:14:22 GMT  
		Size: 2.2 MB (2159275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d172b3fc0308d5d978f7250a8f84c1b2060da92060b6406e0cb6cde75c892a2c`  
		Last Modified: Fri, 14 Feb 2025 05:14:23 GMT  
		Size: 30.5 KB (30500 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:8206dde757aed98a686f4711ce738df19fba91095d7f839b49ef4221eca3c903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78947087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207ee801aafca6b6b728e0d87a301ead2a7d14f45b0b9ac6a903ca017929c3e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Tue, 14 Jan 2025 20:34:52 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Tue, 14 Jan 2025 20:34:51 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf60bd0bee7688614b1af07694e9e862a6e468345b4d8c1274b901e3308d850`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 13.6 MB (13609906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5935d74cc4f8900f9fe931cf198c384636eccfe5b27fcf8222bad1a34adc3c`  
		Last Modified: Fri, 14 Feb 2025 03:03:44 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3dd78614141a7cf92fd59b8e7fccf1f50faaef52fe4a0a661d5b0d846a4ea`  
		Last Modified: Fri, 14 Feb 2025 05:14:49 GMT  
		Size: 24.4 MB (24449108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eb61917bf0624ecf3420f926f6053b48728486c0188ada2088cb4c8939857e`  
		Last Modified: Fri, 14 Feb 2025 05:12:47 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc28a76fb7622bd8689c33b509f275a2d2558a77eccd18f266bc3ce660c7deb6`  
		Last Modified: Fri, 14 Feb 2025 05:14:37 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7df60278df6c56d8ef9b2df595e68e15a33c291bf23b297f3ebb680a74161f`  
		Last Modified: Fri, 14 Feb 2025 05:14:54 GMT  
		Size: 32.0 MB (32009162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24085d57bfcbbba22355b95422cdf2ec94dde42b3fed500ec739e6f28f614030`  
		Last Modified: Fri, 14 Feb 2025 05:14:39 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48d27b78cc2eb4a63b29b6626fac324c0f6707164a18b71e55132f54ce24c9d`  
		Last Modified: Fri, 14 Feb 2025 05:20:56 GMT  
		Size: 1.5 MB (1534120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39627df935107010c348c87049d8237cececbdcda0872b9f5d8de2f3b0a37c13`  
		Last Modified: Fri, 14 Feb 2025 05:20:55 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516723aad7f0ef09c8c93c3992c06f09fab814707eb39d564dd12aeda395012f`  
		Last Modified: Fri, 14 Feb 2025 04:43:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:64f990ea8e8379f655a0307013a12b575d30075faab92c030d985298c62d7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2044753fcc5302e04179c5b25764062da71481a56268c93eaabd69e6b081aaf5`

```dockerfile
```

-	Layers:
	-	`sha256:6a92b3addaccbf42e9455a86fa2b8fa606629bcbf42aa3246dbe97cb5885704c`  
		Last Modified: Fri, 14 Feb 2025 05:14:24 GMT  
		Size: 2.2 MB (2159099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cab56e06cacf87bbb81ee2af9cb52a26600ac8ca68546972b3a26e538fcaaa89`  
		Last Modified: Fri, 14 Feb 2025 05:14:25 GMT  
		Size: 30.5 KB (30528 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; 386

```console
$ docker pull composer@sha256:999c0084291ba62f0f8ca4bbf1e7baa7575140d15953f831d5a1fd1c0ebdee5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78369510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5ec57258189923eb3156405638275f1e0a7891710f0fbb132e988b4d81e017`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c4f61d7599e7869ad3a9d452f69e9bc3899f18d70701124026229667c57db`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 5.5 MB (5479161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb08d2bfa2365278e7427cd03c6a3b6d0d200bf048c31056c211ff6bd1d83e3f`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ccac1acad29397cc55b48dcff4f9ee2a1ad8bb562aefc4e7345e5ba177ea66`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77470d2cfb3c06673c0297f09fdcfd1debad3d8c75b8f08ee1be3f66d5edfb5`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 13.6 MB (13609860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56194a5a61ce8b305a5554d8aff3980c32fe8df11e9dae038a5c1169482a4dff`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb641c65fcb36b09714fd6d6634df4fa431b7f127829dd93eecb97dc6d4674`  
		Last Modified: Fri, 14 Feb 2025 04:09:09 GMT  
		Size: 21.9 MB (21875599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8652ddf39bd8a77eabbc758325596a213cfa201e124d3a8e14c0d3fedbbe920a`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7c976ea7a0a95cb41a13dd1eff7887ba420c913603c766514f637eb3933a56`  
		Last Modified: Fri, 14 Feb 2025 04:09:08 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4c75ab9d6ee0dfba786eef4b37c96f36b47af6393fc9f1ad54103fd0a0401`  
		Last Modified: Fri, 14 Feb 2025 04:09:44 GMT  
		Size: 32.4 MB (32391404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307c85cb9cd140a46bbfe9a5836b595d4ac469d955bcf947e382f9caa5fc7084`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db737518c7a1321b9524cc0c806f0209cf67adcb9fcc4b7217276cbc11757dae`  
		Last Modified: Fri, 14 Feb 2025 04:09:43 GMT  
		Size: 1.5 MB (1525424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30078a4cf8eb3b57398ebe7bdb98b7968f346e86e35c11f18f88f86b5627002f`  
		Last Modified: Fri, 14 Feb 2025 04:09:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991f4051ab2bc9b427dbc31f39e35232e46b7de196f743bdaa8cbae6e807bc3e`  
		Last Modified: Fri, 14 Feb 2025 05:08:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:714c86b48fc46c11adcbc3be0a341f67988e1926c3bf1ab2a7db467b8ec8da06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c187481d326d5839a57ecdd6925a20fb3453363b9a625e05a7ae18436fb24a3`

```dockerfile
```

-	Layers:
	-	`sha256:c23283967f31fbb19c6378629aa097894d319272ca50bb5fd3b31053706f695e`  
		Last Modified: Fri, 14 Feb 2025 05:14:26 GMT  
		Size: 2.2 MB (2158747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfa1bcb19012e00c05e5045b17ccc615bf33c5d0aa49d1ba0c21f7aa8336ee4`  
		Last Modified: Fri, 14 Feb 2025 05:14:27 GMT  
		Size: 30.4 KB (30375 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; ppc64le

```console
$ docker pull composer@sha256:743027019d96c877d84aa61c5ce7aef783fd026f77eda0a166fc75522ffcf5ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80605406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c38d47056d72c55662503db96ff53dd2305b537d0431d9ed36cac6409de427`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.4
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 15 Jan 2025 04:47:37 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704aa6bd4f8e770473b08a863515e74229b7563d9a2694d4dcffebd63189d5ab`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 13.6 MB (13609905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43c7e0504550dd35c7e6f3c1f5c61ed5db00067d11ffd3741e8f23b0dc16660`  
		Last Modified: Fri, 14 Feb 2025 05:09:58 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1167c96dbe49f246b96adc095a28edefcc2fe61bdc39108f8050c176699f483b`  
		Last Modified: Fri, 14 Feb 2025 02:47:38 GMT  
		Size: 25.4 MB (25398061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e16862c42f1028fedb8b04c6b22bd4e945a213a3e5a113872b385ee049f719`  
		Last Modified: Fri, 14 Feb 2025 05:10:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10f990e07f31e3d864671985a77e555905c511508a842be3262c8c7b9a96ec9`  
		Last Modified: Fri, 14 Feb 2025 02:47:37 GMT  
		Size: 19.9 KB (19884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e260f2e53edd998f9cf2d3ba59929e4a7ff0f39075889a9b99dcb55b35732a9`  
		Last Modified: Fri, 14 Feb 2025 04:28:17 GMT  
		Size: 33.0 MB (32950697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717745514d5555d6812144710631aed2946af2ee5c721b80f8bf0a8b750bd43`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839b07734abbe604a248264e5a9a2d440af3d7f32c9f2928a57847906c8be3ef`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 1.6 MB (1572043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5aa094a9e0da1a27d70cf9067c5ffbf2326afb56c6fa64619136b6a617abf49`  
		Last Modified: Fri, 14 Feb 2025 04:28:16 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221496d3f16797dd0e2ba7577369c12f200df6ab91b13afc68e0ed7d2e163c96`  
		Last Modified: Fri, 14 Feb 2025 04:28:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:68f0a3d147944d967eb5dee4bfc61d87b40bec3ed6de9f85b95315fd0dcad507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5638e372becc7a921458207568a965b1410ce28fab67b76a96d6f21de2cecbb5`

```dockerfile
```

-	Layers:
	-	`sha256:a679d6f0d86afde37505cbf319062251c0020159c4478c42a816e86c60428ce6`  
		Last Modified: Fri, 14 Feb 2025 05:14:28 GMT  
		Size: 2.2 MB (2157516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc9e965651ca366ccba635569d99334889804e89c90ca37dc792085a67f4b4b`  
		Last Modified: Fri, 14 Feb 2025 05:14:29 GMT  
		Size: 30.4 KB (30448 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; riscv64

```console
$ docker pull composer@sha256:764fe74ca6e879974d10f5b7d3af8beec53548826daddd27e610ae6c42fa19a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73124201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f54e3c0524d785db83b0e4d4801888c184dae4f032d625ca54dce9c63d39c76`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 15 Jan 2025 08:47:48 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 15 Jan 2025 03:01:25 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 15 Jan 2025 10:06:18 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 21:25:44 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 21:25:46 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 21:25:42 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df9d36d8de7098821c518291549b46c279424dc339b2da655e42c88a93a214e`  
		Last Modified: Mon, 10 Feb 2025 19:35:11 GMT  
		Size: 31.0 MB (31000989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e43f72402a8544ac8a8358f26a470e096d8b0a4416c1d930f95b5531cbe553`  
		Last Modified: Fri, 07 Feb 2025 22:27:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da46c3558a85c68b99a1fd16fe1d5e2df313e50486a17d6664eeb9f16ee7ec62`  
		Last Modified: Tue, 21 Jan 2025 23:33:06 GMT  
		Size: 1.4 MB (1378538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282976d95725176508cc2d12b9917b3a676652d8968c63950552f9ed28c2bf10`  
		Last Modified: Tue, 21 Jan 2025 23:33:05 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6827e80ba34f5e7edde2644e1d74019eb42d77685533efb9933bae5de735a14`  
		Last Modified: Tue, 21 Jan 2025 23:33:06 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:897867ea4f27a79d5dde711f6cf259e7a9e6427c72fc4c1afd434182e6dc4bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bc3fe69a3f94ef5f84b8f3c09aa0c99c01966b85836048a8decf8937d27d8b`

```dockerfile
```

-	Layers:
	-	`sha256:6a9105a5b44ae05153ca58d6957c944756b462378ee992f30d257ca4fc574a83`  
		Last Modified: Fri, 14 Feb 2025 05:14:30 GMT  
		Size: 2.2 MB (2156458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8392c83bb5ca74ac2536da484f476060e0576df4291fcf2a36506693e7c16abb`  
		Last Modified: Fri, 14 Feb 2025 05:14:30 GMT  
		Size: 30.4 KB (30448 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; s390x

```console
$ docker pull composer@sha256:514b1702cd4a4e313e68efb932d1a34e62b5c54c49f0c2465c5dc7fce4994a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf86f0e4de62e927c746bd82826435184b467d536480050009788ae69f9a9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
ENV PHP_VERSION=8.4.3
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 15 Jan 2025 04:47:39 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 15 Jan 2025 04:47:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 21:26:01 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 21:26:03 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 21:25:59 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0774f657550ec6a831bbd0d72b777f8d8977a4143f082a39f86537a6691b415c`  
		Last Modified: Fri, 07 Feb 2025 22:27:36 GMT  
		Size: 31.7 MB (31677626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f93262ff5f92b789b5e28a5fbc8a229794cf568ee5c1a3fe803f21245857e1`  
		Last Modified: Fri, 07 Feb 2025 22:27:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9b2a0bbea2bb78104414d4305d0086cf64327d3c0a3ac678ac07b3d8afcc7a`  
		Last Modified: Tue, 21 Jan 2025 23:28:29 GMT  
		Size: 1.4 MB (1383351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3588ec3a1e72affeaac950ef30c1d99805230b13e773b9aef96652b945fa2141`  
		Last Modified: Tue, 21 Jan 2025 23:28:29 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b453745dccd0fecb39882a5afda7d8b34c942c7048c521a6513882466445da`  
		Last Modified: Tue, 21 Jan 2025 23:28:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:4fb4eaf35b8643843c6417cae1d72c654de0fbe0df2b7de4035367e4a39a4ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae841eb0ef743268cf2abb58eff2284437ad4a7923cb5f07dc868333bc2ac15`

```dockerfile
```

-	Layers:
	-	`sha256:f2f0d9b799b6bc8b7b0408409d0c4c0472e83ee8a40d324f34f5ae17c2fecd2e`  
		Last Modified: Fri, 14 Feb 2025 05:14:32 GMT  
		Size: 2.2 MB (2156244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be5f436ba87454a77d39c8729483d37c276b96306136d5cd9081d576dc12dae7`  
		Last Modified: Fri, 14 Feb 2025 05:14:32 GMT  
		Size: 30.4 KB (30406 bytes)  
		MIME: application/vnd.in-toto+json
