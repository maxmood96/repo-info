## `composer:latest`

```console
$ docker pull composer@sha256:7384cf9fa70b710af02c9f40bec6e44472e07138efa5ab3428a058087c0d2724
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
$ docker pull composer@sha256:1d10c863bacef5b481ac5aa68bc3b2cd0fc23b1613512c01184b5cde3f5e4ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75874566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55376f2df6ea2b8e950cae4eecf6f0bbfab0f17496757e3bd8331ac67300d3e2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 23 Oct 2025 18:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Oct 2025 18:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_VERSION=8.4.14
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Oct 2025 18:46:40 GMT
CMD ["php" "-a"]
# Thu, 13 Nov 2025 19:11:59 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 13 Nov 2025 19:11:59 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 13 Nov 2025 19:12:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 13 Nov 2025 19:12:16 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 13 Nov 2025 19:12:16 GMT
ENV COMPOSER_VERSION=2.9.1
# Thu, 13 Nov 2025 19:12:16 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 13 Nov 2025 19:12:16 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:12:16 GMT
WORKDIR /app
# Thu, 13 Nov 2025 19:12:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:16 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1329c5084d624e0d041d09a190180a44c4d82bf87d29e37124d02a5a4e0e5809`  
		Last Modified: Fri, 24 Oct 2025 19:26:16 GMT  
		Size: 3.5 MB (3463762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc671ef6f9c8e605c15a2d5b9c5be998079cc5cb98e73b58591ca25b97d06def`  
		Last Modified: Fri, 24 Oct 2025 19:26:16 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f413b510cd4a8a8656c38f987bbade3f59c7bba10d1ef2fe4a7afdecf50f70c3`  
		Last Modified: Fri, 24 Oct 2025 19:26:16 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5a2611d454825d1788a2b6b2ad376f47fe60d51390ede78cf08cfbd90122e5`  
		Last Modified: Fri, 24 Oct 2025 19:26:17 GMT  
		Size: 13.7 MB (13665838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad217014f3d0bb47bf766b15315a769b1fd80034bcc74e903a36e5c3a155b48c`  
		Last Modified: Fri, 24 Oct 2025 19:26:16 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800a2b6306a04e9d843a5fc18f1a71fa23b74b09cb7480943467be42458dcfd4`  
		Last Modified: Fri, 24 Oct 2025 19:26:18 GMT  
		Size: 20.0 MB (19955567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb47194af07c23ba476c82020f5c6462ec00ed66bd357a5c32d2cbb7da720585`  
		Last Modified: Fri, 24 Oct 2025 19:26:16 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb8c0d2cc28beed1de437b76f9be01318026f15cc601009f46c36954cdd96e0`  
		Last Modified: Fri, 24 Oct 2025 19:26:16 GMT  
		Size: 20.1 KB (20073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed107248614865eca656b1bffadfb13a230adca7df1bcde3220f3bd98d898f3`  
		Last Modified: Fri, 24 Oct 2025 19:26:16 GMT  
		Size: 20.1 KB (20071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec086752a383156d9d7c3b73cdbfd2c265622533f7a065779a0c1b2a67f566c1`  
		Last Modified: Thu, 13 Nov 2025 19:12:36 GMT  
		Size: 33.9 MB (33947143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96092ce88fc879a36de30d2548132a1e2894d429207af04c20e10bb1bcd37d6`  
		Last Modified: Thu, 13 Nov 2025 19:12:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb53fb453233b4ac6dfe1144b551f3b73e8682eb724054769c261cd31425f14`  
		Last Modified: Thu, 13 Nov 2025 19:12:33 GMT  
		Size: 994.8 KB (994803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3169feeb0b83df0cdc831932a43aab6366ab7e8ee68bc5eef5c61230a4e98899`  
		Last Modified: Thu, 13 Nov 2025 19:12:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d6574a238dffef1b4d319792a07d63333ec68c12656c1ac102548d00328a75`  
		Last Modified: Thu, 13 Nov 2025 19:12:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:a329304f48d6e2dc7d6fe5a58d0d1397521dc1370a14a0847e9d795c95273259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44afe8e46fc3ec952ec9773138ce5c835aba2cfc5fa56fab4f09aee94a81ec6d`

```dockerfile
```

-	Layers:
	-	`sha256:1dffe5de027dfe6c4ec62470c0d365222f59f78e246e04eab93a9144244bed78`  
		Last Modified: Thu, 13 Nov 2025 20:13:50 GMT  
		Size: 2.2 MB (2173411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c2d1febeed191aeb888fdef08be034feba08e57b78ea53abbd713483a9f05e2`  
		Last Modified: Thu, 13 Nov 2025 20:13:51 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:a104469976b610009c2a2512c82e626562f00501e4c35496bff5c54c8d94b2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73515820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0ffa39f0e443f76b505b605ac10cbd4b739f0fb9fa2d51cd31d5bb19b50799`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 23 Oct 2025 18:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Oct 2025 18:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_VERSION=8.4.14
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Oct 2025 18:46:40 GMT
CMD ["php" "-a"]
# Thu, 13 Nov 2025 19:11:04 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 13 Nov 2025 19:11:04 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 13 Nov 2025 19:11:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 13 Nov 2025 19:11:31 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 13 Nov 2025 19:11:31 GMT
ENV COMPOSER_VERSION=2.9.1
# Thu, 13 Nov 2025 19:11:31 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 13 Nov 2025 19:11:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:11:31 GMT
WORKDIR /app
# Thu, 13 Nov 2025 19:11:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 19:11:31 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa92403a7591eac3005b3589514439adb33ddfd0cdf573f41acb7b2f59795ad7`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 3.4 MB (3428323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2061b8000d4d8033b2b8390df19f894b799a70f19e1b18ad00ff070e834c448`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3886f04bed6533c2ca443852c6834c95a2bf593fa2353717502597cdc730e4`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e31262a68741790bc75b7d52bb0dfcf6466cd97c612c50f09ded3fe6418555`  
		Last Modified: Fri, 24 Oct 2025 19:26:52 GMT  
		Size: 13.7 MB (13665835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4a424954978a6cd3cba5774af71e47d6c97e6728c83e3899b1fcd10ba52333`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55585e557ba0bf347b587dbe97b2b0091e13e5412706d0085b7d73006580e619`  
		Last Modified: Fri, 24 Oct 2025 19:26:54 GMT  
		Size: 18.1 MB (18060211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976680173b043a978a102e54fc552619ac2d4451a582fedd2b5b10edf3c81e92`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b3d35e48b94e248c82ef2b7b0963b920bc8ed6f3d8fc072513aac877448996`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 19.9 KB (19861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aeeb1aabb5cdf8cb6f2f2083e84f2f065745a4b811b3e696b40c081e79549c9`  
		Last Modified: Fri, 24 Oct 2025 19:26:51 GMT  
		Size: 19.9 KB (19862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74e4942491530ede4ea5c27655f615c183a929e49ccd107fb3cec80a46e92d4`  
		Last Modified: Thu, 13 Nov 2025 19:11:47 GMT  
		Size: 33.8 MB (33817994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9c1997d09eabeea32f8c6839b25ddf8c9801d5404d0b3d8fb8b6aea2061d44`  
		Last Modified: Thu, 13 Nov 2025 19:11:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f44e3170ed25adfd3afd27b617c0d2abf655185c2a87719da3e90f1b8a85e0`  
		Last Modified: Thu, 13 Nov 2025 19:11:44 GMT  
		Size: 994.8 KB (994800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92fb791b9685a4c2a06197cfe9882ef8d452e1188ff3c8e2963a4bce56026dd`  
		Last Modified: Thu, 13 Nov 2025 19:11:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7fc77dd7c50ada9ea21725f9e7bd298a6469540bc522a36a5f490cfd7c4eb9`  
		Last Modified: Thu, 13 Nov 2025 19:11:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:2f28935aa98414fac2f2fb64f5152df64b96dba9ef4b52c729f8ba6ae02f352c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7d25caa7103c2412fd5ed79a1c97bf3e885f421c29562f21f396aaf887ec22`

```dockerfile
```

-	Layers:
	-	`sha256:6da2c527e0d3431e8fe817bfd14b1b5f292752c6f40a7cd81bbbdfc1f54182f7`  
		Last Modified: Thu, 13 Nov 2025 20:13:54 GMT  
		Size: 31.5 KB (31500 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:01aabeb0ddf1d8d06ee60f1b50e525ed854ad96ab423a860ccd57955e5fc1dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70310777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23e547e773473cbcb0d2d08b9739e6ec6973598b5c119efd33adf6c57d925fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 23 Oct 2025 18:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Oct 2025 18:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_VERSION=8.4.14
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Oct 2025 18:46:40 GMT
CMD ["php" "-a"]
# Thu, 13 Nov 2025 19:09:50 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 13 Nov 2025 19:09:50 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 13 Nov 2025 19:10:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 13 Nov 2025 19:10:14 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 13 Nov 2025 19:10:14 GMT
ENV COMPOSER_VERSION=2.9.1
# Thu, 13 Nov 2025 19:10:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 13 Nov 2025 19:10:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:10:15 GMT
WORKDIR /app
# Thu, 13 Nov 2025 19:10:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 19:10:15 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86befc8c1e2c60f4f39c9201e05c6113f90d2c2c1ba583801d2bb7fc0e048407`  
		Last Modified: Fri, 24 Oct 2025 20:00:19 GMT  
		Size: 3.2 MB (3244388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4090b522cebcb13ace81579f703a792840bd3a2a776d263f618377aa5ad7b837`  
		Last Modified: Fri, 24 Oct 2025 20:00:18 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4226203351d20410512f4260b17c28280033e70ab39fe4e8ca8faaedf80956d`  
		Last Modified: Fri, 24 Oct 2025 20:00:18 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29c954d853d3626c66559e0b82b75a2385f86c3cef8edcd79d3ba80879d8c36`  
		Last Modified: Fri, 24 Oct 2025 20:00:20 GMT  
		Size: 13.7 MB (13665830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88085d351af20bdba1e3ea33e4f437fefc126fd7027872482d442dac2321bb1c`  
		Last Modified: Fri, 24 Oct 2025 20:00:18 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4d1708b787357c5fad8011057efbea12d9483c0ebd8f38676c576073384744`  
		Last Modified: Fri, 24 Oct 2025 20:00:21 GMT  
		Size: 17.1 MB (17050299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b7b8bbe9073e735053fec9c6859ffbfa2c2104861c6bac6e158b43f20fafa6`  
		Last Modified: Fri, 24 Oct 2025 20:00:18 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16bc8c74e19be188069c5b2ca0c62e97ac5da7609764aaa91440656abca26f4`  
		Last Modified: Fri, 24 Oct 2025 20:00:18 GMT  
		Size: 19.9 KB (19857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a3e608ee86aa8bcad71953053412b2deb858a9f8563456f0cc30a004e4b5f6`  
		Last Modified: Fri, 24 Oct 2025 20:00:18 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16c4ec3c4990dc4d18f670ec4b6dbc6f8f02b1c2de29934eba02ecdf4c8e390`  
		Last Modified: Thu, 13 Nov 2025 19:10:34 GMT  
		Size: 32.1 MB (32098333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef607bae027adb326352eb5e59e092cff569d062b6655520b868bb2d11f59632`  
		Last Modified: Thu, 13 Nov 2025 19:10:30 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eeee1db4feed33a3818b04e80dbfa3501d86dd33327f4f08ddb9bb0caa19d7e`  
		Last Modified: Thu, 13 Nov 2025 19:10:30 GMT  
		Size: 985.8 KB (985807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7927de17ea1e1bcfe139c2e2b9f243b393cf88b299fc5b9ce9955ec8ba2c4b9d`  
		Last Modified: Thu, 13 Nov 2025 19:10:30 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ec464e7b139b2244d6f4fe18bf79ede3130fd3fc43c93e6c1fc13fa35d6935`  
		Last Modified: Thu, 13 Nov 2025 19:10:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:0f66dbc6c09e36c288ead1e95de438e525e957526674d4688c3a1ca9315ce549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1aa6ebb1624d3da8545c9de4ab0c9c8d2e03aa46974a07a8cac0ee594154c4`

```dockerfile
```

-	Layers:
	-	`sha256:624f12331a1be2bb5b43535ae9719e878641a52f60d2bb0fbbc235eba95be33e`  
		Last Modified: Thu, 13 Nov 2025 20:13:57 GMT  
		Size: 2.2 MB (2173735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56d342426f3e3d3de989f8dc149c40026adae2c4c1054975cf7c505167af80e6`  
		Last Modified: Thu, 13 Nov 2025 20:13:58 GMT  
		Size: 31.7 KB (31715 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:134e4bf00fe31dfdc35b446b4ebffb541e8dbd7f38036747fe9889b345d42e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75851361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6312b9a36c3e54a2cfeeef884178b8359cee57d444b9abd67631a1b4441c29`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 23 Oct 2025 18:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Oct 2025 18:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_VERSION=8.4.14
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Oct 2025 18:46:40 GMT
CMD ["php" "-a"]
# Thu, 13 Nov 2025 19:12:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 13 Nov 2025 19:12:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 13 Nov 2025 19:12:33 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 13 Nov 2025 19:12:33 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 13 Nov 2025 19:12:33 GMT
ENV COMPOSER_VERSION=2.9.1
# Thu, 13 Nov 2025 19:12:33 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 13 Nov 2025 19:12:33 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:12:33 GMT
WORKDIR /app
# Thu, 13 Nov 2025 19:12:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:33 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab8e5431b232ea17dba82b276ef0be159d4f17c1baa4241a844a7b01c3e1637`  
		Last Modified: Fri, 24 Oct 2025 19:09:32 GMT  
		Size: 3.5 MB (3466793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ef2c9705318e0150447a2c017caca15d03aed2a9d50610d8ac241df0800b20`  
		Last Modified: Fri, 24 Oct 2025 19:09:36 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d201919164abf67a0ef48a249f1129ca012b48e7e275a0ecf20a219e75e08f`  
		Last Modified: Fri, 24 Oct 2025 19:09:36 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3617909786220dc66fea0cc929755ca0582234f21f9664e785104fdbf6ad1a87`  
		Last Modified: Fri, 24 Oct 2025 19:09:37 GMT  
		Size: 13.7 MB (13665831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5126b2a8113f85f6bb3cf754a09409f4248aa53b64ecd13d4bc6cb77af320bb`  
		Last Modified: Fri, 24 Oct 2025 19:09:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bf9fd0c2ec689df2d35e738c05244d989cb6dd76d7e069cb46aa982f43b6ee`  
		Last Modified: Fri, 24 Oct 2025 19:09:37 GMT  
		Size: 19.5 MB (19504879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562973c5a4e7b322fc0a740f6e09b7a4f686f5b1e677635e9d5ebaee5d5bb349`  
		Last Modified: Fri, 24 Oct 2025 19:09:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90ec277e222ddd9149e8d97aa83ab3932d772a8b5dbbda2fccf70936b969646`  
		Last Modified: Fri, 24 Oct 2025 19:09:36 GMT  
		Size: 19.9 KB (19860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ede6f49d9776977104724e69dc09f925074d3f13b570cdaef7d98743219309`  
		Last Modified: Fri, 24 Oct 2025 19:09:36 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840a58cf528a833406aed09074d92b65ab47246972e8809af347c287875e473d`  
		Last Modified: Thu, 13 Nov 2025 19:12:55 GMT  
		Size: 34.0 MB (34036504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dcfaa280bac9f70c229a45c784b28dc33e9143b96a7f941df8e148593f26fa`  
		Last Modified: Thu, 13 Nov 2025 19:12:51 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393206ae3cd3c02d8b7bbb3bbb3ed748e99f15a90f976d28b6be9a7fec89eae9`  
		Last Modified: Thu, 13 Nov 2025 19:12:52 GMT  
		Size: 994.7 KB (994709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898e213f6184a6a11f95c875e59e168a7f131756bc3154801571efb5e0afb878`  
		Last Modified: Thu, 13 Nov 2025 19:12:51 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcebd9d1575e3d057c6bf0c8157731a059aa04d82b35d508958c9dc74d3b3b04`  
		Last Modified: Thu, 13 Nov 2025 19:12:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:4a6a5b481d2a1905e772ca101d464c2dcf57d8a43f3f21c5df3ba9f2577a0ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a56677b78e2def3aa59a5a3d1a57ab62f81d185b1ccc2f5bb5d4d1ca56204b`

```dockerfile
```

-	Layers:
	-	`sha256:52ac66585e6deb01c34090b72d36d9ed77b1da6eaa2b02d71861ee1629b32555`  
		Last Modified: Thu, 13 Nov 2025 20:14:02 GMT  
		Size: 2.2 MB (2173563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d49fa4990c708a4fb87960f4a9bcbf40fbe9df79b6f5f48dbfe52bdb42a2d9`  
		Last Modified: Thu, 13 Nov 2025 20:14:03 GMT  
		Size: 31.7 KB (31743 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:eda89374b487e0e320ff1146f89a2eeb4e8eef3ff5bfd194fdf357e08b616b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76816666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc064dfba5e857fbf05fc65648a26839b99fdbe92b2010d66ec2894dde8a8722`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 23 Oct 2025 18:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Oct 2025 18:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_VERSION=8.4.14
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Oct 2025 18:46:40 GMT
CMD ["php" "-a"]
# Thu, 13 Nov 2025 19:11:38 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 13 Nov 2025 19:11:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 13 Nov 2025 19:12:00 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 13 Nov 2025 19:12:00 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 13 Nov 2025 19:12:00 GMT
ENV COMPOSER_VERSION=2.9.1
# Thu, 13 Nov 2025 19:12:00 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 13 Nov 2025 19:12:00 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:12:00 GMT
WORKDIR /app
# Thu, 13 Nov 2025 19:12:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:00 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd1047cb7f567073e37680da0f0c36a8876c5b443c64da4595cdec94c95024d`  
		Last Modified: Fri, 24 Oct 2025 18:41:55 GMT  
		Size: 3.5 MB (3522934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5432291532ac93ec85b0f03092c7de1698ed58f22f782a88d04612ec689a74`  
		Last Modified: Fri, 24 Oct 2025 18:41:55 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf46d8c3be72e693a97a1954ee7b7b2eb20280f895d12d327877769ad0e67ff`  
		Last Modified: Fri, 24 Oct 2025 18:41:55 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b239e840753cbefa4bb180374d7c4de7017b502a460c7c620aa2de485dea4a`  
		Last Modified: Fri, 24 Oct 2025 18:41:57 GMT  
		Size: 13.7 MB (13665807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ab54154fb78163d7eead7c5a48c6368ac258df68dbd81a9180669ba7b65578`  
		Last Modified: Fri, 24 Oct 2025 18:41:55 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2180045f81b8fe7a4380661a927a38a4193ab8d6c9b475c85cc78fb37e4c37`  
		Last Modified: Fri, 24 Oct 2025 18:41:57 GMT  
		Size: 20.5 MB (20487530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e06449af4deae637dc8823eb2707a0a77708c33956bad55ca2ef902a5079f9`  
		Last Modified: Fri, 24 Oct 2025 18:41:55 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b91cf49295a1961490a462be09ea0d948cec5dffe19693d07fd6482738d2`  
		Last Modified: Fri, 24 Oct 2025 18:41:55 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8433c5c2f5580dd81b3dcce9aa438908101b76876633367f4c63eecbc4f218`  
		Last Modified: Fri, 24 Oct 2025 18:41:55 GMT  
		Size: 20.0 KB (20041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39440a64391aeeb1a0640638ed52e18a3554591f523b0323cdf44480d0c4ea7f`  
		Last Modified: Thu, 13 Nov 2025 19:12:41 GMT  
		Size: 34.5 MB (34468482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cab0f25666f66332fe16ab18f60fed4bbcaca00d837235bea7b745914e03d7`  
		Last Modified: Thu, 13 Nov 2025 19:12:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b0a909fc7fba7fac1acbc1318f0a9266bd8f42b7d88f9d7245e3da1a99456f`  
		Last Modified: Thu, 13 Nov 2025 19:12:36 GMT  
		Size: 1.0 MB (1008031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5249517ced92865896a630084bc8fb5d918bb349cc935135a15ef615098e951d`  
		Last Modified: Thu, 13 Nov 2025 19:12:36 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d12178315f24c8f70620584876be4c5a38b2d42e11008184319800fd19eb09`  
		Last Modified: Thu, 13 Nov 2025 19:12:36 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:949261b8710bdaeeeb5ade85013b471a6729639b2d1aa7d16f371a18a9d920f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698359113fbb282dd1bc3c262646ba89eb272f79c1645ccbe8c72a6f56b1a829`

```dockerfile
```

-	Layers:
	-	`sha256:b3459d00874dbdd042b33562a3ab20e52dae27ac39922d46503f9c4b08ee5239`  
		Last Modified: Thu, 13 Nov 2025 20:14:07 GMT  
		Size: 2.2 MB (2173194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91cad099c05ce9ab64b41ddfa43c3ddd980112f36f209f613edf7b89e9282eeb`  
		Last Modified: Thu, 13 Nov 2025 20:14:08 GMT  
		Size: 31.6 KB (31576 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:5c5cb8f15e132242afdfc9accf6c6818d54ff0a3ad45fe6e0a7bec23ff04ecb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78190140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4776f16a276149cd28a08b558c418ba60c95521b234edea3ca5d29c7f701228`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 23 Oct 2025 18:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Oct 2025 18:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_VERSION=8.4.14
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Oct 2025 18:46:40 GMT
CMD ["php" "-a"]
# Thu, 13 Nov 2025 19:10:47 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 13 Nov 2025 19:10:47 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 13 Nov 2025 19:11:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 13 Nov 2025 19:11:29 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 13 Nov 2025 19:11:29 GMT
ENV COMPOSER_VERSION=2.9.1
# Thu, 13 Nov 2025 19:11:29 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 13 Nov 2025 19:11:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:11:30 GMT
WORKDIR /app
# Thu, 13 Nov 2025 19:11:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 19:11:30 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a0b03903475651b081c7c705a4ab0f68ab5f5bba328735e8dae6e168526c7`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 3.6 MB (3614664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436cae3ea479232d2bcf67ca55e6705ab3775fa412e53331855937a2a7340b65`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1164e359044b0e56f99538c30031735fcef9128820673f06e10663118d04d0e3`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef38c73f3ff68aca00580e73801a535a988fbae408500c93468879ece8ebc678`  
		Last Modified: Fri, 24 Oct 2025 21:07:27 GMT  
		Size: 13.7 MB (13665827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a00a631bb9c16ed735305bb12fd93d2488d0741a8597255ed7563e7d728ff6`  
		Last Modified: Fri, 24 Oct 2025 21:07:27 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ffa15173dd2c88e976a8bc9c8ea99dcc18e321d4772cd35742bbb8e2409539`  
		Last Modified: Fri, 24 Oct 2025 21:07:29 GMT  
		Size: 20.9 MB (20860688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c862d1dbc8c14714255edd6179331935441f0960bd0c4573e31796e9a82fceb1`  
		Last Modified: Fri, 24 Oct 2025 21:07:26 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f45502a2020d8d22fa7393e6cad99679762ffdee488a16af1535a5565cbaef`  
		Last Modified: Fri, 24 Oct 2025 21:07:26 GMT  
		Size: 19.9 KB (19878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2735766e59ead016c2e345f85fba01ed5c0352fbecf5e3007fb3749c5eb511`  
		Last Modified: Fri, 24 Oct 2025 21:07:26 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780a13464d3837c1d0fde41aec0dd3a8de71a1b38ac8bd508d1224a112d44e2f`  
		Last Modified: Thu, 13 Nov 2025 19:12:03 GMT  
		Size: 35.3 MB (35270852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af44601c5f663d8338ba489d7e8757a000e92bf25aeec9a1d4eb10af0bc347e`  
		Last Modified: Thu, 13 Nov 2025 19:11:57 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d3b2444db9d18979d080edc1c43a0645bd069321f12b55368f2362abae13a1`  
		Last Modified: Thu, 13 Nov 2025 19:11:57 GMT  
		Size: 1.0 MB (1001246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815c1059426c6bb6c7a29c298b72188e7e45b007aad30b61cfe2b69032e65d6d`  
		Last Modified: Thu, 13 Nov 2025 19:11:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0f0c6e05c8b34d8bfd5eba7faa9715aa55b81f3f9f41b2380b3522ee972151`  
		Last Modified: Thu, 13 Nov 2025 19:11:57 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:b4af68746f8732b9f64c7b1fad87035c7a3cabb32ff123592e07152e335d19bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc347e7120647e12d77fb07e1953b754552a8d8380ae8c4e66aa429a375d319e`

```dockerfile
```

-	Layers:
	-	`sha256:44191761b3b456ef62762d8bd3b347f324615fe7f797b36f637d0dc4107ced7f`  
		Last Modified: Thu, 13 Nov 2025 20:14:12 GMT  
		Size: 2.2 MB (2171974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc7abbfe00ca42a0c001b548918c60585fd942d10e79decf922f579778ef3a2`  
		Last Modified: Thu, 13 Nov 2025 20:14:12 GMT  
		Size: 31.7 KB (31660 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:9627101f9c1855ce716f2451788bc05d8bb772c7db99cad3c48bdcc76beeb861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72327824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0859c57e0af811a19cc5ba95023c8cfd29a17111b373089ef018626f6113f41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 23 Oct 2025 18:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Oct 2025 18:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_VERSION=8.4.14
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Oct 2025 18:46:40 GMT
CMD ["php" "-a"]
# Mon, 27 Oct 2025 05:32:56 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 27 Oct 2025 05:32:56 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 13 Nov 2025 19:15:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 13 Nov 2025 19:15:18 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 13 Nov 2025 19:15:18 GMT
ENV COMPOSER_VERSION=2.9.1
# Thu, 13 Nov 2025 19:15:18 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 13 Nov 2025 19:15:19 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:15:19 GMT
WORKDIR /app
# Thu, 13 Nov 2025 19:15:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 19:15:19 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e9f10e445dbf7ba866462dd44d0f912a09342dc97a4685769a2d057bcc7a9`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 3.6 MB (3600269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579c35b4a5055268b9ccb82f8c3307c0a781af77168952679399ed4bde3b60a`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b6a920874b5f6759a41702af348a1eefb32a0674eeae4cd9d750418594caed`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b115bacca67276dbf1b2b88c75a1d93a783abab20ad055d2f456784c91848a14`  
		Last Modified: Sat, 25 Oct 2025 20:07:26 GMT  
		Size: 13.7 MB (13665823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa643ca26895c691b4910d72fd561ed485d1c71232f505a04f7dcb490535d6a`  
		Last Modified: Sat, 25 Oct 2025 20:07:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44636f1994b8c2c675720920a0bb9789fc6eb6430fb3a1c1974a2f23fc45ca6`  
		Last Modified: Sat, 25 Oct 2025 20:07:26 GMT  
		Size: 19.4 MB (19378197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0854e2c2237480c7d7f110ec7531105a011961145c5893d54f299a3df5088a2`  
		Last Modified: Sat, 25 Oct 2025 20:07:25 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22295fbf4555881f21a134879c902bd8d957ab88ae584338de3d78f06ada96e`  
		Last Modified: Sat, 25 Oct 2025 20:07:26 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636c9b936e891b05b8c2e03882ad5bb801f88243f72d98c408a0c8215b115e5a`  
		Last Modified: Sat, 25 Oct 2025 20:07:26 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97265ab6c7c326358cedb79d9ac403cf23c21c7ded2d00a8b85ad62cc6eca37`  
		Last Modified: Mon, 27 Oct 2025 05:38:25 GMT  
		Size: 31.1 MB (31131201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89604a377b9c68f35a228966a3bd72ac71d70fd8a335963f9cfe406f225e15c4`  
		Last Modified: Mon, 27 Oct 2025 05:38:23 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbf7d2f478cf348fbf5d05d7a9fc1286ffa9b6d2836441e2171ede045da6ea7`  
		Last Modified: Thu, 13 Nov 2025 20:11:17 GMT  
		Size: 992.5 KB (992507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11034490fac08f319be7a783e4334efe6ce8405840dd73dbcc0080d5914c422`  
		Last Modified: Thu, 13 Nov 2025 20:11:16 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3800544173f19da72a93a0645ce815902643783480b382a6dd9f16298fddd37c`  
		Last Modified: Thu, 13 Nov 2025 20:11:16 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:c0b4646039ac61e0c05ac8626fa5dd947a19e654b8309c68bca444aba38fe1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3bc82ed09a813e31ec95bb71347c0acadcdfa97bb56cc020e96107c2e4444d6`

```dockerfile
```

-	Layers:
	-	`sha256:236ec251d600d5e430f0769070e81c04244d2dd22ee64597fef0a21d470d9832`  
		Last Modified: Thu, 13 Nov 2025 20:14:16 GMT  
		Size: 2.2 MB (2170241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0009d434c3719dba04f801b278c51b18df7911f7058d37607c8165db9025e72`  
		Last Modified: Thu, 13 Nov 2025 20:14:17 GMT  
		Size: 31.7 KB (31657 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:81f53863133291d21620ce1af0e7ce1aa3023258f75e48a7ab9ed3582961953b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73900363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ef55e1bf51d6a4ac4332bfc6bc051cac637627d0deb6a2080068ef1997534f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 23 Oct 2025 18:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Oct 2025 18:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_VERSION=8.4.14
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Thu, 23 Oct 2025 18:46:40 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 23 Oct 2025 18:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Oct 2025 18:46:40 GMT
CMD ["php" "-a"]
# Thu, 13 Nov 2025 19:11:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 13 Nov 2025 19:11:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 13 Nov 2025 19:12:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 13 Nov 2025 19:12:22 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 13 Nov 2025 19:12:22 GMT
ENV COMPOSER_VERSION=2.9.1
# Thu, 13 Nov 2025 19:12:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 13 Nov 2025 19:12:23 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:12:23 GMT
WORKDIR /app
# Thu, 13 Nov 2025 19:12:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 19:12:23 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d2dd4bd3263db65246a0eede02512575e505bf72959ea5d8d1c7f5b3dea5e`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 3.7 MB (3692716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e39eb5e282665e4bd0e90c53a85f696e72ef63e8ef403c40cc9e67742ffe824`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0608d8b4902677a8ba1ccd4d718738714fa13e782091c89842c948b06a52f8`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdea27060aabd36ff31ca9055725e9085bf08b94fc0d4b40028e0d7c21102f40`  
		Last Modified: Fri, 24 Oct 2025 20:03:31 GMT  
		Size: 13.7 MB (13665851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70515c51ba3110abd59c349a4cca83963c57d9e8eea1f5a9531ee7dafa31ec26`  
		Last Modified: Fri, 24 Oct 2025 20:03:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66a11b7c047c1150c15ec0166e1c3737640f6f9ed49c8b67614c8e0e4672cac`  
		Last Modified: Fri, 24 Oct 2025 20:03:32 GMT  
		Size: 20.0 MB (19973403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695d42787f851983f0874071c409307ecdef1c5f9c0f9e6ad3a2f2ce05caf777`  
		Last Modified: Fri, 24 Oct 2025 20:03:30 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2093cfdb1b47e177d32873991ccf3e5cd21236d50791db5baa480c7dd48de0`  
		Last Modified: Fri, 24 Oct 2025 20:03:30 GMT  
		Size: 19.9 KB (19877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d5e698d2cc5b0e0597cf3c7da7ac79ed39aa63a8b61eebb22ad2e642482d87`  
		Last Modified: Fri, 24 Oct 2025 20:03:30 GMT  
		Size: 19.9 KB (19877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98735552ef47cfc8d2d2eb21137a8307ddfb01bfce246ed6254ed8eb39d9d4a`  
		Last Modified: Thu, 13 Nov 2025 19:12:58 GMT  
		Size: 31.9 MB (31876707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f198418e74a5fcdfd46230acd35410cf85c751b63c0c36ed134db7b7caa68652`  
		Last Modified: Thu, 13 Nov 2025 19:12:55 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094f40183c919d5df22c82640e10754dd63992f0de0b9f4f1b2c7564acb7d9bc`  
		Last Modified: Thu, 13 Nov 2025 19:12:55 GMT  
		Size: 997.8 KB (997828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c637f59ebda26564ed07fdf71448207496f87c8a75a4750782574923419a3324`  
		Last Modified: Thu, 13 Nov 2025 19:12:55 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4dec7a9c1ce56eb469a2050deb1ee3aa77abfad874b4cca3b631495fb28fee`  
		Last Modified: Thu, 13 Nov 2025 19:12:55 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:65c1dab17c4ece0dbf77cc67f599c2d7c9f1ce082c433526dd8fa09efea8e438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddc206da18a3f6c7ef5855ece3dca35e678b872e41e30f32f0fcece1980e703`

```dockerfile
```

-	Layers:
	-	`sha256:e6f0664e93bb71db7e972b41a383a4c06f9155a5ed86948087bffc3c4efca0b1`  
		Last Modified: Thu, 13 Nov 2025 20:14:20 GMT  
		Size: 2.2 MB (2170023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2335f9b367e29ed880633b59e62731afbf6b18cc8b41f1655a2974a98b618451`  
		Last Modified: Thu, 13 Nov 2025 20:14:21 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json
