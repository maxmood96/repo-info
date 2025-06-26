## `composer:latest`

```console
$ docker pull composer@sha256:3bb97ebe9a31cc709362b43e0369291bf9dc1edeed0beeb06113df6e4be4337a
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
$ docker pull composer@sha256:22a035cbc3c11dfcac9225eb1a22850b555b0c9c72234eeed74a050653f2e52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76825581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c57fc5e29a7111481b3a6b1621352dc48158192386eaeb9f607a03e35a19ea`
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
RUN docker-php-ext-enable opcache # buildkit
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
	-	`sha256:d94b52dc45b57bdb10adcefbaf15b7407514b6e428c6ff3a204aa3de395930dc`  
		Last Modified: Wed, 25 Jun 2025 19:56:33 GMT  
		Size: 3.5 MB (3468347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b59d780d3e14cb42593d46d17834e9d61fc53a2911c91756df543e237e72df1`  
		Last Modified: Wed, 25 Jun 2025 19:56:32 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b91823d6518dfc3edda879a6c1b4570f00a9904ba181876588dd382ca14f3d9`  
		Last Modified: Wed, 25 Jun 2025 19:56:32 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b85bfbf34452714fdd6bd0b6ae067d4aecd379d026d8a63005cb417e6aa2b00`  
		Last Modified: Wed, 25 Jun 2025 19:56:33 GMT  
		Size: 13.6 MB (13640513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fa75df5070e2bf129ee9a55601fe4aeea9f6733ba7db7e875e0bdf86d5f6f`  
		Last Modified: Wed, 25 Jun 2025 19:56:32 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e596a23157834bb6995c20124de68b3b4709f6f4e48eab120c27d3169ea683c0`  
		Last Modified: Wed, 25 Jun 2025 19:56:33 GMT  
		Size: 21.0 MB (20969831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc997cc1a60339301e41f08fa620e72af007b9ae8e3a6653266631cbcc12b72`  
		Last Modified: Wed, 25 Jun 2025 19:56:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548b03e157af72699a2b0c708ed1848139b85c1e825fae6010a7e9cd0d0b0d3e`  
		Last Modified: Wed, 25 Jun 2025 19:56:31 GMT  
		Size: 20.2 KB (20196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92305aed9fff99346e89b6cf9fb2eaefa429b2ec81bb58c12b79849b4a9989b`  
		Last Modified: Wed, 25 Jun 2025 19:56:31 GMT  
		Size: 20.2 KB (20198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a7cf9e6b5448ec863f17e45bf2ab742be5d945ae30c786b7de74ca808a8f71`  
		Last Modified: Wed, 25 Jun 2025 20:10:58 GMT  
		Size: 33.9 MB (33928384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63563c93a923ed80bd6b380af75f2ad24254318f99d83551aab9afc78c45061`  
		Last Modified: Wed, 25 Jun 2025 20:10:54 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15765c5a420d374fc2e72f09a0a12409a4ad40d80008610f3ce39afedb6d4908`  
		Last Modified: Wed, 25 Jun 2025 20:10:53 GMT  
		Size: 976.4 KB (976409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a8b56b850bb7745e4ac1e7d9d7b555a4ffb8a7136db40f4677a061fcd93b52`  
		Last Modified: Wed, 25 Jun 2025 20:10:54 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11b5224eed86e09a9babac5ce2629840558d33b49b557799960fcf8a006579`  
		Last Modified: Wed, 25 Jun 2025 20:10:53 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:94af336ce22af4eab86934565e7d69d4fe53b980452ef6c2a37a35b374ec5c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199c3fcde247ca2fc04a79f5715a960e5ae8d5afdd370140f57daec9c3ef9b57`

```dockerfile
```

-	Layers:
	-	`sha256:7da5a02414a2954d26ef2325b624809ec6e2893129e4989a9c4d0aa51fe70368`  
		Last Modified: Wed, 25 Jun 2025 22:13:55 GMT  
		Size: 2.2 MB (2175332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:326a2e9e63c141f7dbb07cef94a5ebac2a8d3d4a3cbdd8ea862e75a787912db5`  
		Last Modified: Wed, 25 Jun 2025 22:13:56 GMT  
		Size: 31.6 KB (31643 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:5b79366f9fea074ba4ce661f96610412bb4f75357f091a8863db413eefea2335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74493968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c781c10b413b1953359586d2bbbbe9ea341900d7b2f674bd660dd1031dac251e`
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
RUN docker-php-ext-enable opcache # buildkit
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
	-	`sha256:e5156ab784127c5f20a3284bc78069476b0aec6fca9f1c760d1c0247d2729bf6`  
		Last Modified: Wed, 25 Jun 2025 19:11:46 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6fa42566fcd2f22f0fcb32f9d67be668fadec8dd660d6a59b78743cd2ffbb6`  
		Last Modified: Wed, 25 Jun 2025 19:11:46 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de5862e7e3209a4e6957f47484a85d22d2255e5a5d9b310782bb869fde48ebb`  
		Last Modified: Wed, 25 Jun 2025 19:11:46 GMT  
		Size: 20.0 KB (19992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58e506f673b16ab88134cd2c5799d341eb8e80f988eaed90d920c8e5fd0d701`  
		Last Modified: Wed, 25 Jun 2025 22:15:48 GMT  
		Size: 33.8 MB (33806973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead742195c902065c11752dc6a49d4018c8f25d6464715ab3a176cc65a7b744a`  
		Last Modified: Wed, 25 Jun 2025 22:15:45 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9477cf874532ef3f5377bd7205691a71e01080634b1cf14b165170bbd1debea8`  
		Last Modified: Wed, 25 Jun 2025 20:29:48 GMT  
		Size: 976.8 KB (976759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb15dc78f78d103edcc744c17908609b087a11d0c10548c3f9d791e07ccbca86`  
		Last Modified: Wed, 25 Jun 2025 20:29:47 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d12990d178f3a231689fc65d83f3a7e6a5a2d5eeb8e550e2e668204d5a119c0`  
		Last Modified: Wed, 25 Jun 2025 20:29:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:ec518a5748eb2dc5933b0dde7481955ce9fb44e50e427d39c4f7f2fd0e223e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e33e8e42211269a1e7002b30bea2db3df2082599ce945fb70f1aab1e2f547c`

```dockerfile
```

-	Layers:
	-	`sha256:9098b095d955b2b93f011994099e2f4c22d7b4c69862671929f221150f306076`  
		Last Modified: Wed, 25 Jun 2025 22:13:59 GMT  
		Size: 31.5 KB (31529 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:2bea14b1ce1a271a51ed81bce609701e4941c5e3a55cf789e8813b7605439ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71256030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3d089bfd3bf093d120b5a1661cf8cbfe8774d6e9bf71781f4107c574ec6382`
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
RUN docker-php-ext-enable opcache # buildkit
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
	-	`sha256:caed5fe54fa7698269b0f03745abd3cd03f19be46b6f1f2f34a42189ba12cc78`  
		Last Modified: Wed, 25 Jun 2025 21:54:39 GMT  
		Size: 967.1 KB (967105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f844f6375c378fd706b758befbbf7c50bc4d4f744ee5a4984ca8e31cc047f38b`  
		Last Modified: Wed, 25 Jun 2025 21:54:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75584bd4284df726812248128cb33c077619a446823e08b0125857ca222d2ef`  
		Last Modified: Wed, 25 Jun 2025 21:54:38 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:861353095f105f474f9ade6ab8b05e8466f2a4fd17407b8ce652011908ae81ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57a28954b91d4dcc240f98405c7ff853aba05fc7e3fbe41471e2b338ba6d26f`

```dockerfile
```

-	Layers:
	-	`sha256:08c8592c2e4cb1f04ca0fe7b5af8af4496044af7688342fd58958cc15c5ab89e`  
		Last Modified: Wed, 25 Jun 2025 22:14:03 GMT  
		Size: 2.2 MB (2175656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55dfb5aaafc7d7ed52869be8a006678633e0c88f558698d196d5f17a00f665d4`  
		Last Modified: Wed, 25 Jun 2025 22:14:04 GMT  
		Size: 31.7 KB (31745 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:d2dadc0c40a3554177b591599fb4d6a672330089c735772da89e0220add47f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d43140056d0abec9110d9e36cc98a921b48be8aac07425b3be37eced18794a`
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
RUN docker-php-ext-enable opcache # buildkit
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
	-	`sha256:7ddf66bb9ba56337081b692d4129b361f983e7f9abd1d5e349d28c1c7eade483`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 976.0 KB (976041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b24a8ffa2909a504d9bbfc6df46cc2b56d610d921e33e9974ffc838c62bdd1d`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821b9dea24a435946ecb336cb8278f7297bed4a94795980b99f141347beab268`  
		Last Modified: Thu, 26 Jun 2025 00:28:57 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:df1144ec9680bd760c06c95a7bfff7150690d287e025712cc341c4a5ffe356df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640d11c5a6cebe938b2fd6fab0e883dbce3befa0419a62d2c446198798adf567`

```dockerfile
```

-	Layers:
	-	`sha256:a7b2a0fdfcdccff2b7138ac64502f1f2fb239077a7b59fa7e206bf3e6f124b5c`  
		Last Modified: Thu, 26 Jun 2025 01:13:48 GMT  
		Size: 2.2 MB (2175484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b5ec1ac58d000c75aaad3474d0386b5646668bc3b2685875bd6ce02e925b2b`  
		Last Modified: Thu, 26 Jun 2025 01:13:49 GMT  
		Size: 31.8 KB (31777 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:78960e29b736861203a84f160cccd2dd60ddee1c6cd45d2be5ad27cceeca33a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77748956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684c43fcd75aad95bc5d33c7a3a89f84f9a0e67015351041daed92159438bcc9`
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
RUN docker-php-ext-enable opcache # buildkit
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
	-	`sha256:5ec6ae0f7bd176cd3b23016bb9ee9698507770d28b379f7c3617105788ea8f03`  
		Last Modified: Wed, 25 Jun 2025 19:56:36 GMT  
		Size: 3.5 MB (3527778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf97b1f594033871ab5310105351a00295f6cda0b3b6b64aa7c2530a313ff2f`  
		Last Modified: Wed, 25 Jun 2025 19:56:36 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b4d8bd5000c186b6ddd44f889cc89c9a18ef0e760f4f1b64c37f0d26f95b7f`  
		Last Modified: Wed, 25 Jun 2025 19:17:11 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d744be0c5e8ab473a7ebb7399f80c4408081f06ac83bbe63399fe642c76b21c`  
		Last Modified: Wed, 25 Jun 2025 19:56:37 GMT  
		Size: 13.6 MB (13640494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c9cda8eae5dc08edb62412373f47a15a23be2a2ac313fcde2dd09cfa5a8593`  
		Last Modified: Wed, 25 Jun 2025 19:56:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58194bae6a351287765b02dbcf39ac93de32f73428d63fbc828966a473110735`  
		Last Modified: Wed, 25 Jun 2025 19:56:37 GMT  
		Size: 21.5 MB (21492986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60af96b687f55ce57ae78a8b6decc9aa61b3297f7f0cba4b1a3d94ce45651da9`  
		Last Modified: Wed, 25 Jun 2025 19:56:36 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d24f730e53b3974d094b1bd52b11a0bba281ada5aa6d9b8986ed3d828a592d7`  
		Last Modified: Wed, 25 Jun 2025 19:56:35 GMT  
		Size: 20.2 KB (20189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7f027fc3e2e72fee646df51013f516e6e507dc4e1c3d297ecd04ec8c3d388d`  
		Last Modified: Wed, 25 Jun 2025 19:56:36 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc54df4bcd00e24abd583de43895fbcc07359e249d90a01428a2c5209c3e6f46`  
		Last Modified: Wed, 25 Jun 2025 20:10:53 GMT  
		Size: 34.4 MB (34436734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d9fd01be8a88738d613f3c4000d35b04fce008b1595c21d6c5f7969b581cf3`  
		Last Modified: Wed, 25 Jun 2025 20:10:50 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07eba6c5bb10ada1627f7ba0940107cc88a656575b579a242d2f246a096069a`  
		Last Modified: Wed, 25 Jun 2025 20:10:50 GMT  
		Size: 989.7 KB (989706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffe1eb38e373b55d656275d0f3e1678132c144c5a04273b3f3f9d7b35323025`  
		Last Modified: Wed, 25 Jun 2025 20:10:49 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e211faf6df17d99795a0c47dc68cc7160a26e2e87e2198bbc595e713f842c707`  
		Last Modified: Wed, 25 Jun 2025 20:06:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:764583661b7771d0f5078618672e31e376f2a59cbc88d60b01685abfbdfa2029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a68667dfe0f4c02db393bdb2a063ac4e1defa937a1584db1fa053bab6c1189`

```dockerfile
```

-	Layers:
	-	`sha256:881710b819be86c228feae3c38d94ca8c63ec58f98784f8b0933acb4d56be810`  
		Last Modified: Wed, 25 Jun 2025 22:14:12 GMT  
		Size: 2.2 MB (2175115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1acba33a5e4d89d96dbeb16846651aff9e75e612d1887f20e97aaa19199f6171`  
		Last Modified: Wed, 25 Jun 2025 22:14:13 GMT  
		Size: 31.6 KB (31607 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:526701ba154a0dc5230c8e3b994399ad6cec9003c6a414cc7132bb886f7f5ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79170970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67202a98d340d31e679a27e2684b5bdf3e8bc60745e1d6a64b2e9ef7f06735f`
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
RUN docker-php-ext-enable opcache # buildkit
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
	-	`sha256:1c39f7c5ea781072fb0cebd7228fe3f2bbe1c4616947233ee6be68bacb61fac2`  
		Last Modified: Wed, 25 Jun 2025 22:27:03 GMT  
		Size: 983.0 KB (983046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1791264097295f7d8aab2de52d023c2df3467d9bd93ce2e011e138589cff48`  
		Last Modified: Wed, 25 Jun 2025 22:27:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9888d550f8f9162b8b3c4d6bda88bff46c02584b70edad8262e3a00bbd9df32e`  
		Last Modified: Wed, 25 Jun 2025 22:27:03 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:5b61079a0f29a0a5b0cb9d712fae1e4a2e023a237a47c1a618d5ee8d540feb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa10d7efa1d91615cb8bf4f3837842ee44eae45bc5458617827051d08a2b5efe`

```dockerfile
```

-	Layers:
	-	`sha256:93755768d3e855aafdf9ca81fe69c156d7f2f949dc7849208a3d27216f35c195`  
		Last Modified: Thu, 26 Jun 2025 01:13:56 GMT  
		Size: 2.2 MB (2173895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:917e2ecd9a78302f3990a6866537cfe3eba8a771c6d96c55d91eee7e96b32f4a`  
		Last Modified: Thu, 26 Jun 2025 01:13:56 GMT  
		Size: 31.7 KB (31691 bytes)  
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
