## `composer:lts`

```console
$ docker pull composer@sha256:21b5941afefb69dbb626e77cfd1c97fc5a7e9b6b9b6bc365996f83603ee6b633
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
$ docker pull composer@sha256:c55bbcc0b5116f3ada5b2b794253e8d642d534800f5d711ec781a0631a511b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79153683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bfb9c90c0dd2a8370857b01de5e68a396844fc9b3eb4036bcee5238053fcd1`
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
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
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
	-	`sha256:0b94662290ef2237915af922ad14ae2b406eccea26d9201aa949ea52f20b737f`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 5.9 MB (5944403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a67832465ef6dae00170ccca088bdbc63d05a197e0ba1403442805169a06a`  
		Last Modified: Thu, 03 Jul 2025 23:04:16 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53785dc48fc021d1c3f9c46a776ead61a024377fb5e6ab592908501762d63a7`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c87a7802578b0a5aebb57ffea8e543a2d50cff1ec6ffb0941fe8ad61b3a9e6`  
		Last Modified: Thu, 03 Jul 2025 23:04:23 GMT  
		Size: 13.6 MB (13647262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aa21d09531523ae5c279a8b0eb00236af3b192f428c934050c61f7e1611eaa`  
		Last Modified: Thu, 03 Jul 2025 23:04:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fccbfd125531b00b24f5c4c9c182e17714478e55b96701b7e71d30f7f70f9b`  
		Last Modified: Thu, 03 Jul 2025 23:04:28 GMT  
		Size: 21.0 MB (20971251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481b52666b981ec99f99b98b64ef13ff6ce799950970b68817767c966318dc11`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a3724a01f76e5128bdebeeb89d8f42b63b2e987403c91e1f1f5c084c63ffee`  
		Last Modified: Thu, 03 Jul 2025 23:04:22 GMT  
		Size: 20.2 KB (20205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755a5679cebfbcec196508684d58f3d3479a8923825702cea8057be9ea0509ea`  
		Last Modified: Thu, 03 Jul 2025 23:04:25 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c852688dfb4eb3338fa2b359258f4def968d8542cb467086d1eeea1f28905a74`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 33.9 MB (33928299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c622ee0a80d81cfef14283072f36dba68467de22ad3d6eb6da4af6de1560b45`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46b6d68b19d40cae9d582d523d29cb5445750042c67b4dcd85a60dfeed7b1d`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 820.4 KB (820361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977cbab4acac7e284670ad25a082da694101e85439356ae5286a8f42f5f31dc`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86faa8ac4003596a871ab1662361aac1e1c5201c5cfc449f82586191cc1255f5`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:c559a7d2440eea7f5c9fb090622a49108e7ce577a37fd104b2a86b33e73d37b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6da2df0aa7c1b16267d729ffc7881169798d1c7d7c0d658c344b4e2eb72c10e`

```dockerfile
```

-	Layers:
	-	`sha256:9f3f5251f9a561a4d427ff51a3736e50496fc6f56a1a01f7892baa753af2a16a`  
		Last Modified: Fri, 04 Jul 2025 01:13:55 GMT  
		Size: 2.2 MB (2175046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f9403682c82b56933aafbf66ffbb44b9473316fa9703c0243d322d72269fab`  
		Last Modified: Fri, 04 Jul 2025 01:13:55 GMT  
		Size: 31.3 KB (31348 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v6

```console
$ docker pull composer@sha256:e2b50196a498bf516318301d17e1754812c652b1cb1b4aef8bf98a89bd1bd148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77469333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bad0aebd938e64f2f9d6c7ccaf6c85d7415bb322ec240b81eabfeb48d741c3`
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
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
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
	-	`sha256:5b4a1a48d371204daac6d50cf0ade3fcbe953b7326556c347d0834eeb808b22f`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 13.6 MB (13647232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7209fb73f851518e0fbc85b54004a573116286207c48ee96ab37833cb8ea1353`  
		Last Modified: Thu, 03 Jul 2025 23:00:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698dfdb6ae14586a077f81a7e7531ba3d394ab385475ff9c6573114a36ad047`  
		Last Modified: Thu, 03 Jul 2025 23:00:25 GMT  
		Size: 22.2 MB (22216193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2822e518605b3410372bbcdb567b3220dcdbe3fc3a85d76aeeed7414a97ce84`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc23f56a1dfd1eb937c6d0d63cb116029d4ac6193e3b8e0487798f7859b09cf`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb672fb64a4977b38f156870ac6fd28ad3898b39594ead2e5d7a7a25cf62e07a`  
		Last Modified: Thu, 03 Jul 2025 23:00:24 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f65dda0589cf68df6c1f7a31f2ed36448fe5ac89816b32bef12a62b39575a0`  
		Last Modified: Fri, 04 Jul 2025 01:07:05 GMT  
		Size: 33.8 MB (33807127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af16e8c9f29c59fdf9ae69e6ad7a7f42c68aea017b14dcf169ea15f538efb4e`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a14a438fbcc90ca30c5c0ec991fd8be0c7b0045bcb84a8024e31659a0d3b48`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 820.5 KB (820527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b158de7fb3568a394e48de871c0ea3498efb3301159509001ed1fd223c54d4`  
		Last Modified: Wed, 25 Jun 2025 22:15:59 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54c6b7690f712d9ed6c572e55edda2a4f98703d5ccf8231cdcc9464c367027`  
		Last Modified: Fri, 04 Jul 2025 01:07:01 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:e685378f23766e35af132e6630f24e30d2bf9d499dd7eddc7137591a01ed6753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4222e1dceb530beb0faf6358b42874b5eb34aa6b58bf897d879f22afcd42c1a`

```dockerfile
```

-	Layers:
	-	`sha256:bc7ebbfd707900fd28ec922eab6305413e75e3662224a563f21ae914c3e88644`  
		Last Modified: Fri, 04 Jul 2025 01:13:59 GMT  
		Size: 31.2 KB (31227 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v7

```console
$ docker pull composer@sha256:2e623f99c3c86adb687d3c084ade6d57b8c0de8f3f097bd533977c3506625aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71099745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccf3817f2274639589622c73db5c5f203163bba6bc26445c9771d1115731ef8`
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
RUN docker-php-ext-enable opcache # buildkit
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
	-	`sha256:6bb43a513cc6b21818dbb94e80c2111720a53640ed898b33c7d23eaf2a793b99`  
		Last Modified: Wed, 25 Jun 2025 19:30:30 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bf5f26db369cad64f7244865d73d36a09009ff4cff9337925e0bf1233f4f81`  
		Last Modified: Wed, 25 Jun 2025 19:30:30 GMT  
		Size: 20.0 KB (19998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de1b077491f1ad27d0d36553c589646b18751891cc03f34a6852b7d7036aeda`  
		Last Modified: Wed, 25 Jun 2025 19:30:30 GMT  
		Size: 20.0 KB (19990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7950499433d748460b045565809e870c5e47ada373f7e5e31bf6726f728fce`  
		Last Modified: Wed, 25 Jun 2025 21:53:12 GMT  
		Size: 32.1 MB (32070108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f777ef2db19334ec21f12f9572d4c04b4b44685fbd57f4831a51d4895c7ad1`  
		Last Modified: Wed, 25 Jun 2025 21:53:08 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd9f45b2b68a54ae7311c41435a17c3e24c3896ee734b5b6f964b33560b2ae3`  
		Last Modified: Wed, 25 Jun 2025 21:53:09 GMT  
		Size: 810.8 KB (810819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dff55f28e8e3546642ae9af35ee298ca586e46f7c319c686ed265277ef0c530`  
		Last Modified: Wed, 25 Jun 2025 21:53:08 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31640281e627c347a4fd2b2e78a20706f34f25f416ca908375783b9c4ccec07`  
		Last Modified: Wed, 25 Jun 2025 21:53:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:ea9f19d3b72c7c5388362d67c97ec0fab326808180a721ade5ffa524e01918a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776f8f76eecaae9c41c05bcdd8ee025afb84d8db4bf2fe891e39d066d170e5bc`

```dockerfile
```

-	Layers:
	-	`sha256:c929987a1efcae781df1e53d0172a22ddffc58aefe31c61b134ca6f23ab7541e`  
		Last Modified: Wed, 25 Jun 2025 22:14:36 GMT  
		Size: 2.2 MB (2175354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2758e4c6b36af23b93b7180d4d41969ca84cf6f3fdbe73e79fba8c823d07198`  
		Last Modified: Wed, 25 Jun 2025 22:14:36 GMT  
		Size: 31.4 KB (31433 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:8f286e6030c88da3ebf654805893416ce91c0ff0b6c587922c758719addd7866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76642077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7fc2bfa74eb8329a653fbc48ce981ae1b47ba41c1dfbdf3bdc798f246890e0`
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
RUN docker-php-ext-enable opcache # buildkit
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
	-	`sha256:5d74afa414d93be74315fb2fbbededff31189950343736eb9412b26b4f530d1a`  
		Last Modified: Fri, 20 Jun 2025 19:32:29 GMT  
		Size: 3.5 MB (3470712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91ea4522a211c5e50ab5b22083b52449e7ad38398a1f6e5dad24e4a62961906`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b695911010ae65b6cf4c4b5ac350b27932e3b4b29077f6094baa473db50fb5`  
		Last Modified: Fri, 20 Jun 2025 19:32:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2341d4b1828e7c29626f05458e9c7ac77b849f7fa211122c5e49f3db640c2`  
		Last Modified: Wed, 25 Jun 2025 19:58:30 GMT  
		Size: 13.6 MB (13640504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214385dee2a6502125f514cfafec9ffbab10a83686ed1edebefbe13bb98e0df`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2192f9a8f7dc985e1b1534af7a423269d9525cd446882c0b66bc83bd73c1d`  
		Last Modified: Wed, 25 Jun 2025 19:58:29 GMT  
		Size: 20.5 MB (20519110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7813f4e30ce21280209e560b03ffd244261e042d03b4f926c87197d856e4d07a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5659da52250b6def060ce2459caf69d028600439407c5609ffb01e17d290d0a`  
		Last Modified: Wed, 25 Jun 2025 19:58:27 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed11a0655a2eb0f0eae0b13f815d1385ec0d4bc0fc0d3e23f5c2e3aed8e1799`  
		Last Modified: Wed, 25 Jun 2025 19:58:28 GMT  
		Size: 20.0 KB (19987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db90ec20dde1245e26657e9eeab7a68a4f381ea6442f98f105cfc54ce54e3a0b`  
		Last Modified: Thu, 26 Jun 2025 00:27:56 GMT  
		Size: 34.0 MB (34010879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb4fdb28ebd43bf90c0134d109bd7f9e79aa657ab4e9e040a42ac1d008e71aa`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6ec42a724f2aeefbcb1a20585daef187b07891cf75207c6c8db8117c63f9dc`  
		Last Modified: Thu, 26 Jun 2025 00:27:53 GMT  
		Size: 820.1 KB (820096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c471c3b23b3d1c864515b5a0b7cb90ce65eeeab79a4a63f4124a62b97d0a47`  
		Last Modified: Thu, 26 Jun 2025 00:27:54 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86049f63a03e6d1fc9d7a24051761f819a9295c93f7a01b04a0aa6399c11a3f`  
		Last Modified: Thu, 26 Jun 2025 00:27:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:cc3d9242f043df599446e6c0b5e5f1a301af00ffedac8d01124c669a5f4fbc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7786c5b0b76b9606b04ac037989fe51ed5022aa69503163ea017ac00f4988cc7`

```dockerfile
```

-	Layers:
	-	`sha256:0a7c6843ff21da43780c0935db32f4b4a9f1781127257f6fbca18f55263c549d`  
		Last Modified: Thu, 26 Jun 2025 01:13:57 GMT  
		Size: 2.2 MB (2175178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75d88db614b9377920d6ef117f33d1dc25945865090eb46f2ebed565a1843b39`  
		Last Modified: Thu, 26 Jun 2025 01:13:58 GMT  
		Size: 31.5 KB (31461 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; 386

```console
$ docker pull composer@sha256:3549d1950413df9cf9ec5dc3cba56b8a4003b398f6aaa586dabe82fe4561687e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79886978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f414549109ad3eaf016596d8b177151fdd48b457782dd8dd896c90ef88a8d3e3`
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
ENV PHP_VERSION=8.4.10
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.10.tar.xz.asc
# Mon, 12 May 2025 11:49:32 GMT
ENV PHP_SHA256=14983a9ef8800e6bc2d920739fd386054402f7976ca9cd7f711509496f0d2632
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 12 May 2025 11:49:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 12 May 2025 11:49:32 GMT
RUN docker-php-ext-enable opcache # buildkit
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
	-	`sha256:4579a4802acae62f9995bc4ca35846cfa477f9a889ce0fb2017ac6630b78bd4a`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 5.8 MB (5806973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57074fe130dea7f1367879dc4bc435c31dce84ecd32b48ea0a63d35b4a08b836`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7e9cf52dab21b2f526412767a5e92e23eeb507ad11d31f9bf4391ad5eb6a66`  
		Last Modified: Thu, 03 Jul 2025 23:04:53 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee47d22d22648a57b652a67b201fb0e169513c91be3eec67cb726ba70e375a83`  
		Last Modified: Thu, 03 Jul 2025 23:05:02 GMT  
		Size: 13.6 MB (13647238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ed9c7929ede2d39288b5cdc1a881693463f9694eab366fbb269e70c0d92a49`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b1c24d7566d919e950b1eaf0a78b66a3bebc8b853f7dac99909776dbae0f1`  
		Last Modified: Thu, 03 Jul 2025 23:05:04 GMT  
		Size: 21.5 MB (21500663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f235298ca3bcb11577f52427a9e9abe5f5708168ce3e6f7a92e3516e12f33f6`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3069db4b5ea73d2b8c2f80770d98b1ecf8fc539f7fcb87b04c2a4d4c1d2747`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af93b74a51d1b8b0d9adaa24d025147b9bbb65f3dea67b796f0959416093750`  
		Last Modified: Thu, 03 Jul 2025 23:05:01 GMT  
		Size: 20.2 KB (20192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8afe5fb2921fe882cd785fafb8a340bc48fa984eaeb95084167790e1303e977`  
		Last Modified: Thu, 03 Jul 2025 23:12:10 GMT  
		Size: 34.4 MB (34436630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f1c0fa4f5c61d324236c0742a29d9c95bfd3957e20bf4b0b2737ca6d553db7`  
		Last Modified: Thu, 03 Jul 2025 23:12:08 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a0f472aa74942d9a4ee3c0864e5be87ebfd153fe0626ec341f9e4bf8532dd8`  
		Last Modified: Thu, 03 Jul 2025 23:12:08 GMT  
		Size: 834.2 KB (834207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4accc71185fa51ed185fc3226e03f27c8bf432a8af67578471b49317a5d6f501`  
		Last Modified: Thu, 03 Jul 2025 23:12:07 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d8365033a3cd146c7ce81b6969d385bc6830b8b0e7b79f9b8178fe789738e0`  
		Last Modified: Thu, 03 Jul 2025 23:12:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:78d5e6ade889c8d8ab29ae66c8b2c10b66b6e8ff4c2d587f7b6c704c44bbf784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b7cdd657a2cd5660845907325e60ef43285c10450db487f79e4f039bec77e1`

```dockerfile
```

-	Layers:
	-	`sha256:fa6faf45644f32be1508f47e007d90b37c699e54e366da94d5110b2450da5b12`  
		Last Modified: Fri, 04 Jul 2025 01:14:11 GMT  
		Size: 2.2 MB (2174834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3844137036bf9a81ac64e5bd8df05c0abf34b7d05ae60974c75f020d99ff72e9`  
		Last Modified: Fri, 04 Jul 2025 01:14:12 GMT  
		Size: 31.3 KB (31316 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; ppc64le

```console
$ docker pull composer@sha256:17d990ba91733dd4a66c9f750c1f78b9cfb96e69d86f3531d5ed41e3065f5692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (79014944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a53fa4034ca3e51ceab8126b31845df459db3e2876176c79dbdd51daecc4fc`
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
RUN docker-php-ext-enable opcache # buildkit
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
	-	`sha256:d5b6bb6879849aac5b27aee39d2d94016f30c04c04f58ec31d2a54cdf9b9005f`  
		Last Modified: Wed, 25 Jun 2025 19:28:12 GMT  
		Size: 21.9 MB (21874143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0153508085a0eccd2c5a479136b3a5818dc0af2a9f519301ecc29d9e3ea57c`  
		Last Modified: Wed, 25 Jun 2025 19:28:10 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cd469cdf896f3397244a1ba52aacfb3295f1bfc89e70e4f7bc4f67113384f7`  
		Last Modified: Wed, 25 Jun 2025 19:28:09 GMT  
		Size: 20.0 KB (20005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a2dae6690e928ff0492599e654c93e0c755703f909cc4adc3e30c7818d0dd0`  
		Last Modified: Wed, 25 Jun 2025 19:28:11 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6135ef8dbfa2274e88b70d78a340a7a056a3ef5e3b93db244516dd86f4451c67`  
		Last Modified: Wed, 25 Jun 2025 22:25:20 GMT  
		Size: 35.3 MB (35279081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10ef8935b1db9be847ef4f62af1feae74b37a7f577c0267b1e6576a80ae72db`  
		Last Modified: Wed, 25 Jun 2025 22:25:17 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a904d7d589aae16460234a34178dfc33c48c5d8df97002c20a9bd6ca339528`  
		Last Modified: Wed, 25 Jun 2025 22:25:18 GMT  
		Size: 827.0 KB (827019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4d6896a690f52e358a10f5abe8da9513e445b6b4520a84da11321287970e7d`  
		Last Modified: Wed, 25 Jun 2025 22:25:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b247e6411009874a0dd07b041bf68e727871c382c9e2101563cbcaa01ecce95`  
		Last Modified: Wed, 25 Jun 2025 22:25:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:4746eb49582e4a29b342e910a2bb6835160610f1855e3ed85eb6327268fbff37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3befd5b44ddd406cd08826f36c629741d02e60a2973af0305be35db49515a0e1`

```dockerfile
```

-	Layers:
	-	`sha256:4b6b14e5466250c8cb811cea0e516b9cc6040d5533f948376a9903050d1e9cdd`  
		Last Modified: Thu, 26 Jun 2025 01:14:04 GMT  
		Size: 2.2 MB (2173595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b7fd1fa67e13798ad6ce9f1e8cb178808583d7cea787710a106d20dfad42fe6`  
		Last Modified: Thu, 26 Jun 2025 01:14:05 GMT  
		Size: 31.4 KB (31381 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; riscv64

```console
$ docker pull composer@sha256:9860f66c267457248e2763c6a09e85eb82ceb877f6d62a9e676ba6c8ae4187ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73116976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8966d79120c2abe2947477d17e117a3104862944b5f4e13ef23367ead908a2c`
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
RUN docker-php-ext-enable opcache # buildkit
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
	-	`sha256:b91ae988832dcf22e179ec800eee279369b0d1b8a4129c2bd761a392671d8d32`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5d276f1eb8afbe6e12101788a8d8d2c68f0875a801fca945c95b68b009ee44`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c69f0ad5808ebac07aefd6d1a9c0933c09e134334a8bd72a2f49fb7ed2297`  
		Last Modified: Wed, 25 Jun 2025 19:18:50 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7d4367f9b25dba1c9057a363403805d1f3ffce81d401bb89eaa3652ee82d83`  
		Last Modified: Thu, 26 Jun 2025 08:33:02 GMT  
		Size: 31.1 MB (31107678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a85da3fdbf5b1c41e6f68043dc7ff3cb2ef316082fa092b6f23657dffda19a1`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7494a442b1a2a3710ab64d55620187bf77c0d16ae5055db9f579c4613fc818`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 818.2 KB (818166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb79f82b329094c3615c093e293350ba5ba421f1a9af75f3edfda9333a8544ce`  
		Last Modified: Thu, 26 Jun 2025 08:32:59 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9e9900ee8d756b449b4fd43c55d64c8e8395d9abf19cefb38fa404c3b7bfa2`  
		Last Modified: Thu, 26 Jun 2025 08:33:00 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:d4dcc48985653e30399123cfa46b169aa591904b480bc2df5ba88df19e87917c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4124f1fb2e0f031c7b2758e04efcd50a6e073195d783b727ba466240a5c7408e`

```dockerfile
```

-	Layers:
	-	`sha256:cc65df97003e1fdf43a52d8ff3ea55f84dfa01ea4c263ceb697e09918c64f9e7`  
		Last Modified: Thu, 26 Jun 2025 10:13:52 GMT  
		Size: 2.2 MB (2171862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f19f57694101dadef618bbb4001a3dda36cac3b1d2a49238a8e065cb866f0390`  
		Last Modified: Thu, 26 Jun 2025 10:13:52 GMT  
		Size: 31.4 KB (31381 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; s390x

```console
$ docker pull composer@sha256:b6ddc3f630dd983a928f7ac2582444f466fabcaf35f1d7dfd286b64b40294811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75141676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6caa476f4608e6b11fbc336b9dd2519f232486b7b3345cb7eec1072ed9bf3317`
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
RUN docker-php-ext-enable opcache # buildkit
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
	-	`sha256:6c50b23d2f6267cb43b11b038938247a74fe9e643b50e59fdbb4b5a4b6fe7861`  
		Last Modified: Fri, 20 Jun 2025 19:20:52 GMT  
		Size: 3.7 MB (3699029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d657aded1e5f64f14aeb2f0fb46bb5042326900e94f375c02676e1df16f2c0`  
		Last Modified: Fri, 20 Jun 2025 19:20:51 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773155ae64957d9bd56f77026e1934533d4df47e0e44a57e52cc2ecc33f78584`  
		Last Modified: Fri, 20 Jun 2025 19:20:51 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d822c9d5a1030ab3c3269394abf80c023151b1a59827d801166b5145f76b4b24`  
		Last Modified: Wed, 25 Jun 2025 23:54:39 GMT  
		Size: 13.6 MB (13640517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9dbb04ef645b5874aa35f37d0b50a07b7dbbb0a077a3a0f90c2f2f7578ada9`  
		Last Modified: Wed, 25 Jun 2025 23:54:38 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdea73576f59da4b4d05095ca8c19d71770f99937b315c3b75175172222a0d8`  
		Last Modified: Wed, 25 Jun 2025 23:54:41 GMT  
		Size: 21.4 MB (21447113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4593ddbf6cac4b48dada192cd7a09c5f448702a71031f89e1d8a28932d7fb1`  
		Last Modified: Wed, 25 Jun 2025 23:54:38 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e0b7d92cdad27b44de8c8a61cd63501a0e95d837956383b28b1ef267e3ecc`  
		Last Modified: Wed, 25 Jun 2025 23:54:38 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340c807aaf9359cb6ac7245e5f7d87b5958fbd2fb2575361ffec01837d86fa1b`  
		Last Modified: Wed, 25 Jun 2025 23:54:38 GMT  
		Size: 20.0 KB (19994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4065e0dec5a76a7d8c20757720e80afea7e9c2bb447e6269b59d660491901064`  
		Last Modified: Thu, 26 Jun 2025 02:57:30 GMT  
		Size: 31.8 MB (31839124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540bfdb510ef2fd1bbe021101fae79eda09626b3b552aa01023f987a111347a4`  
		Last Modified: Thu, 26 Jun 2025 02:57:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a339854206849bd44e1043c5354055e8ce4aead7fac5a90930ef246db6129e91`  
		Last Modified: Thu, 26 Jun 2025 02:57:23 GMT  
		Size: 823.5 KB (823502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09e003982f1052c1dd1d6aabfa0c12e20bafdc0ca473a683a94f375b83fa27e`  
		Last Modified: Thu, 26 Jun 2025 02:57:22 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17e3ea869a00f6c8e561e4ab9a9145c9ca9fcf6744859601e364cfb77ded23d`  
		Last Modified: Thu, 26 Jun 2025 02:57:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:45c183352b4f6173747be9a89d4acb26625f455a404ac29b41d40117e1290218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8185d1796f629095efe8788b0c566d6fa092eeeb9dda7d05d1d34eeab1352056`

```dockerfile
```

-	Layers:
	-	`sha256:1df08c6b6c8e550ddc30007ee70520984a8391c51facfaf562ed61541f8423fe`  
		Last Modified: Thu, 26 Jun 2025 04:13:57 GMT  
		Size: 2.2 MB (2171650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d7ef6ec295b269a38f02238f0f08df9c6e1b676617ecbd15c69bdbc6797711`  
		Last Modified: Thu, 26 Jun 2025 04:13:58 GMT  
		Size: 31.3 KB (31339 bytes)  
		MIME: application/vnd.in-toto+json
