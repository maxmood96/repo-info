<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.28`](#composer11028)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.28`](#composer2228)
-	[`composer:2.9`](#composer29)
-	[`composer:2.9.8`](#composer298)
-	[`composer:latest`](#composerlatest)

## `composer:1`

```console
$ docker pull composer@sha256:dbc308a7af43fd5b1084ced476e67df2a34e04371100fae720f4893321f23c6d
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
$ docker pull composer@sha256:24fceab78a0b2bccf763b67cb68a85bb69c8e316e5de31bf994fd071f6cf6337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75615868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bd535adaec9b3ebdfa7b381f96653138f8cab9236249566b8c4f619ff344bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1329c5084d624e0d041d09a190180a44c4d82bf87d29e37124d02a5a4e0e5809`  
		Last Modified: Fri, 24 Oct 2025 19:26:00 GMT  
		Size: 3.5 MB (3463762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc671ef6f9c8e605c15a2d5b9c5be998079cc5cb98e73b58591ca25b97d06def`  
		Last Modified: Fri, 24 Oct 2025 19:26:00 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f413b510cd4a8a8656c38f987bbade3f59c7bba10d1ef2fe4a7afdecf50f70c3`  
		Last Modified: Fri, 24 Oct 2025 19:26:00 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5a2611d454825d1788a2b6b2ad376f47fe60d51390ede78cf08cfbd90122e5`  
		Last Modified: Fri, 24 Oct 2025 19:26:00 GMT  
		Size: 13.7 MB (13665838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad217014f3d0bb47bf766b15315a769b1fd80034bcc74e903a36e5c3a155b48c`  
		Last Modified: Fri, 24 Oct 2025 19:26:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800a2b6306a04e9d843a5fc18f1a71fa23b74b09cb7480943467be42458dcfd4`  
		Last Modified: Fri, 24 Oct 2025 19:26:02 GMT  
		Size: 20.0 MB (19955567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb47194af07c23ba476c82020f5c6462ec00ed66bd357a5c32d2cbb7da720585`  
		Last Modified: Fri, 24 Oct 2025 19:26:01 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb8c0d2cc28beed1de437b76f9be01318026f15cc601009f46c36954cdd96e0`  
		Last Modified: Fri, 24 Oct 2025 19:26:02 GMT  
		Size: 20.1 KB (20073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed107248614865eca656b1bffadfb13a230adca7df1bcde3220f3bd98d898f3`  
		Last Modified: Fri, 24 Oct 2025 19:26:02 GMT  
		Size: 20.1 KB (20071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a77d225a4093408ffc09f88e84ceecb9a9237fce71c0c2e253da24dba08370e`  
		Last Modified: Fri, 24 Oct 2025 20:15:33 GMT  
		Size: 33.9 MB (33947738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58861f8d0fbf31403e66960ced7a82c738d6ab53693214ff5f3fc15eaf3d6ae0`  
		Last Modified: Fri, 24 Oct 2025 20:15:32 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428d0474586e75f564c8fb583700920feb4e9cff72c624ba23af2eb21e00953f`  
		Last Modified: Fri, 24 Oct 2025 20:15:32 GMT  
		Size: 735.5 KB (735524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2b7ddc51d0e4faafc87372c0be76bf07826c6b188c8a6abdce072c69fe4c`  
		Last Modified: Fri, 24 Oct 2025 20:15:32 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e28c9c8dfe1ad11e48c41658e1e3aa78ead447e93a75f771f2b08463a1b21af`  
		Last Modified: Fri, 24 Oct 2025 20:15:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:b3a3a57911d32bffebd31262aaec3838ebb3cde1f662d49e437a9e5130905838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3acd5795d652baf2e335ac4b4b155986ae965e54b50d15835834d518d482a08`

```dockerfile
```

-	Layers:
	-	`sha256:a734a51ed57dcddb9fde01424686ee059ec94007b5fd6e1fb7e453143d190078`  
		Last Modified: Fri, 24 Oct 2025 20:15:32 GMT  
		Size: 2.2 MB (2171917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88fee191536e0b5f4ac3d663c892026c66bded5f02b82e74fdd35dab855aebcc`  
		Last Modified: Fri, 24 Oct 2025 20:15:32 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:8a8a0731a9e5729912c6825063bf0f05638f83b2282d1fa5f29122f60a83dd3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73256862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d8e0098302e5e9a3146aa2a9dff256cf4f8ad82646d722f417f98a3c5e7ce0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:10 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa92403a7591eac3005b3589514439adb33ddfd0cdf573f41acb7b2f59795ad7`  
		Last Modified: Fri, 24 Oct 2025 19:26:43 GMT  
		Size: 3.4 MB (3428323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2061b8000d4d8033b2b8390df19f894b799a70f19e1b18ad00ff070e834c448`  
		Last Modified: Fri, 24 Oct 2025 19:26:43 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3886f04bed6533c2ca443852c6834c95a2bf593fa2353717502597cdc730e4`  
		Last Modified: Fri, 24 Oct 2025 19:26:43 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e31262a68741790bc75b7d52bb0dfcf6466cd97c612c50f09ded3fe6418555`  
		Last Modified: Fri, 24 Oct 2025 19:26:43 GMT  
		Size: 13.7 MB (13665835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4a424954978a6cd3cba5774af71e47d6c97e6728c83e3899b1fcd10ba52333`  
		Last Modified: Fri, 24 Oct 2025 19:26:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55585e557ba0bf347b587dbe97b2b0091e13e5412706d0085b7d73006580e619`  
		Last Modified: Fri, 24 Oct 2025 19:26:45 GMT  
		Size: 18.1 MB (18060211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976680173b043a978a102e54fc552619ac2d4451a582fedd2b5b10edf3c81e92`  
		Last Modified: Fri, 24 Oct 2025 19:26:44 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b3d35e48b94e248c82ef2b7b0963b920bc8ed6f3d8fc072513aac877448996`  
		Last Modified: Fri, 24 Oct 2025 19:26:45 GMT  
		Size: 19.9 KB (19861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aeeb1aabb5cdf8cb6f2f2083e84f2f065745a4b811b3e696b40c081e79549c9`  
		Last Modified: Fri, 24 Oct 2025 19:26:45 GMT  
		Size: 19.9 KB (19862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f50ecb5de6b2a764828b7e80a55568de1f3e08b01da01bede558990e54249a`  
		Last Modified: Fri, 24 Oct 2025 20:42:37 GMT  
		Size: 33.8 MB (33817685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199fc7d3655041ca726674511a54af7aa7e06c208a7c9fc486684a943e414b28`  
		Last Modified: Fri, 24 Oct 2025 20:42:36 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329a763f3c1b2a9af24106880b4d662addd61836e8ba1c1d339555de3ee73f9d`  
		Last Modified: Fri, 24 Oct 2025 20:42:36 GMT  
		Size: 736.2 KB (736163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd71e2d9ab85b2f85c2579f108bfb049211c12f23b0e8a2fa7c3ffcfb84d5b55`  
		Last Modified: Fri, 24 Oct 2025 20:42:36 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb209078f69abb5d309cfc93d9931327093107718ad214a3c38b51dc56dd59f`  
		Last Modified: Fri, 24 Oct 2025 20:42:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:5468b59883447c633cbb52ba5f3245f7d1c9cfd5bce330d85e97df02b3b9c8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2696c0a41081f3a1b2eb428b2ce647dee085693569892dabbecccce7bfd76946`

```dockerfile
```

-	Layers:
	-	`sha256:ce03e73d27d7ab6ccc257ea5a3f4aa35436f6d2f698f66ea1257d7d7dee8c899`  
		Last Modified: Fri, 24 Oct 2025 20:42:36 GMT  
		Size: 31.2 KB (31239 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:38402e43ff8e4cd428a730cf2ca0da259d45d63d56966a267592883356b3b261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70050749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d2bbb1d28ac7eedd28718f47750aea0696b60e8cc4486138881219a9318d61`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:18 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86befc8c1e2c60f4f39c9201e05c6113f90d2c2c1ba583801d2bb7fc0e048407`  
		Last Modified: Fri, 24 Oct 2025 20:00:09 GMT  
		Size: 3.2 MB (3244388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4090b522cebcb13ace81579f703a792840bd3a2a776d263f618377aa5ad7b837`  
		Last Modified: Fri, 24 Oct 2025 20:00:09 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4226203351d20410512f4260b17c28280033e70ab39fe4e8ca8faaedf80956d`  
		Last Modified: Fri, 24 Oct 2025 20:00:09 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29c954d853d3626c66559e0b82b75a2385f86c3cef8edcd79d3ba80879d8c36`  
		Last Modified: Fri, 24 Oct 2025 20:00:09 GMT  
		Size: 13.7 MB (13665830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88085d351af20bdba1e3ea33e4f437fefc126fd7027872482d442dac2321bb1c`  
		Last Modified: Fri, 24 Oct 2025 20:00:10 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4d1708b787357c5fad8011057efbea12d9483c0ebd8f38676c576073384744`  
		Last Modified: Fri, 24 Oct 2025 20:00:10 GMT  
		Size: 17.1 MB (17050299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b7b8bbe9073e735053fec9c6859ffbfa2c2104861c6bac6e158b43f20fafa6`  
		Last Modified: Fri, 24 Oct 2025 20:00:10 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16bc8c74e19be188069c5b2ca0c62e97ac5da7609764aaa91440656abca26f4`  
		Last Modified: Fri, 24 Oct 2025 20:00:11 GMT  
		Size: 19.9 KB (19857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a3e608ee86aa8bcad71953053412b2deb858a9f8563456f0cc30a004e4b5f6`  
		Last Modified: Fri, 24 Oct 2025 20:00:11 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b496992fd95d278fc615a6d681b3df6fce057c58b56c782d8236767de8085ca4`  
		Last Modified: Fri, 24 Oct 2025 20:50:32 GMT  
		Size: 32.1 MB (32097494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adda9bacbaacaf11314077d9d1f2ad447ec51704363faaca03cc3eaefccfa9a`  
		Last Modified: Fri, 24 Oct 2025 20:50:31 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad691cdddbcc251fb5123965de8d982c8fdf0539b96accd5e0dd06ab4bc8e62`  
		Last Modified: Fri, 24 Oct 2025 20:50:31 GMT  
		Size: 726.6 KB (726631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3df618c1f1a615a187a5a8f54b9da335dbddd69ec791d1c32be5b7342c5e9`  
		Last Modified: Fri, 24 Oct 2025 20:50:32 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b838b6672c3ea31406ab925fd8b445cfa08369f57c2b4a5b90c51cbe53087bf9`  
		Last Modified: Fri, 24 Oct 2025 20:50:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:90839f3d443aa02dcf8b4f108adbf2e97a2a2115afcf2d3a1b04339525689e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e523228cd25adc7aafbc9f9a926c7886b5b0b91510b36437d123b256508b43f5`

```dockerfile
```

-	Layers:
	-	`sha256:85ce9827390b67e3cddcd712131f608fb8f5135342d97eb9a45fe49bc28ca67a`  
		Last Modified: Fri, 24 Oct 2025 20:50:31 GMT  
		Size: 2.2 MB (2172233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d202613b539ab5cb3e6f61290c58ad176ef5daafe4af103009faa4827863d0`  
		Last Modified: Fri, 24 Oct 2025 20:50:31 GMT  
		Size: 31.5 KB (31453 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:5b44ff00b6ffb4c2cfdd5a109056cd49a8be67713f4f71d439d6200d3895f19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75592209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b56cfbb0460a8d58d50d0bfadec9763bbf817b723402080ce408a636c9942a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab8e5431b232ea17dba82b276ef0be159d4f17c1baa4241a844a7b01c3e1637`  
		Last Modified: Fri, 24 Oct 2025 19:09:22 GMT  
		Size: 3.5 MB (3466793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ef2c9705318e0150447a2c017caca15d03aed2a9d50610d8ac241df0800b20`  
		Last Modified: Fri, 24 Oct 2025 19:09:29 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d201919164abf67a0ef48a249f1129ca012b48e7e275a0ecf20a219e75e08f`  
		Last Modified: Fri, 24 Oct 2025 19:09:29 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3617909786220dc66fea0cc929755ca0582234f21f9664e785104fdbf6ad1a87`  
		Last Modified: Fri, 24 Oct 2025 19:09:30 GMT  
		Size: 13.7 MB (13665831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5126b2a8113f85f6bb3cf754a09409f4248aa53b64ecd13d4bc6cb77af320bb`  
		Last Modified: Fri, 24 Oct 2025 19:09:29 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bf9fd0c2ec689df2d35e738c05244d989cb6dd76d7e069cb46aa982f43b6ee`  
		Last Modified: Fri, 24 Oct 2025 19:09:31 GMT  
		Size: 19.5 MB (19504879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562973c5a4e7b322fc0a740f6e09b7a4f686f5b1e677635e9d5ebaee5d5bb349`  
		Last Modified: Fri, 24 Oct 2025 19:09:30 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90ec277e222ddd9149e8d97aa83ab3932d772a8b5dbbda2fccf70936b969646`  
		Last Modified: Fri, 24 Oct 2025 19:09:30 GMT  
		Size: 19.9 KB (19860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ede6f49d9776977104724e69dc09f925074d3f13b570cdaef7d98743219309`  
		Last Modified: Fri, 24 Oct 2025 19:09:31 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47e0817c1589b3a8c31cfd8f21fcd9d1d5a1bce7621341675d4824d0652be50`  
		Last Modified: Fri, 24 Oct 2025 20:19:09 GMT  
		Size: 34.0 MB (34036569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d1ebc8aa7aaa83d0b7718ebbcc1afadbab8007c29947b3a5ce90c9a9ba5ef4`  
		Last Modified: Fri, 24 Oct 2025 20:19:08 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608cbc8ecfe727dbd2ede43881a759a4343d037d71cf6bb6638d3bc665889446`  
		Last Modified: Fri, 24 Oct 2025 20:19:08 GMT  
		Size: 735.5 KB (735507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071babbe10a242439c89a9e6ad25c50e8f7dfc4ba73cd4d39f3a72319b317b9`  
		Last Modified: Fri, 24 Oct 2025 20:19:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f90b53632aee8eb5358956bff199a14db4c27d27191d47115ee8792fb44483`  
		Last Modified: Fri, 24 Oct 2025 20:19:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:4b8a94295da96c263657130630255549aee511d4ccb4cf8df294c223caee2622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47eaad1da7582b41691bc6257e0a916126c719e3f09f9f15ea0d386c17c9c621`

```dockerfile
```

-	Layers:
	-	`sha256:a581fae8deb1f9322c2e9c2421fd26fc26fbd8bc7bdb7591ead53fca565f8ed1`  
		Last Modified: Fri, 24 Oct 2025 20:19:08 GMT  
		Size: 2.2 MB (2172057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b94b1cdb98ebfd7140d88cb296f595e57246ec42cb3a366d1536879d21e13eb`  
		Last Modified: Fri, 24 Oct 2025 20:19:07 GMT  
		Size: 31.5 KB (31478 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:d5931ffe7ddaa2b8c280eece7cfb730f24c641e7cbdda5cad0a4fa4c26d0f50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76556135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3f21ef35e2080c1a9e315c584a10bf6e5b8e3b464ae9b5551d958ed6a2584e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd1047cb7f567073e37680da0f0c36a8876c5b443c64da4595cdec94c95024d`  
		Last Modified: Fri, 24 Oct 2025 18:41:48 GMT  
		Size: 3.5 MB (3522934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5432291532ac93ec85b0f03092c7de1698ed58f22f782a88d04612ec689a74`  
		Last Modified: Fri, 24 Oct 2025 18:41:48 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf46d8c3be72e693a97a1954ee7b7b2eb20280f895d12d327877769ad0e67ff`  
		Last Modified: Fri, 24 Oct 2025 18:41:48 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b239e840753cbefa4bb180374d7c4de7017b502a460c7c620aa2de485dea4a`  
		Last Modified: Fri, 24 Oct 2025 18:41:48 GMT  
		Size: 13.7 MB (13665807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ab54154fb78163d7eead7c5a48c6368ac258df68dbd81a9180669ba7b65578`  
		Last Modified: Fri, 24 Oct 2025 18:41:49 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2180045f81b8fe7a4380661a927a38a4193ab8d6c9b475c85cc78fb37e4c37`  
		Last Modified: Fri, 24 Oct 2025 18:41:49 GMT  
		Size: 20.5 MB (20487530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e06449af4deae637dc8823eb2707a0a77708c33956bad55ca2ef902a5079f9`  
		Last Modified: Fri, 24 Oct 2025 18:41:49 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b91cf49295a1961490a462be09ea0d948cec5dffe19693d07fd6482738d2`  
		Last Modified: Fri, 24 Oct 2025 18:41:50 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8433c5c2f5580dd81b3dcce9aa438908101b76876633367f4c63eecbc4f218`  
		Last Modified: Fri, 24 Oct 2025 18:41:50 GMT  
		Size: 20.0 KB (20041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836a5d5dc2ba5d6b83f610c968f5f78e537c713046bc3dfc23e1118c481dd21a`  
		Last Modified: Fri, 24 Oct 2025 19:20:37 GMT  
		Size: 34.5 MB (34468602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b7ea9d567b4cf490dd161bf3907e23a29c3d22680cc8bca898abf4e05d1a90`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1d5f987256f0839ccbdcdebe7345e065c5e9e2cc80cddcb505b88e03d3a598`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 747.4 KB (747393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c28bc494b31382832a91c6bf7ce60699575866f4aa870fd2f833d5eea0da9cc`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2de9e6df9ee11c875c4fb5488b02e6f8fc352cb8fb9f4776478e13e1a3a32d0`  
		Last Modified: Fri, 24 Oct 2025 19:20:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:9e08de58062e3aaf6c950ebe877739f1c8768692cd8f23a707a57ae9b7a8821b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a466f1c78f97c9b074d2a358200f5be94b841347eed3207d0ea1920e7469abe`

```dockerfile
```

-	Layers:
	-	`sha256:0de4281bb9c055fde212d6e18ad0e4bf9383b49c95ba02045e3726ee7929e0e0`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 2.2 MB (2171705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ab52739d09a0d44bcf8d60ac6468c70f60454a4dd190d164cc71554fd76e5e`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 31.3 KB (31325 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:f33d5c5a009118baf420169d571626ecd2648d8edc3fdd59cc782340caa13a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77931423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642ab0094838e9b27715efcb0a44a01704869672b4d027a6c46bf1faffb341a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:06 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a0b03903475651b081c7c705a4ab0f68ab5f5bba328735e8dae6e168526c7`  
		Last Modified: Thu, 09 Oct 2025 00:55:48 GMT  
		Size: 3.6 MB (3614664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436cae3ea479232d2bcf67ca55e6705ab3775fa412e53331855937a2a7340b65`  
		Last Modified: Thu, 09 Oct 2025 00:55:47 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1164e359044b0e56f99538c30031735fcef9128820673f06e10663118d04d0e3`  
		Last Modified: Thu, 09 Oct 2025 00:55:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef38c73f3ff68aca00580e73801a535a988fbae408500c93468879ece8ebc678`  
		Last Modified: Fri, 24 Oct 2025 21:07:11 GMT  
		Size: 13.7 MB (13665827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a00a631bb9c16ed735305bb12fd93d2488d0741a8597255ed7563e7d728ff6`  
		Last Modified: Fri, 24 Oct 2025 21:07:11 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ffa15173dd2c88e976a8bc9c8ea99dcc18e321d4772cd35742bbb8e2409539`  
		Last Modified: Fri, 24 Oct 2025 21:07:12 GMT  
		Size: 20.9 MB (20860688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c862d1dbc8c14714255edd6179331935441f0960bd0c4573e31796e9a82fceb1`  
		Last Modified: Fri, 24 Oct 2025 21:07:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f45502a2020d8d22fa7393e6cad99679762ffdee488a16af1535a5565cbaef`  
		Last Modified: Fri, 24 Oct 2025 21:07:12 GMT  
		Size: 19.9 KB (19878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2735766e59ead016c2e345f85fba01ed5c0352fbecf5e3007fb3749c5eb511`  
		Last Modified: Fri, 24 Oct 2025 21:07:12 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed081ffdd4491cb0756d8066e967a4ccfb6ec0396b925452d511692e5bee5cf`  
		Last Modified: Sat, 25 Oct 2025 03:01:00 GMT  
		Size: 35.3 MB (35270819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d6d368be31ca2cd1a1d82175e3dfc299bb7ecb217a2f8c6b43984b1f544666`  
		Last Modified: Sat, 25 Oct 2025 03:00:49 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c4e2341ac4473f2c7d9b0b244b2c599d9f2f56f47d629d0f32d5f86091532b`  
		Last Modified: Sat, 25 Oct 2025 03:03:23 GMT  
		Size: 742.6 KB (742573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd36a531da73ec90e635f870050c746ed1b6a71e88260b7e107d34aa9055176`  
		Last Modified: Sat, 25 Oct 2025 03:03:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e162c226fcf7b060ec6e08b1686f667222419866cd7944884b0e6be264a14bb`  
		Last Modified: Sat, 25 Oct 2025 03:03:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:ffcfb1757ad65a0d99f0bc161dd0e9ba902a595fa1cf789ec2d1f798146ec2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c047948f85dd1ea3d1adb10a2fd734a7a867601f3d68e78826d352499f49407`

```dockerfile
```

-	Layers:
	-	`sha256:d2fbfcb3f383849927f99f670f4862a13fc7980bc0a001ad8afafd454245af82`  
		Last Modified: Sat, 25 Oct 2025 03:03:23 GMT  
		Size: 2.2 MB (2170474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52cb1b756733811a62001df4106a04fb49ab1de0eed371438e57d07a5127878a`  
		Last Modified: Sat, 25 Oct 2025 03:03:22 GMT  
		Size: 31.4 KB (31397 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:72145d70874f9ec0a6d8fe983e574a6b52954b33fb04fed585cc4f3a5268e992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72068576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc8a1bb5749686a1bca2db46be7ec6216602970644d17b93380df2ed267f5a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:17:39 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e9f10e445dbf7ba866462dd44d0f912a09342dc97a4685769a2d057bcc7a9`  
		Last Modified: Thu, 09 Oct 2025 06:22:25 GMT  
		Size: 3.6 MB (3600269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579c35b4a5055268b9ccb82f8c3307c0a781af77168952679399ed4bde3b60a`  
		Last Modified: Thu, 09 Oct 2025 06:22:25 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b6a920874b5f6759a41702af348a1eefb32a0674eeae4cd9d750418594caed`  
		Last Modified: Thu, 09 Oct 2025 06:22:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b115bacca67276dbf1b2b88c75a1d93a783abab20ad055d2f456784c91848a14`  
		Last Modified: Sat, 25 Oct 2025 20:07:15 GMT  
		Size: 13.7 MB (13665823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa643ca26895c691b4910d72fd561ed485d1c71232f505a04f7dcb490535d6a`  
		Last Modified: Sat, 25 Oct 2025 20:07:11 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44636f1994b8c2c675720920a0bb9789fc6eb6430fb3a1c1974a2f23fc45ca6`  
		Last Modified: Sat, 25 Oct 2025 20:07:16 GMT  
		Size: 19.4 MB (19378197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0854e2c2237480c7d7f110ec7531105a011961145c5893d54f299a3df5088a2`  
		Last Modified: Sat, 25 Oct 2025 20:07:11 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22295fbf4555881f21a134879c902bd8d957ab88ae584338de3d78f06ada96e`  
		Last Modified: Sat, 25 Oct 2025 20:07:12 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636c9b936e891b05b8c2e03882ad5bb801f88243f72d98c408a0c8215b115e5a`  
		Last Modified: Sat, 25 Oct 2025 20:07:13 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97265ab6c7c326358cedb79d9ac403cf23c21c7ded2d00a8b85ad62cc6eca37`  
		Last Modified: Mon, 27 Oct 2025 05:38:18 GMT  
		Size: 31.1 MB (31131201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89604a377b9c68f35a228966a3bd72ac71d70fd8a335963f9cfe406f225e15c4`  
		Last Modified: Mon, 27 Oct 2025 05:38:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a2dc4841380c0781fabbcca634c3fb89f7234c09019b88b2d7135c26c8a21e`  
		Last Modified: Mon, 27 Oct 2025 05:50:33 GMT  
		Size: 733.3 KB (733269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1f5b878c4f175244e47161bb30c3011a875d49c85d78710eceb0be3242f4b8`  
		Last Modified: Mon, 27 Oct 2025 05:50:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99f8f3f92e67b642f6a05cb3c952373d01f6134bbf85bfe97467459be5ad805`  
		Last Modified: Mon, 27 Oct 2025 05:49:52 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:292baeff292e1baab0f702b58a5d03e2c453deeaa01265501a44450cb1433659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0b70f3631d1638e1fdbd7f163130604a6d972bb325618e641fec33fb9e73cf`

```dockerfile
```

-	Layers:
	-	`sha256:89f1ca74a0086b17ccbbfc51180873244e1f5865dc41b3fca9d752011a20da4a`  
		Last Modified: Mon, 27 Oct 2025 05:50:33 GMT  
		Size: 2.2 MB (2168741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61708f796761d77926081020402ea14d43fd149c0253455ca87be36072ab81c`  
		Last Modified: Mon, 27 Oct 2025 05:50:33 GMT  
		Size: 31.4 KB (31398 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:e306b9d0761d031fb405d31761b59db64fb68f9cc0bb603701e70631d2c2f611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73641484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1987d9313acb745a6e210afd202e8607e699b06197bfd317a60885241822b83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:18 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d2dd4bd3263db65246a0eede02512575e505bf72959ea5d8d1c7f5b3dea5e`  
		Last Modified: Thu, 09 Oct 2025 00:53:56 GMT  
		Size: 3.7 MB (3692716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e39eb5e282665e4bd0e90c53a85f696e72ef63e8ef403c40cc9e67742ffe824`  
		Last Modified: Thu, 09 Oct 2025 00:53:56 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0608d8b4902677a8ba1ccd4d718738714fa13e782091c89842c948b06a52f8`  
		Last Modified: Thu, 09 Oct 2025 00:53:56 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdea27060aabd36ff31ca9055725e9085bf08b94fc0d4b40028e0d7c21102f40`  
		Last Modified: Fri, 24 Oct 2025 20:03:24 GMT  
		Size: 13.7 MB (13665851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70515c51ba3110abd59c349a4cca83963c57d9e8eea1f5a9531ee7dafa31ec26`  
		Last Modified: Fri, 24 Oct 2025 20:03:24 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66a11b7c047c1150c15ec0166e1c3737640f6f9ed49c8b67614c8e0e4672cac`  
		Last Modified: Fri, 24 Oct 2025 20:03:24 GMT  
		Size: 20.0 MB (19973403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695d42787f851983f0874071c409307ecdef1c5f9c0f9e6ad3a2f2ce05caf777`  
		Last Modified: Fri, 24 Oct 2025 20:03:24 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2093cfdb1b47e177d32873991ccf3e5cd21236d50791db5baa480c7dd48de0`  
		Last Modified: Fri, 24 Oct 2025 20:03:24 GMT  
		Size: 19.9 KB (19877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d5e698d2cc5b0e0597cf3c7da7ac79ed39aa63a8b61eebb22ad2e642482d87`  
		Last Modified: Fri, 24 Oct 2025 20:03:24 GMT  
		Size: 19.9 KB (19877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b060327ba474d1cf63109f15475371951efdc6ef2c7efb8f661feddd98182e3b`  
		Last Modified: Sat, 25 Oct 2025 02:00:42 GMT  
		Size: 31.9 MB (31876783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873c78c6813aebbe53313c614bdf3ec6a120060f40b61687560613d1f850a980`  
		Last Modified: Sat, 25 Oct 2025 02:00:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4824920824ff0a317ee8173e9b0bf4f661ffa147eba75522c2c53595eed2ee72`  
		Last Modified: Sat, 25 Oct 2025 02:02:31 GMT  
		Size: 738.9 KB (738885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2112d62c5a43f45c87ec4a6f27c36c2fd539d17e710af12efe7caaa00e1d0f9`  
		Last Modified: Sat, 25 Oct 2025 02:02:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3d1196770491fd3a90d7aa8b8374f28eb48ee47e4d5c48c84d392197614dfb`  
		Last Modified: Sat, 25 Oct 2025 02:02:31 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:3184d29d8ad0c72790246a71189d2e1fcf37cb94f752f29f67069088686e7728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74a75671343f7c90f2ee9029052377eedc2260a728a72289167761af27a5163`

```dockerfile
```

-	Layers:
	-	`sha256:e58711673c2ddcc53ad516eb97ef9252b13a98a4c396f0ec8cc6cf4814ac789a`  
		Last Modified: Sat, 25 Oct 2025 02:02:31 GMT  
		Size: 2.2 MB (2168529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e25a4a3503bfedc7a99b5b5ec2cf1aef371400473c7419eb078f7897c98830`  
		Last Modified: Sat, 25 Oct 2025 02:02:31 GMT  
		Size: 31.4 KB (31355 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:dbc308a7af43fd5b1084ced476e67df2a34e04371100fae720f4893321f23c6d
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
$ docker pull composer@sha256:24fceab78a0b2bccf763b67cb68a85bb69c8e316e5de31bf994fd071f6cf6337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75615868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72bd535adaec9b3ebdfa7b381f96653138f8cab9236249566b8c4f619ff344bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1329c5084d624e0d041d09a190180a44c4d82bf87d29e37124d02a5a4e0e5809`  
		Last Modified: Fri, 24 Oct 2025 19:26:00 GMT  
		Size: 3.5 MB (3463762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc671ef6f9c8e605c15a2d5b9c5be998079cc5cb98e73b58591ca25b97d06def`  
		Last Modified: Fri, 24 Oct 2025 19:26:00 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f413b510cd4a8a8656c38f987bbade3f59c7bba10d1ef2fe4a7afdecf50f70c3`  
		Last Modified: Fri, 24 Oct 2025 19:26:00 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5a2611d454825d1788a2b6b2ad376f47fe60d51390ede78cf08cfbd90122e5`  
		Last Modified: Fri, 24 Oct 2025 19:26:00 GMT  
		Size: 13.7 MB (13665838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad217014f3d0bb47bf766b15315a769b1fd80034bcc74e903a36e5c3a155b48c`  
		Last Modified: Fri, 24 Oct 2025 19:26:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800a2b6306a04e9d843a5fc18f1a71fa23b74b09cb7480943467be42458dcfd4`  
		Last Modified: Fri, 24 Oct 2025 19:26:02 GMT  
		Size: 20.0 MB (19955567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb47194af07c23ba476c82020f5c6462ec00ed66bd357a5c32d2cbb7da720585`  
		Last Modified: Fri, 24 Oct 2025 19:26:01 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb8c0d2cc28beed1de437b76f9be01318026f15cc601009f46c36954cdd96e0`  
		Last Modified: Fri, 24 Oct 2025 19:26:02 GMT  
		Size: 20.1 KB (20073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed107248614865eca656b1bffadfb13a230adca7df1bcde3220f3bd98d898f3`  
		Last Modified: Fri, 24 Oct 2025 19:26:02 GMT  
		Size: 20.1 KB (20071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a77d225a4093408ffc09f88e84ceecb9a9237fce71c0c2e253da24dba08370e`  
		Last Modified: Fri, 24 Oct 2025 20:15:33 GMT  
		Size: 33.9 MB (33947738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58861f8d0fbf31403e66960ced7a82c738d6ab53693214ff5f3fc15eaf3d6ae0`  
		Last Modified: Fri, 24 Oct 2025 20:15:32 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428d0474586e75f564c8fb583700920feb4e9cff72c624ba23af2eb21e00953f`  
		Last Modified: Fri, 24 Oct 2025 20:15:32 GMT  
		Size: 735.5 KB (735524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2b7ddc51d0e4faafc87372c0be76bf07826c6b188c8a6abdce072c69fe4c`  
		Last Modified: Fri, 24 Oct 2025 20:15:32 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e28c9c8dfe1ad11e48c41658e1e3aa78ead447e93a75f771f2b08463a1b21af`  
		Last Modified: Fri, 24 Oct 2025 20:15:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:b3a3a57911d32bffebd31262aaec3838ebb3cde1f662d49e437a9e5130905838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3acd5795d652baf2e335ac4b4b155986ae965e54b50d15835834d518d482a08`

```dockerfile
```

-	Layers:
	-	`sha256:a734a51ed57dcddb9fde01424686ee059ec94007b5fd6e1fb7e453143d190078`  
		Last Modified: Fri, 24 Oct 2025 20:15:32 GMT  
		Size: 2.2 MB (2171917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88fee191536e0b5f4ac3d663c892026c66bded5f02b82e74fdd35dab855aebcc`  
		Last Modified: Fri, 24 Oct 2025 20:15:32 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:8a8a0731a9e5729912c6825063bf0f05638f83b2282d1fa5f29122f60a83dd3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73256862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d8e0098302e5e9a3146aa2a9dff256cf4f8ad82646d722f417f98a3c5e7ce0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:10 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa92403a7591eac3005b3589514439adb33ddfd0cdf573f41acb7b2f59795ad7`  
		Last Modified: Fri, 24 Oct 2025 19:26:43 GMT  
		Size: 3.4 MB (3428323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2061b8000d4d8033b2b8390df19f894b799a70f19e1b18ad00ff070e834c448`  
		Last Modified: Fri, 24 Oct 2025 19:26:43 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3886f04bed6533c2ca443852c6834c95a2bf593fa2353717502597cdc730e4`  
		Last Modified: Fri, 24 Oct 2025 19:26:43 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e31262a68741790bc75b7d52bb0dfcf6466cd97c612c50f09ded3fe6418555`  
		Last Modified: Fri, 24 Oct 2025 19:26:43 GMT  
		Size: 13.7 MB (13665835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4a424954978a6cd3cba5774af71e47d6c97e6728c83e3899b1fcd10ba52333`  
		Last Modified: Fri, 24 Oct 2025 19:26:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55585e557ba0bf347b587dbe97b2b0091e13e5412706d0085b7d73006580e619`  
		Last Modified: Fri, 24 Oct 2025 19:26:45 GMT  
		Size: 18.1 MB (18060211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976680173b043a978a102e54fc552619ac2d4451a582fedd2b5b10edf3c81e92`  
		Last Modified: Fri, 24 Oct 2025 19:26:44 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b3d35e48b94e248c82ef2b7b0963b920bc8ed6f3d8fc072513aac877448996`  
		Last Modified: Fri, 24 Oct 2025 19:26:45 GMT  
		Size: 19.9 KB (19861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aeeb1aabb5cdf8cb6f2f2083e84f2f065745a4b811b3e696b40c081e79549c9`  
		Last Modified: Fri, 24 Oct 2025 19:26:45 GMT  
		Size: 19.9 KB (19862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f50ecb5de6b2a764828b7e80a55568de1f3e08b01da01bede558990e54249a`  
		Last Modified: Fri, 24 Oct 2025 20:42:37 GMT  
		Size: 33.8 MB (33817685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199fc7d3655041ca726674511a54af7aa7e06c208a7c9fc486684a943e414b28`  
		Last Modified: Fri, 24 Oct 2025 20:42:36 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329a763f3c1b2a9af24106880b4d662addd61836e8ba1c1d339555de3ee73f9d`  
		Last Modified: Fri, 24 Oct 2025 20:42:36 GMT  
		Size: 736.2 KB (736163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd71e2d9ab85b2f85c2579f108bfb049211c12f23b0e8a2fa7c3ffcfb84d5b55`  
		Last Modified: Fri, 24 Oct 2025 20:42:36 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb209078f69abb5d309cfc93d9931327093107718ad214a3c38b51dc56dd59f`  
		Last Modified: Fri, 24 Oct 2025 20:42:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:5468b59883447c633cbb52ba5f3245f7d1c9cfd5bce330d85e97df02b3b9c8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2696c0a41081f3a1b2eb428b2ce647dee085693569892dabbecccce7bfd76946`

```dockerfile
```

-	Layers:
	-	`sha256:ce03e73d27d7ab6ccc257ea5a3f4aa35436f6d2f698f66ea1257d7d7dee8c899`  
		Last Modified: Fri, 24 Oct 2025 20:42:36 GMT  
		Size: 31.2 KB (31239 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:38402e43ff8e4cd428a730cf2ca0da259d45d63d56966a267592883356b3b261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70050749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d2bbb1d28ac7eedd28718f47750aea0696b60e8cc4486138881219a9318d61`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:18 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86befc8c1e2c60f4f39c9201e05c6113f90d2c2c1ba583801d2bb7fc0e048407`  
		Last Modified: Fri, 24 Oct 2025 20:00:09 GMT  
		Size: 3.2 MB (3244388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4090b522cebcb13ace81579f703a792840bd3a2a776d263f618377aa5ad7b837`  
		Last Modified: Fri, 24 Oct 2025 20:00:09 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4226203351d20410512f4260b17c28280033e70ab39fe4e8ca8faaedf80956d`  
		Last Modified: Fri, 24 Oct 2025 20:00:09 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29c954d853d3626c66559e0b82b75a2385f86c3cef8edcd79d3ba80879d8c36`  
		Last Modified: Fri, 24 Oct 2025 20:00:09 GMT  
		Size: 13.7 MB (13665830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88085d351af20bdba1e3ea33e4f437fefc126fd7027872482d442dac2321bb1c`  
		Last Modified: Fri, 24 Oct 2025 20:00:10 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4d1708b787357c5fad8011057efbea12d9483c0ebd8f38676c576073384744`  
		Last Modified: Fri, 24 Oct 2025 20:00:10 GMT  
		Size: 17.1 MB (17050299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b7b8bbe9073e735053fec9c6859ffbfa2c2104861c6bac6e158b43f20fafa6`  
		Last Modified: Fri, 24 Oct 2025 20:00:10 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16bc8c74e19be188069c5b2ca0c62e97ac5da7609764aaa91440656abca26f4`  
		Last Modified: Fri, 24 Oct 2025 20:00:11 GMT  
		Size: 19.9 KB (19857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a3e608ee86aa8bcad71953053412b2deb858a9f8563456f0cc30a004e4b5f6`  
		Last Modified: Fri, 24 Oct 2025 20:00:11 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b496992fd95d278fc615a6d681b3df6fce057c58b56c782d8236767de8085ca4`  
		Last Modified: Fri, 24 Oct 2025 20:50:32 GMT  
		Size: 32.1 MB (32097494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adda9bacbaacaf11314077d9d1f2ad447ec51704363faaca03cc3eaefccfa9a`  
		Last Modified: Fri, 24 Oct 2025 20:50:31 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad691cdddbcc251fb5123965de8d982c8fdf0539b96accd5e0dd06ab4bc8e62`  
		Last Modified: Fri, 24 Oct 2025 20:50:31 GMT  
		Size: 726.6 KB (726631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3df618c1f1a615a187a5a8f54b9da335dbddd69ec791d1c32be5b7342c5e9`  
		Last Modified: Fri, 24 Oct 2025 20:50:32 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b838b6672c3ea31406ab925fd8b445cfa08369f57c2b4a5b90c51cbe53087bf9`  
		Last Modified: Fri, 24 Oct 2025 20:50:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:90839f3d443aa02dcf8b4f108adbf2e97a2a2115afcf2d3a1b04339525689e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e523228cd25adc7aafbc9f9a926c7886b5b0b91510b36437d123b256508b43f5`

```dockerfile
```

-	Layers:
	-	`sha256:85ce9827390b67e3cddcd712131f608fb8f5135342d97eb9a45fe49bc28ca67a`  
		Last Modified: Fri, 24 Oct 2025 20:50:31 GMT  
		Size: 2.2 MB (2172233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d202613b539ab5cb3e6f61290c58ad176ef5daafe4af103009faa4827863d0`  
		Last Modified: Fri, 24 Oct 2025 20:50:31 GMT  
		Size: 31.5 KB (31453 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:5b44ff00b6ffb4c2cfdd5a109056cd49a8be67713f4f71d439d6200d3895f19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75592209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b56cfbb0460a8d58d50d0bfadec9763bbf817b723402080ce408a636c9942a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab8e5431b232ea17dba82b276ef0be159d4f17c1baa4241a844a7b01c3e1637`  
		Last Modified: Fri, 24 Oct 2025 19:09:22 GMT  
		Size: 3.5 MB (3466793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ef2c9705318e0150447a2c017caca15d03aed2a9d50610d8ac241df0800b20`  
		Last Modified: Fri, 24 Oct 2025 19:09:29 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d201919164abf67a0ef48a249f1129ca012b48e7e275a0ecf20a219e75e08f`  
		Last Modified: Fri, 24 Oct 2025 19:09:29 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3617909786220dc66fea0cc929755ca0582234f21f9664e785104fdbf6ad1a87`  
		Last Modified: Fri, 24 Oct 2025 19:09:30 GMT  
		Size: 13.7 MB (13665831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5126b2a8113f85f6bb3cf754a09409f4248aa53b64ecd13d4bc6cb77af320bb`  
		Last Modified: Fri, 24 Oct 2025 19:09:29 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bf9fd0c2ec689df2d35e738c05244d989cb6dd76d7e069cb46aa982f43b6ee`  
		Last Modified: Fri, 24 Oct 2025 19:09:31 GMT  
		Size: 19.5 MB (19504879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562973c5a4e7b322fc0a740f6e09b7a4f686f5b1e677635e9d5ebaee5d5bb349`  
		Last Modified: Fri, 24 Oct 2025 19:09:30 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90ec277e222ddd9149e8d97aa83ab3932d772a8b5dbbda2fccf70936b969646`  
		Last Modified: Fri, 24 Oct 2025 19:09:30 GMT  
		Size: 19.9 KB (19860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ede6f49d9776977104724e69dc09f925074d3f13b570cdaef7d98743219309`  
		Last Modified: Fri, 24 Oct 2025 19:09:31 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47e0817c1589b3a8c31cfd8f21fcd9d1d5a1bce7621341675d4824d0652be50`  
		Last Modified: Fri, 24 Oct 2025 20:19:09 GMT  
		Size: 34.0 MB (34036569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d1ebc8aa7aaa83d0b7718ebbcc1afadbab8007c29947b3a5ce90c9a9ba5ef4`  
		Last Modified: Fri, 24 Oct 2025 20:19:08 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608cbc8ecfe727dbd2ede43881a759a4343d037d71cf6bb6638d3bc665889446`  
		Last Modified: Fri, 24 Oct 2025 20:19:08 GMT  
		Size: 735.5 KB (735507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071babbe10a242439c89a9e6ad25c50e8f7dfc4ba73cd4d39f3a72319b317b9`  
		Last Modified: Fri, 24 Oct 2025 20:19:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f90b53632aee8eb5358956bff199a14db4c27d27191d47115ee8792fb44483`  
		Last Modified: Fri, 24 Oct 2025 20:19:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:4b8a94295da96c263657130630255549aee511d4ccb4cf8df294c223caee2622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47eaad1da7582b41691bc6257e0a916126c719e3f09f9f15ea0d386c17c9c621`

```dockerfile
```

-	Layers:
	-	`sha256:a581fae8deb1f9322c2e9c2421fd26fc26fbd8bc7bdb7591ead53fca565f8ed1`  
		Last Modified: Fri, 24 Oct 2025 20:19:08 GMT  
		Size: 2.2 MB (2172057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b94b1cdb98ebfd7140d88cb296f595e57246ec42cb3a366d1536879d21e13eb`  
		Last Modified: Fri, 24 Oct 2025 20:19:07 GMT  
		Size: 31.5 KB (31478 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:d5931ffe7ddaa2b8c280eece7cfb730f24c641e7cbdda5cad0a4fa4c26d0f50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76556135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3f21ef35e2080c1a9e315c584a10bf6e5b8e3b464ae9b5551d958ed6a2584e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd1047cb7f567073e37680da0f0c36a8876c5b443c64da4595cdec94c95024d`  
		Last Modified: Fri, 24 Oct 2025 18:41:48 GMT  
		Size: 3.5 MB (3522934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5432291532ac93ec85b0f03092c7de1698ed58f22f782a88d04612ec689a74`  
		Last Modified: Fri, 24 Oct 2025 18:41:48 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf46d8c3be72e693a97a1954ee7b7b2eb20280f895d12d327877769ad0e67ff`  
		Last Modified: Fri, 24 Oct 2025 18:41:48 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b239e840753cbefa4bb180374d7c4de7017b502a460c7c620aa2de485dea4a`  
		Last Modified: Fri, 24 Oct 2025 18:41:48 GMT  
		Size: 13.7 MB (13665807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ab54154fb78163d7eead7c5a48c6368ac258df68dbd81a9180669ba7b65578`  
		Last Modified: Fri, 24 Oct 2025 18:41:49 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2180045f81b8fe7a4380661a927a38a4193ab8d6c9b475c85cc78fb37e4c37`  
		Last Modified: Fri, 24 Oct 2025 18:41:49 GMT  
		Size: 20.5 MB (20487530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e06449af4deae637dc8823eb2707a0a77708c33956bad55ca2ef902a5079f9`  
		Last Modified: Fri, 24 Oct 2025 18:41:49 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940b91cf49295a1961490a462be09ea0d948cec5dffe19693d07fd6482738d2`  
		Last Modified: Fri, 24 Oct 2025 18:41:50 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8433c5c2f5580dd81b3dcce9aa438908101b76876633367f4c63eecbc4f218`  
		Last Modified: Fri, 24 Oct 2025 18:41:50 GMT  
		Size: 20.0 KB (20041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836a5d5dc2ba5d6b83f610c968f5f78e537c713046bc3dfc23e1118c481dd21a`  
		Last Modified: Fri, 24 Oct 2025 19:20:37 GMT  
		Size: 34.5 MB (34468602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b7ea9d567b4cf490dd161bf3907e23a29c3d22680cc8bca898abf4e05d1a90`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1d5f987256f0839ccbdcdebe7345e065c5e9e2cc80cddcb505b88e03d3a598`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 747.4 KB (747393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c28bc494b31382832a91c6bf7ce60699575866f4aa870fd2f833d5eea0da9cc`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2de9e6df9ee11c875c4fb5488b02e6f8fc352cb8fb9f4776478e13e1a3a32d0`  
		Last Modified: Fri, 24 Oct 2025 19:20:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:9e08de58062e3aaf6c950ebe877739f1c8768692cd8f23a707a57ae9b7a8821b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a466f1c78f97c9b074d2a358200f5be94b841347eed3207d0ea1920e7469abe`

```dockerfile
```

-	Layers:
	-	`sha256:0de4281bb9c055fde212d6e18ad0e4bf9383b49c95ba02045e3726ee7929e0e0`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 2.2 MB (2171705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ab52739d09a0d44bcf8d60ac6468c70f60454a4dd190d164cc71554fd76e5e`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 31.3 KB (31325 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:f33d5c5a009118baf420169d571626ecd2648d8edc3fdd59cc782340caa13a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77931423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642ab0094838e9b27715efcb0a44a01704869672b4d027a6c46bf1faffb341a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:06 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a0b03903475651b081c7c705a4ab0f68ab5f5bba328735e8dae6e168526c7`  
		Last Modified: Thu, 09 Oct 2025 00:55:48 GMT  
		Size: 3.6 MB (3614664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436cae3ea479232d2bcf67ca55e6705ab3775fa412e53331855937a2a7340b65`  
		Last Modified: Thu, 09 Oct 2025 00:55:47 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1164e359044b0e56f99538c30031735fcef9128820673f06e10663118d04d0e3`  
		Last Modified: Thu, 09 Oct 2025 00:55:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef38c73f3ff68aca00580e73801a535a988fbae408500c93468879ece8ebc678`  
		Last Modified: Fri, 24 Oct 2025 21:07:11 GMT  
		Size: 13.7 MB (13665827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a00a631bb9c16ed735305bb12fd93d2488d0741a8597255ed7563e7d728ff6`  
		Last Modified: Fri, 24 Oct 2025 21:07:11 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ffa15173dd2c88e976a8bc9c8ea99dcc18e321d4772cd35742bbb8e2409539`  
		Last Modified: Fri, 24 Oct 2025 21:07:12 GMT  
		Size: 20.9 MB (20860688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c862d1dbc8c14714255edd6179331935441f0960bd0c4573e31796e9a82fceb1`  
		Last Modified: Fri, 24 Oct 2025 21:07:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f45502a2020d8d22fa7393e6cad99679762ffdee488a16af1535a5565cbaef`  
		Last Modified: Fri, 24 Oct 2025 21:07:12 GMT  
		Size: 19.9 KB (19878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2735766e59ead016c2e345f85fba01ed5c0352fbecf5e3007fb3749c5eb511`  
		Last Modified: Fri, 24 Oct 2025 21:07:12 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed081ffdd4491cb0756d8066e967a4ccfb6ec0396b925452d511692e5bee5cf`  
		Last Modified: Sat, 25 Oct 2025 03:01:00 GMT  
		Size: 35.3 MB (35270819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d6d368be31ca2cd1a1d82175e3dfc299bb7ecb217a2f8c6b43984b1f544666`  
		Last Modified: Sat, 25 Oct 2025 03:00:49 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c4e2341ac4473f2c7d9b0b244b2c599d9f2f56f47d629d0f32d5f86091532b`  
		Last Modified: Sat, 25 Oct 2025 03:03:23 GMT  
		Size: 742.6 KB (742573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd36a531da73ec90e635f870050c746ed1b6a71e88260b7e107d34aa9055176`  
		Last Modified: Sat, 25 Oct 2025 03:03:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e162c226fcf7b060ec6e08b1686f667222419866cd7944884b0e6be264a14bb`  
		Last Modified: Sat, 25 Oct 2025 03:03:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:ffcfb1757ad65a0d99f0bc161dd0e9ba902a595fa1cf789ec2d1f798146ec2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c047948f85dd1ea3d1adb10a2fd734a7a867601f3d68e78826d352499f49407`

```dockerfile
```

-	Layers:
	-	`sha256:d2fbfcb3f383849927f99f670f4862a13fc7980bc0a001ad8afafd454245af82`  
		Last Modified: Sat, 25 Oct 2025 03:03:23 GMT  
		Size: 2.2 MB (2170474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52cb1b756733811a62001df4106a04fb49ab1de0eed371438e57d07a5127878a`  
		Last Modified: Sat, 25 Oct 2025 03:03:22 GMT  
		Size: 31.4 KB (31397 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:72145d70874f9ec0a6d8fe983e574a6b52954b33fb04fed585cc4f3a5268e992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72068576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc8a1bb5749686a1bca2db46be7ec6216602970644d17b93380df2ed267f5a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:17:39 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e9f10e445dbf7ba866462dd44d0f912a09342dc97a4685769a2d057bcc7a9`  
		Last Modified: Thu, 09 Oct 2025 06:22:25 GMT  
		Size: 3.6 MB (3600269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579c35b4a5055268b9ccb82f8c3307c0a781af77168952679399ed4bde3b60a`  
		Last Modified: Thu, 09 Oct 2025 06:22:25 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b6a920874b5f6759a41702af348a1eefb32a0674eeae4cd9d750418594caed`  
		Last Modified: Thu, 09 Oct 2025 06:22:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b115bacca67276dbf1b2b88c75a1d93a783abab20ad055d2f456784c91848a14`  
		Last Modified: Sat, 25 Oct 2025 20:07:15 GMT  
		Size: 13.7 MB (13665823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa643ca26895c691b4910d72fd561ed485d1c71232f505a04f7dcb490535d6a`  
		Last Modified: Sat, 25 Oct 2025 20:07:11 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44636f1994b8c2c675720920a0bb9789fc6eb6430fb3a1c1974a2f23fc45ca6`  
		Last Modified: Sat, 25 Oct 2025 20:07:16 GMT  
		Size: 19.4 MB (19378197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0854e2c2237480c7d7f110ec7531105a011961145c5893d54f299a3df5088a2`  
		Last Modified: Sat, 25 Oct 2025 20:07:11 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22295fbf4555881f21a134879c902bd8d957ab88ae584338de3d78f06ada96e`  
		Last Modified: Sat, 25 Oct 2025 20:07:12 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636c9b936e891b05b8c2e03882ad5bb801f88243f72d98c408a0c8215b115e5a`  
		Last Modified: Sat, 25 Oct 2025 20:07:13 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97265ab6c7c326358cedb79d9ac403cf23c21c7ded2d00a8b85ad62cc6eca37`  
		Last Modified: Mon, 27 Oct 2025 05:38:18 GMT  
		Size: 31.1 MB (31131201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89604a377b9c68f35a228966a3bd72ac71d70fd8a335963f9cfe406f225e15c4`  
		Last Modified: Mon, 27 Oct 2025 05:38:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a2dc4841380c0781fabbcca634c3fb89f7234c09019b88b2d7135c26c8a21e`  
		Last Modified: Mon, 27 Oct 2025 05:50:33 GMT  
		Size: 733.3 KB (733269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1f5b878c4f175244e47161bb30c3011a875d49c85d78710eceb0be3242f4b8`  
		Last Modified: Mon, 27 Oct 2025 05:50:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99f8f3f92e67b642f6a05cb3c952373d01f6134bbf85bfe97467459be5ad805`  
		Last Modified: Mon, 27 Oct 2025 05:49:52 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:292baeff292e1baab0f702b58a5d03e2c453deeaa01265501a44450cb1433659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0b70f3631d1638e1fdbd7f163130604a6d972bb325618e641fec33fb9e73cf`

```dockerfile
```

-	Layers:
	-	`sha256:89f1ca74a0086b17ccbbfc51180873244e1f5865dc41b3fca9d752011a20da4a`  
		Last Modified: Mon, 27 Oct 2025 05:50:33 GMT  
		Size: 2.2 MB (2168741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61708f796761d77926081020402ea14d43fd149c0253455ca87be36072ab81c`  
		Last Modified: Mon, 27 Oct 2025 05:50:33 GMT  
		Size: 31.4 KB (31398 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:e306b9d0761d031fb405d31761b59db64fb68f9cc0bb603701e70631d2c2f611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73641484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1987d9313acb745a6e210afd202e8607e699b06197bfd317a60885241822b83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.14
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:18 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d2dd4bd3263db65246a0eede02512575e505bf72959ea5d8d1c7f5b3dea5e`  
		Last Modified: Thu, 09 Oct 2025 00:53:56 GMT  
		Size: 3.7 MB (3692716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e39eb5e282665e4bd0e90c53a85f696e72ef63e8ef403c40cc9e67742ffe824`  
		Last Modified: Thu, 09 Oct 2025 00:53:56 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0608d8b4902677a8ba1ccd4d718738714fa13e782091c89842c948b06a52f8`  
		Last Modified: Thu, 09 Oct 2025 00:53:56 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdea27060aabd36ff31ca9055725e9085bf08b94fc0d4b40028e0d7c21102f40`  
		Last Modified: Fri, 24 Oct 2025 20:03:24 GMT  
		Size: 13.7 MB (13665851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70515c51ba3110abd59c349a4cca83963c57d9e8eea1f5a9531ee7dafa31ec26`  
		Last Modified: Fri, 24 Oct 2025 20:03:24 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66a11b7c047c1150c15ec0166e1c3737640f6f9ed49c8b67614c8e0e4672cac`  
		Last Modified: Fri, 24 Oct 2025 20:03:24 GMT  
		Size: 20.0 MB (19973403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695d42787f851983f0874071c409307ecdef1c5f9c0f9e6ad3a2f2ce05caf777`  
		Last Modified: Fri, 24 Oct 2025 20:03:24 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2093cfdb1b47e177d32873991ccf3e5cd21236d50791db5baa480c7dd48de0`  
		Last Modified: Fri, 24 Oct 2025 20:03:24 GMT  
		Size: 19.9 KB (19877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d5e698d2cc5b0e0597cf3c7da7ac79ed39aa63a8b61eebb22ad2e642482d87`  
		Last Modified: Fri, 24 Oct 2025 20:03:24 GMT  
		Size: 19.9 KB (19877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b060327ba474d1cf63109f15475371951efdc6ef2c7efb8f661feddd98182e3b`  
		Last Modified: Sat, 25 Oct 2025 02:00:42 GMT  
		Size: 31.9 MB (31876783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873c78c6813aebbe53313c614bdf3ec6a120060f40b61687560613d1f850a980`  
		Last Modified: Sat, 25 Oct 2025 02:00:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4824920824ff0a317ee8173e9b0bf4f661ffa147eba75522c2c53595eed2ee72`  
		Last Modified: Sat, 25 Oct 2025 02:02:31 GMT  
		Size: 738.9 KB (738885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2112d62c5a43f45c87ec4a6f27c36c2fd539d17e710af12efe7caaa00e1d0f9`  
		Last Modified: Sat, 25 Oct 2025 02:02:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3d1196770491fd3a90d7aa8b8374f28eb48ee47e4d5c48c84d392197614dfb`  
		Last Modified: Sat, 25 Oct 2025 02:02:31 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:3184d29d8ad0c72790246a71189d2e1fcf37cb94f752f29f67069088686e7728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74a75671343f7c90f2ee9029052377eedc2260a728a72289167761af27a5163`

```dockerfile
```

-	Layers:
	-	`sha256:e58711673c2ddcc53ad516eb97ef9252b13a98a4c396f0ec8cc6cf4814ac789a`  
		Last Modified: Sat, 25 Oct 2025 02:02:31 GMT  
		Size: 2.2 MB (2168529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e25a4a3503bfedc7a99b5b5ec2cf1aef371400473c7419eb078f7897c98830`  
		Last Modified: Sat, 25 Oct 2025 02:02:31 GMT  
		Size: 31.4 KB (31355 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.28`

**does not exist** (yet?)

## `composer:2`

```console
$ docker pull composer@sha256:02062f7719ec9433a9d4256cfba1c792db96dc9db60a4a92e48264c9e166b877
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
$ docker pull composer@sha256:53cf0b9d41bdaeecf5d8a77c68e29261f94882e967d938857bf71fd2e34b3f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78484055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff46f57437edc2ca4595a7a8d78662fa8244cb1d42613e67f18b9955fbb809ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:42:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:42:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:42:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:42:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:42:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:42:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:42:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:45:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:45:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:45:39 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:12:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:12:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:13:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:13:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:13:06 GMT
WORKDIR /app
# Fri, 08 May 2026 17:13:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:13:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b654640ed6c037ccdd1a25b2ae62a871ca0e1bf5f618ba969849b3b37e41af9`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 3.6 MB (3587616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40dc33330cb19d83115d1ae026d5d72ac32bd8f837cb79fd478c41aa3f53402`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e446c9444036d9a2b21592e04a74826d4671da791aae6d29163a697fac95881`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876fc8d6931dd52d5f7c4f3cc4c919d4d1322fe96fb1fd86cfcf7263dc5d76e`  
		Last Modified: Fri, 08 May 2026 16:45:48 GMT  
		Size: 14.4 MB (14417256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc09d7abe17a7b63967addd04a8285ed821149aaf96abb091020b22dfc68da0`  
		Last Modified: Fri, 08 May 2026 16:45:48 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7df31be2e3d6e83e0a06d7db20dd2ed43de7db70f1f45922f5c9f31516c2e0`  
		Last Modified: Fri, 08 May 2026 16:45:49 GMT  
		Size: 22.7 MB (22737297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82f0392f38de2fe157b97e8b3e797cc29975af6582edfbe95f905610501469d`  
		Last Modified: Fri, 08 May 2026 16:45:49 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d06dd6155739ed0fdc8c2b8f504f010792857d77998808592321d2f069d66`  
		Last Modified: Fri, 08 May 2026 16:45:49 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de747511d75dae581727a208d63cfb5dea9e1fc1abcecacab949f5b12312bfd`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 32.8 MB (32828492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269a50648c44005c9ce75745a80fe4eeba16e58075b02faaba9167dd62f94f6c`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f99f1add8b2e47ef4c93e3ef8db7e4ee1ff4f1ddec9668a7dc678dcae1a761`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 1.0 MB (1020970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54e359a2490a0cfb8cf0abd62ae66660b8bd29c46d0188821477f2793f5c779`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ec74ff474580cdfb131bba3665bbe4d30f27af1621c5765f8d129184953152`  
		Last Modified: Fri, 08 May 2026 17:13:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:b2e58d5d24fd4b4f29ea1a2909f182c866afb66581e952e0ab448cd5149b75ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753008aac0ec509459ba1b22c11c5f9fcb0c6b33ebf6b6a64460232c39a621d1`

```dockerfile
```

-	Layers:
	-	`sha256:746c6fb2ee8c17dcbc39cb6c9c0556a4a7e6ebad1896dc253fb9af81cd91d091`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 2.2 MB (2178657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0ae0ecb79efd72ef7fb43faccb0213b01a36a52ce2b4406756c7343383482d5`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:d8f4737995e55f7ee7537b83414ec0ddd381fb5c791509eca6170ef062676e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74944089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f509acb9370fd0b773b49d03f931dd6c664361af2afcea51e8c940bcb200416b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:37:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:37:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:37:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:37:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:37:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:37:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:37:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:37:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:40:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:40:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:40:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:40:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:40:33 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:16:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:16:45 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:17:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:17:09 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:17:09 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:17:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:17:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:17:09 GMT
WORKDIR /app
# Fri, 08 May 2026 17:17:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:17:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7063123be49bca3c998dd15fff3e6bf8b9037bf5d865219ec15d07a6a71f28dc`  
		Last Modified: Fri, 08 May 2026 16:40:39 GMT  
		Size: 3.5 MB (3543633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9796ddaa8b110e8c816d869c6bc6fdcd20ddfbdc2639897f4ea4e471eb76d9da`  
		Last Modified: Fri, 08 May 2026 16:40:38 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d042438a1f97af109fca616efe49b3235d7670aed6e54b7ac442be53baf34b9`  
		Last Modified: Fri, 08 May 2026 16:40:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f0c23d67858d02523a626ed972e24d143da08132aca3dc630277e8583931d8`  
		Last Modified: Fri, 08 May 2026 16:40:39 GMT  
		Size: 14.4 MB (14417274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a6444cc1ed13e98572aaf15c85e820b0ef5b704841ee7c0b1f67c6dbea66ef`  
		Last Modified: Fri, 08 May 2026 16:40:39 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4768db37e754a6d93cc79ac0a31a2ea1f70184527bcd68959c2ab652d02d1c9`  
		Last Modified: Fri, 08 May 2026 16:40:40 GMT  
		Size: 19.7 MB (19697128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f957f930966405369a831e03ca98d7ba85c480752557629a73a620ffe0d90c`  
		Last Modified: Fri, 08 May 2026 16:40:40 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1427b05be5ea97cb6c0e772bc00d53506512fe29ee3be3e18c369541c419e929`  
		Last Modified: Fri, 08 May 2026 16:40:40 GMT  
		Size: 23.2 KB (23197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dff3060bb020b0473474d4cb9fdd4803f80e08b9cb2f4ea223d8c47157e504`  
		Last Modified: Fri, 08 May 2026 17:17:17 GMT  
		Size: 32.7 MB (32665130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e491c1151f322528ac8da5713503882aa94b82e54abcfa9f69617d54bbeca985`  
		Last Modified: Fri, 08 May 2026 17:17:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc745588e596fde362f8c52dfa19dddd1cf9246f31b3ef3996b1ffc1ee43f6e`  
		Last Modified: Fri, 08 May 2026 17:17:17 GMT  
		Size: 1.0 MB (1021009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b05442fa40f67a80fbab357e3df30103fdc4a61691ed44913bf29bb1399c15`  
		Last Modified: Fri, 08 May 2026 17:17:17 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96154d4dfff66bad1ef878d986e6586487cdd509d291703f58ec0a18f6adc944`  
		Last Modified: Fri, 08 May 2026 17:17:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:cb8787c6d483c7ef737b88b7bb3a9b629d1d8bdb24365a44d4bb732c16447ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f95bafc6309e007d8e4f38c71a8327894ba5bd97f02638330ec37d277bbd1a`

```dockerfile
```

-	Layers:
	-	`sha256:da5b01da4e7fa686621bc3af7fac04b24513974542ccfa5799f5d68e2ceb1293`  
		Last Modified: Fri, 08 May 2026 17:17:16 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:cc5f9d74347953922012cb33c56431b1474184be21bbad0c50aca87942ba3319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71765815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff801114ce25400a1404f7598ff059edddcc5da4ac7b1e70f7d7c5a9cc377c21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:44:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:44:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:44:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:44:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:44:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:44:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:44:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:44:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:47:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:47:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:47:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:47:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:47:48 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:17:51 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:17:51 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:18:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:18:14 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:18:14 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:18:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:18:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:18:14 GMT
WORKDIR /app
# Fri, 08 May 2026 17:18:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:18:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad56310a751a6c77d98383a79b8b40902a76cd99bbf031203cb5e50009a7e21`  
		Last Modified: Fri, 08 May 2026 16:47:56 GMT  
		Size: 3.3 MB (3343518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c349e30aca535b108f20451e16f49be87dafc29ff25aa3cb46d835f1cfd79c`  
		Last Modified: Fri, 08 May 2026 16:47:55 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a86d13cd318b8c71ed9e3d842909aef3bd247db089054a734caf702a4494e7a`  
		Last Modified: Fri, 08 May 2026 16:47:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e0ebb3537ef57ac21c0136ab9d86c6cf673686a1758c7dccf2e0507677c4ca`  
		Last Modified: Fri, 08 May 2026 16:47:56 GMT  
		Size: 14.4 MB (14417282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630cde6decb0613f633233436ae8d90ee7ac540ee35fdcc79a02830b44cde2d9`  
		Last Modified: Fri, 08 May 2026 16:47:57 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe23a1ee2edd4df1b0b2cb1b55f49f366672aee55411cf4f3a2482a5ef63859e`  
		Last Modified: Fri, 08 May 2026 16:47:57 GMT  
		Size: 18.6 MB (18586006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a83f016507951154ecee1da8a8a702c4913bcf89a5352f214180fd893ee7e`  
		Last Modified: Fri, 08 May 2026 16:47:57 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aacec4ecdb1ac54d3f59f543d94f4d982681fee3b6017409510c7db02a56cd3`  
		Last Modified: Fri, 08 May 2026 16:47:58 GMT  
		Size: 23.2 KB (23207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1609486e3fbc531402cdafca7c4d66bbe99aec7a16c658fba42c842dfffc4d15`  
		Last Modified: Fri, 08 May 2026 17:18:24 GMT  
		Size: 31.1 MB (31096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b2f2f550ad5a55cc50fd37619e858e9520c81e24b5ab12d8740ed3f9774744`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de963be19db260c4d1ecaa29abea921afae50d8596803e760b6cdbddcf47fa4f`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 1.0 MB (1011442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2626607b68a635ac9532e2b9a5a9b58eb8e1b1831ae92813511c3ac726b744`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1848b8c9ab7b90543a2747f0793762ca2e39358956a467811dcce1b1538039d5`  
		Last Modified: Fri, 08 May 2026 17:18:24 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:463c12dfc3c1783ddd7df87a857010aedb0227ff78ad920ee0e5bb3bd04b274e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434eab32ce67c1bb0264ed8065a6f1baf42a44b342102b2028e449774550a13f`

```dockerfile
```

-	Layers:
	-	`sha256:0b0e7f2b324a71b90066d60e3576a4be7bc93787f1cf62c76dc1fe9c6fc61023`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 2.2 MB (2178328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283190992301d9998ab0ef9162d01dc8b93c6cbe1171e49b615dd1351af7f233`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 30.8 KB (30773 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:16fc896e904662ba6b82db1a156864c97a42083b456cefca413e44d2d5d48d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78144594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76ff5069c100e0c2bab675679be74b6c604790ea8e3fb69eb52f9d1c83a220a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:41:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:41:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:41:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:41:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:41:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:41:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:41:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:45:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:45:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:45:21 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:13:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:13:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:13:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:13:28 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:13:28 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:13:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:13:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:13:28 GMT
WORKDIR /app
# Fri, 08 May 2026 17:13:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:13:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fccd1681e76186ece96de411a47fcf0a2ea8b3a42bea388612e2ad17682df83`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 3.6 MB (3596160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b123c2ad03bae81cac30c7ce6c83449c58af169a38e2769582cf57b4bd5fec2`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19e0156c658a50f56baef5e593490b5422a02e961c8c72379e3ecfec4bbe8f`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882cd6a9aa6b8d82c2bd2475162ef7321121ed51bd6227365f4118b9ee016d51`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 14.4 MB (14417265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dd7533a619b5ba3534670946cde6191553e5eeba6399d44b5d1b0902176a5a`  
		Last Modified: Fri, 08 May 2026 16:45:30 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e4c9ba7c6c87f5254867ebaa82b91c46bfb66fc18f43dee2582724cc72d33c`  
		Last Modified: Fri, 08 May 2026 16:45:31 GMT  
		Size: 21.9 MB (21912560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2023c08468a22348b2f976f9c71b54d7afc2b0d8f0c5abba36494ff090f157`  
		Last Modified: Fri, 08 May 2026 16:45:31 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea47019ff974219dca03451a8728ab2d8389f57d08ae0db784f0a0b68f3d5739`  
		Last Modified: Fri, 08 May 2026 16:45:31 GMT  
		Size: 23.2 KB (23210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc79e203ef84c43f54c47df5625b30a4bfaadb6fd2098d4645b6ade1b6cae86f`  
		Last Modified: Fri, 08 May 2026 17:13:39 GMT  
		Size: 33.0 MB (32970871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e04d47530b717eb87b2d3cb3ad54c6275aaec2527b39d824839db9a79dc66e`  
		Last Modified: Fri, 08 May 2026 17:13:37 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d044ee4a5c5e3f1126f849352857799eaffbc5be36bf6c1201083713111971`  
		Last Modified: Fri, 08 May 2026 17:13:38 GMT  
		Size: 1.0 MB (1019808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe82d1d4338e8583db891c7f71bdfd70b97c6e2ecf06e3e87679821668892af`  
		Last Modified: Fri, 08 May 2026 17:13:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8dd62b0c5bf51f6d305cc43debbaeb5ff5403e72d5b8533a80aa562d7c33b3`  
		Last Modified: Fri, 08 May 2026 17:13:39 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:a3b00a48da16f5c9b1bc08f29f178f82170ca2567b3caadc5db6e1abf5668dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ae42e0cdb89975c6c9f1c106c094a38e5f1b52ad00abc05b83adbde915ec5c`

```dockerfile
```

-	Layers:
	-	`sha256:353d3c7c3f15f78cb51d5c3773b552c563d10916326a051b5d4503c11b4f6623`  
		Last Modified: Fri, 08 May 2026 17:13:37 GMT  
		Size: 2.2 MB (2178158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38cd920e5244111e906a24374c25aaa430b0df481f42512fa6593471e763c19f`  
		Last Modified: Fri, 08 May 2026 17:13:37 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:c7684d3fed68105ad4f06bc286b2bcfb932ccfd4465899af81ecc7441e59088f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79333375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b598f10979ecabbbecd2fbeca22124ace9a9ace399cda7e378aae0af918c2c33`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:45:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:45:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:45:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:45:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:45:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:45:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:45:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:49:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:49:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:49:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:49:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:49:23 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:12:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:12:50 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:13:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:13:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:13:06 GMT
WORKDIR /app
# Fri, 08 May 2026 17:13:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:13:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5f818fb7c09d275f57b0be232e3327c598854c2cd8c1af2e5536f47c030109`  
		Last Modified: Fri, 08 May 2026 16:49:31 GMT  
		Size: 3.6 MB (3625695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bde2dbfa2d2a3c95dc2eb8f7e57ce0c5861a36e95ff913cab891df185c56779`  
		Last Modified: Fri, 08 May 2026 16:49:31 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f7ce7672df1bccaf696725c7cf018abd4fcce22df9ddd66674d1d181d1fb1`  
		Last Modified: Fri, 08 May 2026 16:49:31 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c78a34ca66f37347555dd11601a37b28fb5dc7b9164650aef7bbcdc265237d`  
		Last Modified: Fri, 08 May 2026 16:49:32 GMT  
		Size: 14.4 MB (14417249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d49058f5e508fbedf7c1761ed74c3488a1b66aa1c53245df6f5c202bd01e68`  
		Last Modified: Fri, 08 May 2026 16:49:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0d59880de31c08bb1c82cab93a0766a728df6e6f0b2f8b018340e1f90e839e`  
		Last Modified: Fri, 08 May 2026 16:49:33 GMT  
		Size: 23.2 MB (23185462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b3fdeafdda5d52745fb055ae2c3da55119fc9058b9c9ac2880f1358ed8790`  
		Last Modified: Fri, 08 May 2026 16:49:33 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179dc4512664e42fc76b4cbd3cb62d559b6534581642050bc82876d631c7be5c`  
		Last Modified: Fri, 08 May 2026 16:49:33 GMT  
		Size: 23.4 KB (23378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7d15ac4f12ca126a295236e4d7d0544b30ba61b18f042c1b2b3c1c5f5c1894`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 33.4 MB (33353595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c445445a600188721e5cd81fe3fc287d738e58cffc77ebe8e25ba5cce6155f86`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88601221afe1744e48943b5c1fe721cb5ac894586745c4a3780ac3f588ad7a`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 1.0 MB (1032700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b04c9c8d07dca7ff58a463258a23075b5124f8dc39586c413c774fdd43ca7`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ec74ff474580cdfb131bba3665bbe4d30f27af1621c5765f8d129184953152`  
		Last Modified: Fri, 08 May 2026 17:13:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:7c6caa805b56d2cf26b35c94546e7ef1d5a5dec144b18729498db946dbcd9c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc0ec7f96942e271b7d7631c3b46d6dbb800d5d898b2c6fe6ebd881faddd386`

```dockerfile
```

-	Layers:
	-	`sha256:030ced0a8be99eea3c9b9fd78f0393f312863b389dc7a53d3d17f94c8431c692`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 2.2 MB (2178442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b33345f3941243a749471efabde80bc10e90cfaea692daa3fe8531fae4a866`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 30.6 KB (30631 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:3a37fd68a6042cb82fd1c521b31aef4ca1d26d867c7b9c13d7401784777eeff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80378812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765290965180ecbca7e191081d78c709ff334540dff4504dc828ba8496da13ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:20:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:20:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.5.6
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 19:47:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 19:47:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:52:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:52:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:52:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:52:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:52:48 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 22:31:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 22:31:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 22:32:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 22:32:37 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 22:32:37 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 22:32:37 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 22:32:37 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 22:32:37 GMT
WORKDIR /app
# Fri, 08 May 2026 22:32:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 22:32:37 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59216db1edcf64b90905df63416f821bfacdba590544dcdb3c340ea538567c`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 3.8 MB (3767095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dbb332183b4f53eb48b10e61f11a67b23c5647a6901cf35be6037e209a0f51`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd758015c67cd7fae70202df89f7e42a01ff424cadf0cd92070805333b28821`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5702960144fbb228318e4c40ca2e9c98158a8c7b9f71390320236bda898ca95`  
		Last Modified: Fri, 08 May 2026 19:53:03 GMT  
		Size: 14.4 MB (14417280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358ab27e77a70ddec9b84d07b8f7d4afdddd40d4273150e0f53f745558ec45e`  
		Last Modified: Fri, 08 May 2026 19:53:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d790c857f23d764dbb55c79e470cb965a5e1400d248610a1b021e5da4b086f`  
		Last Modified: Fri, 08 May 2026 19:53:04 GMT  
		Size: 23.1 MB (23128501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d767ccb38fac4728b8964553352783881ac8482bff309e0e7a49475c1c68d10`  
		Last Modified: Fri, 08 May 2026 19:53:03 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792fe8cb0c39c5be7986dfbc108e720fbe9f5b205a09ea9e786278ca7d2d3b11`  
		Last Modified: Fri, 08 May 2026 19:53:04 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2594f5b2cc2f273332e529c87042778906a76cf847c1bbbfb0afb3a53554b1b5`  
		Last Modified: Fri, 08 May 2026 22:32:56 GMT  
		Size: 34.2 MB (34180303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ac582f80c6a79ddb5212f9a4b1ef780331e87889d7c30fee1b86fc32cdbbc0`  
		Last Modified: Fri, 08 May 2026 22:32:54 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72388f9529399090e5800a46557ae5093e9aeacd27281f855788291ddb37069e`  
		Last Modified: Fri, 08 May 2026 22:32:55 GMT  
		Size: 1.0 MB (1026571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25f9d92287139c4c82a3bac211848cb7a07d6f2aa71ce60801c76d1ef214beb`  
		Last Modified: Fri, 08 May 2026 22:32:54 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a103edbe4df44409e697cd61db384f5cdfb624730e03035597985b13bda6a050`  
		Last Modified: Fri, 08 May 2026 22:32:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:a2d34893c3a2c5fb4746092fe95ba67b9c6f72589696f5b80baa03608007418a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7e76daebcc65909e955a1b3934377e39f50689ddeeae82674e6453d372226d`

```dockerfile
```

-	Layers:
	-	`sha256:10d3d3b85cb1245b350e666620671874ef164948262ea04701a0e063108eab93`  
		Last Modified: Fri, 08 May 2026 22:32:54 GMT  
		Size: 2.2 MB (2178515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01f2d29228b635dc3ef228ece64bda988eaad8b7fa7fcca684415e671fea1d47`  
		Last Modified: Fri, 08 May 2026 22:32:54 GMT  
		Size: 30.7 KB (30715 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:201fb227742eda84c3920f1565e36deec0155cc20c27503627daad12fcc76545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75255480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16f0073e3ec90e47a472eea73f9e48783013f33733be9a1a6b00ca52915ef16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 16 Apr 2026 00:30:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Apr 2026 00:30:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_VERSION=8.5.6
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 21:51:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 21:51:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:52:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 22:52:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:52:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 22:52:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 22:52:16 GMT
CMD ["php" "-a"]
# Mon, 11 May 2026 00:57:44 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 11 May 2026 00:57:45 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 11 May 2026 01:01:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 11 May 2026 01:01:09 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 11 May 2026 01:01:09 GMT
ENV COMPOSER_VERSION=2.9.7
# Mon, 11 May 2026 01:01:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 11 May 2026 01:01:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 11 May 2026 01:01:09 GMT
WORKDIR /app
# Mon, 11 May 2026 01:01:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 01:01:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78828518b8b5af0bc74ba3bd169a5c835b32f2a1452a7cd03ad8117a0128165b`  
		Last Modified: Thu, 16 Apr 2026 01:32:16 GMT  
		Size: 3.7 MB (3734242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1c9b4ddefe159b602dd6cdf3bcfff1bf48c922a0f1047bb5402dc2c6c988b`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2a62067bd9660d4987f0df8c18a9ac2818a33d0443ac9c5c806eb7925b9957`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b300791544e0c87f44b461c514787bf7d38ce6f5ad1d34bad34bc1c4782d3f`  
		Last Modified: Fri, 08 May 2026 22:53:24 GMT  
		Size: 14.4 MB (14417294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a331978dcb7855b965e50fa41230cb7f963d49113c956b0e49057d02df423466`  
		Last Modified: Fri, 08 May 2026 22:53:20 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcc286c95072e0d8d8b60f5e888859a51d02c496556840b68e28764a6173ecd`  
		Last Modified: Fri, 08 May 2026 22:53:25 GMT  
		Size: 21.2 MB (21171065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9799a7293faac913a8c2e0ba1a7628be32b2a5ea0e7dd2d76b844e7dfce47ad`  
		Last Modified: Fri, 08 May 2026 22:53:19 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb29c91c88ab86cb8131cb830f2bb49a8ffa2614cedc1c31b69e2c77a975695d`  
		Last Modified: Fri, 08 May 2026 22:53:21 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c65261e37a7d3f9ee21b1c9a9bd5ea90cb040884d3cbfb68f7150999f038c4`  
		Last Modified: Mon, 11 May 2026 01:02:48 GMT  
		Size: 31.3 MB (31299460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4361abd2c1daef5f4b6053d114136340df2419298fa403e48ae9996cced2b79`  
		Last Modified: Mon, 11 May 2026 01:02:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4e9a5a183a412aeab22b9bd7a35dbe3ddf399a681f5635e496b9c528121cc1`  
		Last Modified: Mon, 11 May 2026 01:02:44 GMT  
		Size: 1.0 MB (1017615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7681fc7957bbd94bf344f9bd1d7d20f834516ef48691c0bdd749d92ec99fdf2`  
		Last Modified: Mon, 11 May 2026 01:02:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1a9a59e18e5374c9718c827255af5499b066d9dfa2132339e54344c31bf500`  
		Last Modified: Mon, 11 May 2026 01:01:23 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:a328837c6987cad2823792a27dcb579f1e02ff98360d0fdeab5bddf78b5dc12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9b86e0d7a6aeb07175f26c5e648750546e24b473d1dbd38b2478b319c806d2`

```dockerfile
```

-	Layers:
	-	`sha256:1c6aabf396b9034e4e8398ae6b930e4fed5f617e38493e2d4a2c36ce315be2ef`  
		Last Modified: Mon, 11 May 2026 01:02:44 GMT  
		Size: 2.2 MB (2177456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a51e1cba29e30595a491fb536a64e76d162dab7ff375b5848e32937d4358e2`  
		Last Modified: Mon, 11 May 2026 01:02:43 GMT  
		Size: 30.7 KB (30715 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:99863cc662e4b5958234f74730006b98c072da8266d99f0688188349ebee9e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76696548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc203f97b83b8715f9a920330a5325d8ed4a3edcf20ded5cb7f3adfe1a85676`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:41:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 May 2026 23:41:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 05 May 2026 23:41:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 05 May 2026 23:41:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 May 2026 23:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 May 2026 23:41:50 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_VERSION=8.5.6
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:51:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:57:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:57:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:57:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:57:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:57:50 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:14:56 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:14:56 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:15:21 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:15:21 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:15:21 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:15:21 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:15:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:15:21 GMT
WORKDIR /app
# Fri, 08 May 2026 17:15:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:15:21 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e5b23cd7e08583775ca52654782b3eb898be0895811ff074d0b60e2bdabdca`  
		Last Modified: Tue, 05 May 2026 23:50:39 GMT  
		Size: 3.8 MB (3787468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f70f6e1cd967f35b17107285a2dc3920f6cf2d49ba0521083fa3949317113`  
		Last Modified: Tue, 05 May 2026 23:50:38 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cc64825ed6643492e29ef55789e3eb5ed14b413945792b7bc86db5b7c4e70c`  
		Last Modified: Tue, 05 May 2026 23:50:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70b8b3c23d4b9513ddce760870ee58e711276bb86bdaa74045eafcaf6ae2dc`  
		Last Modified: Fri, 08 May 2026 16:58:06 GMT  
		Size: 14.4 MB (14417277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a38b097c90d256a49ef7bdca140fa8da69c874c923a1dfdd3513846d669f87`  
		Last Modified: Fri, 08 May 2026 16:58:06 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31050156e2ccbc94f9c20b8bcc6638051971128034fb34ad2fdcd18496bf5ec`  
		Last Modified: Fri, 08 May 2026 16:58:07 GMT  
		Size: 21.6 MB (21596857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac685bed84db73eb81d30fa0fa48e67ef3dc625228c72a0ebbc4c8799811eb2`  
		Last Modified: Fri, 08 May 2026 16:58:06 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3171cf62ee41e70bb40f0a98476a7b9f2b6ae9b42d0846873babe98b876b5b60`  
		Last Modified: Fri, 08 May 2026 16:58:07 GMT  
		Size: 23.2 KB (23211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a5b3a5457c384d521a0679d9ad0cfe2efd36175f48ece0b87ed81ff481849`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 32.1 MB (32116524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d567a1a4fa1f8f4985421d4acd4135b3ad52ef380c3f5b44f0291c750cc47c`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82f007fb94228f94c86d027e3598ca58aa08111593d3ca64f403e622325a629`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 1.0 MB (1023820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a42c97b56e0830eede2e46fb214d069afd35578b2e1aee6d27d8af45f256707`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7726d52575774721ccc577d8e854ec56153c76f536b5ef5e8556ab5cbb039ee`  
		Last Modified: Fri, 08 May 2026 17:15:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:40436a63296c0d39fd5eb482c639272e706d6913e9f9203bee69df14cc3a4c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e856da7070e174ec6524a5c1bb2e68da3bac933ad4ae559cc7b63fdbb0b523c1`

```dockerfile
```

-	Layers:
	-	`sha256:97ee1766c209a040ea17e116ebf93e681b06c3c47dcb4f0063bbe36c36e6d312`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 2.2 MB (2177238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4e44f195d88ce08505dfde243f4efde4685113a38414e45fde22d52cd50add6`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:c3839969c321299911640b84a569cca993c633e8d8b23df8a5c1138a1d43553c
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
$ docker pull composer@sha256:6decc36fff118076baceb12b795f24cb32deb1ad6ed160edaa310bbfec9eb53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78288396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf64b630a4f1cc80d78f0459b842313b393ec1c54542d884cae41f06ef810652`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:42:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:42:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:42:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:42:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:42:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:42:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:42:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:45:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:45:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:45:39 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:12:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:12:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:13:12 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:13:12 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:13:12 GMT
ENV COMPOSER_VERSION=2.2.27
# Fri, 08 May 2026 17:13:12 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:13:12 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:13:12 GMT
WORKDIR /app
# Fri, 08 May 2026 17:13:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:13:12 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b654640ed6c037ccdd1a25b2ae62a871ca0e1bf5f618ba969849b3b37e41af9`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 3.6 MB (3587616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40dc33330cb19d83115d1ae026d5d72ac32bd8f837cb79fd478c41aa3f53402`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e446c9444036d9a2b21592e04a74826d4671da791aae6d29163a697fac95881`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876fc8d6931dd52d5f7c4f3cc4c919d4d1322fe96fb1fd86cfcf7263dc5d76e`  
		Last Modified: Fri, 08 May 2026 16:45:48 GMT  
		Size: 14.4 MB (14417256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc09d7abe17a7b63967addd04a8285ed821149aaf96abb091020b22dfc68da0`  
		Last Modified: Fri, 08 May 2026 16:45:48 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7df31be2e3d6e83e0a06d7db20dd2ed43de7db70f1f45922f5c9f31516c2e0`  
		Last Modified: Fri, 08 May 2026 16:45:49 GMT  
		Size: 22.7 MB (22737297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82f0392f38de2fe157b97e8b3e797cc29975af6582edfbe95f905610501469d`  
		Last Modified: Fri, 08 May 2026 16:45:49 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d06dd6155739ed0fdc8c2b8f504f010792857d77998808592321d2f069d66`  
		Last Modified: Fri, 08 May 2026 16:45:49 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a629abc234b3d6950ccc733c2587e7376556facc10a96613a17bf69291f8b5`  
		Last Modified: Fri, 08 May 2026 17:13:22 GMT  
		Size: 32.8 MB (32828492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cab580b38d5d5b4c4e3119e3f6602b86baf6401a8ca9868f0bb8e856b6c287`  
		Last Modified: Fri, 08 May 2026 17:13:21 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9cce196fe019217fb2472b245ea8406a9a7cc873b8b32603cce7c8284aa4b3`  
		Last Modified: Fri, 08 May 2026 17:13:22 GMT  
		Size: 825.3 KB (825311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc079b62f70d33d148d98130522c1b1c598276e7f2378f02ed51f5d309c339b2`  
		Last Modified: Fri, 08 May 2026 17:13:21 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cf58e79618b862c3a4fb5ecb4ac842a76ca554ef4ba1d479a645cdd36d6238`  
		Last Modified: Fri, 08 May 2026 17:13:23 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:2723afc59a7f95d478f2574d21c5fcc0c48513e35492721c5a898d690473a1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0dffd7d32f3f78b973a33ded9820455e6a6c92a2a703fada74166c100dde33`

```dockerfile
```

-	Layers:
	-	`sha256:027caf20808727dbef1bb18875cc61396774ae4f876e87f0dabad0ea6f4a9a0f`  
		Last Modified: Fri, 08 May 2026 17:13:21 GMT  
		Size: 2.2 MB (2178067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:035b18106a565b62278d23d232e0061fc90b53710cb1c4e8856a90f628f93390`  
		Last Modified: Fri, 08 May 2026 17:13:21 GMT  
		Size: 30.1 KB (30064 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:8c216fa38ec641e480582a38128440f89c32896f2bbd480671ffa4e44858b2bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74748594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4097e23390f97b27649adde8c730da8e2861f9006ca1e6cb67949f0bf43206a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:37:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:37:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:37:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:37:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:37:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:37:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:37:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:37:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:40:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:40:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:40:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:40:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:40:33 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:17:01 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:17:01 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:17:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:17:24 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:17:24 GMT
ENV COMPOSER_VERSION=2.2.27
# Fri, 08 May 2026 17:17:24 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:17:24 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:17:24 GMT
WORKDIR /app
# Fri, 08 May 2026 17:17:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:17:24 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7063123be49bca3c998dd15fff3e6bf8b9037bf5d865219ec15d07a6a71f28dc`  
		Last Modified: Fri, 08 May 2026 16:40:39 GMT  
		Size: 3.5 MB (3543633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9796ddaa8b110e8c816d869c6bc6fdcd20ddfbdc2639897f4ea4e471eb76d9da`  
		Last Modified: Fri, 08 May 2026 16:40:38 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d042438a1f97af109fca616efe49b3235d7670aed6e54b7ac442be53baf34b9`  
		Last Modified: Fri, 08 May 2026 16:40:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f0c23d67858d02523a626ed972e24d143da08132aca3dc630277e8583931d8`  
		Last Modified: Fri, 08 May 2026 16:40:39 GMT  
		Size: 14.4 MB (14417274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a6444cc1ed13e98572aaf15c85e820b0ef5b704841ee7c0b1f67c6dbea66ef`  
		Last Modified: Fri, 08 May 2026 16:40:39 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4768db37e754a6d93cc79ac0a31a2ea1f70184527bcd68959c2ab652d02d1c9`  
		Last Modified: Fri, 08 May 2026 16:40:40 GMT  
		Size: 19.7 MB (19697128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f957f930966405369a831e03ca98d7ba85c480752557629a73a620ffe0d90c`  
		Last Modified: Fri, 08 May 2026 16:40:40 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1427b05be5ea97cb6c0e772bc00d53506512fe29ee3be3e18c369541c419e929`  
		Last Modified: Fri, 08 May 2026 16:40:40 GMT  
		Size: 23.2 KB (23197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ead5fe7ba02671cd215026186d1dea3ff0c1e06ad81e0ddcf4a6325899eb09`  
		Last Modified: Fri, 08 May 2026 17:17:32 GMT  
		Size: 32.7 MB (32665961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c73db4e04737e7aec59f503719e8e70a84b0a53d2781f856b5757afc603331`  
		Last Modified: Fri, 08 May 2026 17:17:31 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f8128ddc0363af275cb22a1ec095ecab62a8960f58fd32e80eb32022ed245d`  
		Last Modified: Fri, 08 May 2026 17:17:31 GMT  
		Size: 824.7 KB (824678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d165f51fc5e1f6e08a3b4c238e6268d8afb307a4db187291f663f50211a4b0`  
		Last Modified: Fri, 08 May 2026 17:17:31 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bbcc48efbd8662838724189e766146396c15b8383a034e7d185f92e594511d`  
		Last Modified: Fri, 08 May 2026 17:17:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:8fe124a5f74b2b8db834d0a1c5ce316c3a48046572c26199baa7a3ffafbd9a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 KB (29939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43950f5e4949d393c34f568659d7a1927b9af6e48bed42f34ead1f3728296d2f`

```dockerfile
```

-	Layers:
	-	`sha256:c8f6b9dd3fb5c0baca4916825531406fda6ce977ae6f9646207c7ed5e04b4004`  
		Last Modified: Fri, 08 May 2026 17:17:31 GMT  
		Size: 29.9 KB (29939 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:f6f68b331185217f1a8e3dc09d3bc2fcd576abbe58e88944edffc5ee6304833e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71569967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b905fdfaff09fe87828eca8edec07652650b5bb8d23ecef4610d4d0999a433cb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:44:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:44:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:44:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:44:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:44:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:44:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:44:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:44:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:47:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:47:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:47:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:47:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:47:48 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:17:51 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:17:51 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:18:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:18:14 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:18:14 GMT
ENV COMPOSER_VERSION=2.2.27
# Fri, 08 May 2026 17:18:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:18:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:18:14 GMT
WORKDIR /app
# Fri, 08 May 2026 17:18:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:18:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad56310a751a6c77d98383a79b8b40902a76cd99bbf031203cb5e50009a7e21`  
		Last Modified: Fri, 08 May 2026 16:47:56 GMT  
		Size: 3.3 MB (3343518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c349e30aca535b108f20451e16f49be87dafc29ff25aa3cb46d835f1cfd79c`  
		Last Modified: Fri, 08 May 2026 16:47:55 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a86d13cd318b8c71ed9e3d842909aef3bd247db089054a734caf702a4494e7a`  
		Last Modified: Fri, 08 May 2026 16:47:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e0ebb3537ef57ac21c0136ab9d86c6cf673686a1758c7dccf2e0507677c4ca`  
		Last Modified: Fri, 08 May 2026 16:47:56 GMT  
		Size: 14.4 MB (14417282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630cde6decb0613f633233436ae8d90ee7ac540ee35fdcc79a02830b44cde2d9`  
		Last Modified: Fri, 08 May 2026 16:47:57 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe23a1ee2edd4df1b0b2cb1b55f49f366672aee55411cf4f3a2482a5ef63859e`  
		Last Modified: Fri, 08 May 2026 16:47:57 GMT  
		Size: 18.6 MB (18586006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a83f016507951154ecee1da8a8a702c4913bcf89a5352f214180fd893ee7e`  
		Last Modified: Fri, 08 May 2026 16:47:57 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aacec4ecdb1ac54d3f59f543d94f4d982681fee3b6017409510c7db02a56cd3`  
		Last Modified: Fri, 08 May 2026 16:47:58 GMT  
		Size: 23.2 KB (23207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150e70637032a2cd1b01d83d5ef773f8c9f400820cafcaff2c7730605507e6be`  
		Last Modified: Fri, 08 May 2026 17:18:24 GMT  
		Size: 31.1 MB (31096417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8107873784341246cfe2438b8983104cf9c02d4ccf5e93a8a979e0a5effb5832`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0dc65918f7cd47ae719811467da139e213ac9260bbd1bc32e72f9241080fd5`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 815.6 KB (815562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61097016e4e31ef7057f7d99a03b6de20c83bfb51468c54edf5f7c2c627c962f`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1848b8c9ab7b90543a2747f0793762ca2e39358956a467811dcce1b1538039d5`  
		Last Modified: Fri, 08 May 2026 17:18:24 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:1456752f0aa90aa7dc59eaf1d99e3a8fc0b81388c3d419402aff1022d300d0c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60bac3ff5ed44ecfa3cf5ae2ed6ab98da02aab4b94635bacc82c2d40d9cc669`

```dockerfile
```

-	Layers:
	-	`sha256:afcdbd609043d8c8969d247826aa58213ab7eec2547a7cc54e688c0e88b6f690`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 2.2 MB (2177722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d3be86486cfd4a51b91db5299730766250e749e379731dc17879b134b6437b`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 30.2 KB (30152 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:be1b49885ba5a0209b50a45a0f02822d35d69ba5623f7bda126ad13043e141ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77949091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508163614da2bdfaf0e6b0651326c9834624945cea19902493124b6175d878ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:41:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:41:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:41:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:41:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:41:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:41:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:41:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:45:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:45:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:45:21 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:13:11 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:13:11 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:13:30 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:13:30 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:13:30 GMT
ENV COMPOSER_VERSION=2.2.27
# Fri, 08 May 2026 17:13:30 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:13:30 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:13:31 GMT
WORKDIR /app
# Fri, 08 May 2026 17:13:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:13:31 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fccd1681e76186ece96de411a47fcf0a2ea8b3a42bea388612e2ad17682df83`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 3.6 MB (3596160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b123c2ad03bae81cac30c7ce6c83449c58af169a38e2769582cf57b4bd5fec2`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19e0156c658a50f56baef5e593490b5422a02e961c8c72379e3ecfec4bbe8f`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882cd6a9aa6b8d82c2bd2475162ef7321121ed51bd6227365f4118b9ee016d51`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 14.4 MB (14417265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dd7533a619b5ba3534670946cde6191553e5eeba6399d44b5d1b0902176a5a`  
		Last Modified: Fri, 08 May 2026 16:45:30 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e4c9ba7c6c87f5254867ebaa82b91c46bfb66fc18f43dee2582724cc72d33c`  
		Last Modified: Fri, 08 May 2026 16:45:31 GMT  
		Size: 21.9 MB (21912560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2023c08468a22348b2f976f9c71b54d7afc2b0d8f0c5abba36494ff090f157`  
		Last Modified: Fri, 08 May 2026 16:45:31 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea47019ff974219dca03451a8728ab2d8389f57d08ae0db784f0a0b68f3d5739`  
		Last Modified: Fri, 08 May 2026 16:45:31 GMT  
		Size: 23.2 KB (23210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0085dd809931185cb9e8c3c550c5d06dfc4b0a5f17fb83c791de1477da756132`  
		Last Modified: Fri, 08 May 2026 17:13:41 GMT  
		Size: 33.0 MB (32971262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbf84dd84017de934a49ecdade94191a84c6296ffca1e3558dc1955ead4f923`  
		Last Modified: Fri, 08 May 2026 17:13:40 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e496f82545c68f6e791523a2454e4c44d60ba41fdbdf3298b8a946f654c4ec6c`  
		Last Modified: Fri, 08 May 2026 17:13:40 GMT  
		Size: 823.9 KB (823914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa6803c7e9b037b5475210b9e93c931d986582c3dd35c3ab65518476cc1eeb6`  
		Last Modified: Fri, 08 May 2026 17:13:40 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31713207265a9f4dd7893cfaee0b7f15413e54b5e8ed785b766051ec42bff553`  
		Last Modified: Fri, 08 May 2026 17:13:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:f8e178de6aca8ff5fcb08e4f3f35e3794d1307bd8a97d07bc4f9f5f9bfc9ad33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638ae8fc678d9e804a35ad272402deaa50f8c4f76512bbb44749dff1b719377d`

```dockerfile
```

-	Layers:
	-	`sha256:36777f6b466b3f433e03ed26cf8ed598a2c1679c5ec144787e081418798880e9`  
		Last Modified: Fri, 08 May 2026 17:13:40 GMT  
		Size: 2.2 MB (2177544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fe640aa3b13c554d89ecefabb65d00882809557a86bd77e570d20f81db5d74d`  
		Last Modified: Fri, 08 May 2026 17:13:40 GMT  
		Size: 30.2 KB (30174 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:0597eb521dff22b9ededbd01f07bb03eac3f75f0d2da70b724e55267c0f438d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79139349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449fb865e187d4bbb46de260cff68a1c0c9e1e2520782faf75f14afb73baf9e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:45:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:45:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:45:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:45:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:45:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:45:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:45:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:49:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:49:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:49:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:49:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:49:23 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:12:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:12:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:13:07 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:13:07 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:13:07 GMT
ENV COMPOSER_VERSION=2.2.27
# Fri, 08 May 2026 17:13:07 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:13:07 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:13:07 GMT
WORKDIR /app
# Fri, 08 May 2026 17:13:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:13:07 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5f818fb7c09d275f57b0be232e3327c598854c2cd8c1af2e5536f47c030109`  
		Last Modified: Fri, 08 May 2026 16:49:31 GMT  
		Size: 3.6 MB (3625695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bde2dbfa2d2a3c95dc2eb8f7e57ce0c5861a36e95ff913cab891df185c56779`  
		Last Modified: Fri, 08 May 2026 16:49:31 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f7ce7672df1bccaf696725c7cf018abd4fcce22df9ddd66674d1d181d1fb1`  
		Last Modified: Fri, 08 May 2026 16:49:31 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c78a34ca66f37347555dd11601a37b28fb5dc7b9164650aef7bbcdc265237d`  
		Last Modified: Fri, 08 May 2026 16:49:32 GMT  
		Size: 14.4 MB (14417249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d49058f5e508fbedf7c1761ed74c3488a1b66aa1c53245df6f5c202bd01e68`  
		Last Modified: Fri, 08 May 2026 16:49:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0d59880de31c08bb1c82cab93a0766a728df6e6f0b2f8b018340e1f90e839e`  
		Last Modified: Fri, 08 May 2026 16:49:33 GMT  
		Size: 23.2 MB (23185462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b3fdeafdda5d52745fb055ae2c3da55119fc9058b9c9ac2880f1358ed8790`  
		Last Modified: Fri, 08 May 2026 16:49:33 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179dc4512664e42fc76b4cbd3cb62d559b6534581642050bc82876d631c7be5c`  
		Last Modified: Fri, 08 May 2026 16:49:33 GMT  
		Size: 23.4 KB (23378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb8a138d023d34f8851756b64731938872bbdbcc0555fc4acf1c9ed2a51b5ff`  
		Last Modified: Fri, 08 May 2026 17:13:18 GMT  
		Size: 33.4 MB (33353624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c280ed2cb94eb7f504064fb8d1a5683e4b919c6b94c13b96cc2e1b95afe6147f`  
		Last Modified: Fri, 08 May 2026 17:13:17 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2227447cb0edd5e189f7ece2afac0822801cba7106f28f2ac4df3c2dc510ccf`  
		Last Modified: Fri, 08 May 2026 17:13:17 GMT  
		Size: 838.6 KB (838646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54e359a2490a0cfb8cf0abd62ae66660b8bd29c46d0188821477f2793f5c779`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b60fa7ec9e265070663fcebe1949c1d6fde53bcf01831964a734c8638828d2`  
		Last Modified: Fri, 08 May 2026 17:13:18 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:70497d414c4bb1fc578616d5489ccf780abf12df600198b67f10ecde36fff947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d2a961c48adaa3366cc39f1f26c30e161a6ac04fcdd72960a87261bec82bd8`

```dockerfile
```

-	Layers:
	-	`sha256:e2a2d7e8facf5663541f9391ebc0f7678c81131927114de9d10f0db28239ef32`  
		Last Modified: Fri, 08 May 2026 17:13:17 GMT  
		Size: 2.2 MB (2177862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e613c2afc3bc2822349f7a77bba6df2a4cd4f26fcab63403899a79c36fa42e`  
		Last Modified: Fri, 08 May 2026 17:13:17 GMT  
		Size: 30.0 KB (30038 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:c35a90cfa8dae43f0f8ee902af6a28e8719e7ba60f570771cd4e53453de6a30d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80183144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c3e12b7e15b238a9f83872ceb27196f077a464d48825b7e0d66ca35142d1aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:20:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:20:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.5.6
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 19:47:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 19:47:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:52:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:52:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:52:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:52:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:52:48 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 22:31:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 22:31:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 22:33:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 22:33:06 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 22:33:06 GMT
ENV COMPOSER_VERSION=2.2.27
# Fri, 08 May 2026 22:33:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 22:33:07 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 22:33:07 GMT
WORKDIR /app
# Fri, 08 May 2026 22:33:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 22:33:07 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59216db1edcf64b90905df63416f821bfacdba590544dcdb3c340ea538567c`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 3.8 MB (3767095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dbb332183b4f53eb48b10e61f11a67b23c5647a6901cf35be6037e209a0f51`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd758015c67cd7fae70202df89f7e42a01ff424cadf0cd92070805333b28821`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5702960144fbb228318e4c40ca2e9c98158a8c7b9f71390320236bda898ca95`  
		Last Modified: Fri, 08 May 2026 19:53:03 GMT  
		Size: 14.4 MB (14417280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358ab27e77a70ddec9b84d07b8f7d4afdddd40d4273150e0f53f745558ec45e`  
		Last Modified: Fri, 08 May 2026 19:53:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d790c857f23d764dbb55c79e470cb965a5e1400d248610a1b021e5da4b086f`  
		Last Modified: Fri, 08 May 2026 19:53:04 GMT  
		Size: 23.1 MB (23128501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d767ccb38fac4728b8964553352783881ac8482bff309e0e7a49475c1c68d10`  
		Last Modified: Fri, 08 May 2026 19:53:03 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792fe8cb0c39c5be7986dfbc108e720fbe9f5b205a09ea9e786278ca7d2d3b11`  
		Last Modified: Fri, 08 May 2026 19:53:04 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2594f5b2cc2f273332e529c87042778906a76cf847c1bbbfb0afb3a53554b1b5`  
		Last Modified: Fri, 08 May 2026 22:32:56 GMT  
		Size: 34.2 MB (34180303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ac582f80c6a79ddb5212f9a4b1ef780331e87889d7c30fee1b86fc32cdbbc0`  
		Last Modified: Fri, 08 May 2026 22:32:54 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c724b4a91d8a9f40460d6e944cb2a2ace01b2d558b70cb6fa8cb183ef3510ef0`  
		Last Modified: Fri, 08 May 2026 22:33:19 GMT  
		Size: 830.9 KB (830902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0a18f80c2f747c7d126ea3b387f40c3de0891e79d6a4e4f06a3af85d8a5bc5`  
		Last Modified: Fri, 08 May 2026 22:33:19 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31ef7c11c68d34284471e0eaacd3d990469830b0cb299d29e0950d401fc4399`  
		Last Modified: Fri, 08 May 2026 22:33:19 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:b8841020f8539b4bbb8333df0889b2bfee26cebe7dbba3844dff8853b2fc39b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ca47b42511b383000e9e05c33292a5ea2fa19c456b7b7f9cf86835f2ba294e`

```dockerfile
```

-	Layers:
	-	`sha256:204224a0aff05e42f74046ecefcb72e9d04eab5c368df929c751e5f631a69a8a`  
		Last Modified: Fri, 08 May 2026 22:33:19 GMT  
		Size: 2.2 MB (2177913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:683c0f3aab11301f7c237cabfa335e188c1dac3d72369bafcc7b68e1ba3204e2`  
		Last Modified: Fri, 08 May 2026 22:33:18 GMT  
		Size: 30.1 KB (30100 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:d3e62c3847d9f66d96a8b052581cbf8b03003443fd3f6754735376e97ef4b492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75059574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabc511ffebcd628557a60fa3a74639b2b9217b2a188a1b8eb48bc35c709a8d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 16 Apr 2026 00:30:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Apr 2026 00:30:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_VERSION=8.5.6
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 21:51:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 21:51:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:52:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 22:52:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:52:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 22:52:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 22:52:16 GMT
CMD ["php" "-a"]
# Mon, 11 May 2026 00:57:44 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 11 May 2026 00:57:45 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 11 May 2026 01:06:39 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 11 May 2026 01:06:39 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 11 May 2026 01:06:39 GMT
ENV COMPOSER_VERSION=2.2.27
# Mon, 11 May 2026 01:06:39 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 11 May 2026 01:06:39 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 11 May 2026 01:06:39 GMT
WORKDIR /app
# Mon, 11 May 2026 01:06:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 01:06:39 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78828518b8b5af0bc74ba3bd169a5c835b32f2a1452a7cd03ad8117a0128165b`  
		Last Modified: Thu, 16 Apr 2026 01:32:16 GMT  
		Size: 3.7 MB (3734242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1c9b4ddefe159b602dd6cdf3bcfff1bf48c922a0f1047bb5402dc2c6c988b`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2a62067bd9660d4987f0df8c18a9ac2818a33d0443ac9c5c806eb7925b9957`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b300791544e0c87f44b461c514787bf7d38ce6f5ad1d34bad34bc1c4782d3f`  
		Last Modified: Fri, 08 May 2026 22:53:24 GMT  
		Size: 14.4 MB (14417294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a331978dcb7855b965e50fa41230cb7f963d49113c956b0e49057d02df423466`  
		Last Modified: Fri, 08 May 2026 22:53:20 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcc286c95072e0d8d8b60f5e888859a51d02c496556840b68e28764a6173ecd`  
		Last Modified: Fri, 08 May 2026 22:53:25 GMT  
		Size: 21.2 MB (21171065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9799a7293faac913a8c2e0ba1a7628be32b2a5ea0e7dd2d76b844e7dfce47ad`  
		Last Modified: Fri, 08 May 2026 22:53:19 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb29c91c88ab86cb8131cb830f2bb49a8ffa2614cedc1c31b69e2c77a975695d`  
		Last Modified: Fri, 08 May 2026 22:53:21 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c65261e37a7d3f9ee21b1c9a9bd5ea90cb040884d3cbfb68f7150999f038c4`  
		Last Modified: Mon, 11 May 2026 01:02:48 GMT  
		Size: 31.3 MB (31299460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4361abd2c1daef5f4b6053d114136340df2419298fa403e48ae9996cced2b79`  
		Last Modified: Mon, 11 May 2026 01:02:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ddca659560ff095583ad782cb2a44201ad37f1934ce33356c3e8eda4bf9232`  
		Last Modified: Mon, 11 May 2026 01:07:40 GMT  
		Size: 821.7 KB (821710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e386e5330b7933ee52c101dafc5db0caa22b958319d0ea59bf5260d1150957`  
		Last Modified: Mon, 11 May 2026 01:07:40 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ae31d344729dc268783a3bb3d7ae0b831f7d040bed215294105acf718368d9`  
		Last Modified: Mon, 11 May 2026 01:07:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:3e286aa79885cd52fc8841dd48374c88365854a1de68390911d6b1f56dc54cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9d5a8f33db939295c38dcad181a94f1196bc40e5228348e9f5273d30f04af8`

```dockerfile
```

-	Layers:
	-	`sha256:98ef16b70e65173d452602a8313512967c96174976712638a7dab6a02e182de9`  
		Last Modified: Mon, 11 May 2026 01:07:40 GMT  
		Size: 2.2 MB (2176854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d0b1176d36244d5695fb9a52e303e768369387f426afed8bda9b838c7ebfdb2`  
		Last Modified: Mon, 11 May 2026 01:07:40 GMT  
		Size: 30.1 KB (30100 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:e2b5dde5685bf47233a28543f27b7452843f16d9d59b835480902fe3fcbb2fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76500782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96af798fc563174a44e55f6a222531922538ccabcead4dc3bea95a030670f9a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:41:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 May 2026 23:41:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 05 May 2026 23:41:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 05 May 2026 23:41:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 May 2026 23:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 May 2026 23:41:50 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_VERSION=8.5.6
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:51:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:57:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:57:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:57:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:57:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:57:50 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:14:30 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:14:30 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:14:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:14:54 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:14:54 GMT
ENV COMPOSER_VERSION=2.2.27
# Fri, 08 May 2026 17:14:54 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:14:54 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:14:54 GMT
WORKDIR /app
# Fri, 08 May 2026 17:14:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:14:54 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e5b23cd7e08583775ca52654782b3eb898be0895811ff074d0b60e2bdabdca`  
		Last Modified: Tue, 05 May 2026 23:50:39 GMT  
		Size: 3.8 MB (3787468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f70f6e1cd967f35b17107285a2dc3920f6cf2d49ba0521083fa3949317113`  
		Last Modified: Tue, 05 May 2026 23:50:38 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cc64825ed6643492e29ef55789e3eb5ed14b413945792b7bc86db5b7c4e70c`  
		Last Modified: Tue, 05 May 2026 23:50:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70b8b3c23d4b9513ddce760870ee58e711276bb86bdaa74045eafcaf6ae2dc`  
		Last Modified: Fri, 08 May 2026 16:58:06 GMT  
		Size: 14.4 MB (14417277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a38b097c90d256a49ef7bdca140fa8da69c874c923a1dfdd3513846d669f87`  
		Last Modified: Fri, 08 May 2026 16:58:06 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31050156e2ccbc94f9c20b8bcc6638051971128034fb34ad2fdcd18496bf5ec`  
		Last Modified: Fri, 08 May 2026 16:58:07 GMT  
		Size: 21.6 MB (21596857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac685bed84db73eb81d30fa0fa48e67ef3dc625228c72a0ebbc4c8799811eb2`  
		Last Modified: Fri, 08 May 2026 16:58:06 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3171cf62ee41e70bb40f0a98476a7b9f2b6ae9b42d0846873babe98b876b5b60`  
		Last Modified: Fri, 08 May 2026 16:58:07 GMT  
		Size: 23.2 KB (23211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7787013b1da03d9633569a1babfe5be53e33425a5cc32ac2304c9e8ca32553c`  
		Last Modified: Fri, 08 May 2026 17:15:16 GMT  
		Size: 32.1 MB (32116737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bba2a9fd6bf2cce08f308a330e727fecc9d5742f206d4dc17d1796213d1989`  
		Last Modified: Fri, 08 May 2026 17:15:15 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820d9569b37cde519dd2b1a708420be1ef06e6712900738a3acc85601cc09640`  
		Last Modified: Fri, 08 May 2026 17:15:15 GMT  
		Size: 827.8 KB (827842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865fd5fc01c6f007794882751138e08a543f862baa2a25ad2f4cf9f22d49558e`  
		Last Modified: Fri, 08 May 2026 17:15:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391907f45c9d176324f88b67327e83082aadf5581305a25d5a6fca39c6b03c22`  
		Last Modified: Fri, 08 May 2026 17:15:16 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:15b0a3be236008edbc8a939bfa4f2ded5e3159f2b728780040c2f9b224512213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca03d45a20909d0a23b90a95ed5aac575d4e6697ae72519d2f73045d29952fb5`

```dockerfile
```

-	Layers:
	-	`sha256:b399569195a13b97ec44c021df04e195823903b35ef1b10429b40be7d0239822`  
		Last Modified: Fri, 08 May 2026 17:15:15 GMT  
		Size: 2.2 MB (2176648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dcfdb000b62f8482cc30ebe088dc3ae32b421b327229bf7a1b7d9958dd28b6`  
		Last Modified: Fri, 08 May 2026 17:15:15 GMT  
		Size: 30.1 KB (30064 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.28`

**does not exist** (yet?)

## `composer:2.9`

```console
$ docker pull composer@sha256:02062f7719ec9433a9d4256cfba1c792db96dc9db60a4a92e48264c9e166b877
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

### `composer:2.9` - linux; amd64

```console
$ docker pull composer@sha256:53cf0b9d41bdaeecf5d8a77c68e29261f94882e967d938857bf71fd2e34b3f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78484055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff46f57437edc2ca4595a7a8d78662fa8244cb1d42613e67f18b9955fbb809ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:42:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:42:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:42:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:42:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:42:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:42:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:42:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:45:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:45:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:45:39 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:12:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:12:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:13:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:13:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:13:06 GMT
WORKDIR /app
# Fri, 08 May 2026 17:13:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:13:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b654640ed6c037ccdd1a25b2ae62a871ca0e1bf5f618ba969849b3b37e41af9`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 3.6 MB (3587616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40dc33330cb19d83115d1ae026d5d72ac32bd8f837cb79fd478c41aa3f53402`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e446c9444036d9a2b21592e04a74826d4671da791aae6d29163a697fac95881`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876fc8d6931dd52d5f7c4f3cc4c919d4d1322fe96fb1fd86cfcf7263dc5d76e`  
		Last Modified: Fri, 08 May 2026 16:45:48 GMT  
		Size: 14.4 MB (14417256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc09d7abe17a7b63967addd04a8285ed821149aaf96abb091020b22dfc68da0`  
		Last Modified: Fri, 08 May 2026 16:45:48 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7df31be2e3d6e83e0a06d7db20dd2ed43de7db70f1f45922f5c9f31516c2e0`  
		Last Modified: Fri, 08 May 2026 16:45:49 GMT  
		Size: 22.7 MB (22737297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82f0392f38de2fe157b97e8b3e797cc29975af6582edfbe95f905610501469d`  
		Last Modified: Fri, 08 May 2026 16:45:49 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d06dd6155739ed0fdc8c2b8f504f010792857d77998808592321d2f069d66`  
		Last Modified: Fri, 08 May 2026 16:45:49 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de747511d75dae581727a208d63cfb5dea9e1fc1abcecacab949f5b12312bfd`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 32.8 MB (32828492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269a50648c44005c9ce75745a80fe4eeba16e58075b02faaba9167dd62f94f6c`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f99f1add8b2e47ef4c93e3ef8db7e4ee1ff4f1ddec9668a7dc678dcae1a761`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 1.0 MB (1020970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54e359a2490a0cfb8cf0abd62ae66660b8bd29c46d0188821477f2793f5c779`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ec74ff474580cdfb131bba3665bbe4d30f27af1621c5765f8d129184953152`  
		Last Modified: Fri, 08 May 2026 17:13:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:b2e58d5d24fd4b4f29ea1a2909f182c866afb66581e952e0ab448cd5149b75ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753008aac0ec509459ba1b22c11c5f9fcb0c6b33ebf6b6a64460232c39a621d1`

```dockerfile
```

-	Layers:
	-	`sha256:746c6fb2ee8c17dcbc39cb6c9c0556a4a7e6ebad1896dc253fb9af81cd91d091`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 2.2 MB (2178657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0ae0ecb79efd72ef7fb43faccb0213b01a36a52ce2b4406756c7343383482d5`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9` - linux; arm variant v6

```console
$ docker pull composer@sha256:d8f4737995e55f7ee7537b83414ec0ddd381fb5c791509eca6170ef062676e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74944089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f509acb9370fd0b773b49d03f931dd6c664361af2afcea51e8c940bcb200416b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:37:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:37:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:37:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:37:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:37:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:37:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:37:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:37:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:40:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:40:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:40:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:40:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:40:33 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:16:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:16:45 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:17:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:17:09 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:17:09 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:17:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:17:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:17:09 GMT
WORKDIR /app
# Fri, 08 May 2026 17:17:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:17:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7063123be49bca3c998dd15fff3e6bf8b9037bf5d865219ec15d07a6a71f28dc`  
		Last Modified: Fri, 08 May 2026 16:40:39 GMT  
		Size: 3.5 MB (3543633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9796ddaa8b110e8c816d869c6bc6fdcd20ddfbdc2639897f4ea4e471eb76d9da`  
		Last Modified: Fri, 08 May 2026 16:40:38 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d042438a1f97af109fca616efe49b3235d7670aed6e54b7ac442be53baf34b9`  
		Last Modified: Fri, 08 May 2026 16:40:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f0c23d67858d02523a626ed972e24d143da08132aca3dc630277e8583931d8`  
		Last Modified: Fri, 08 May 2026 16:40:39 GMT  
		Size: 14.4 MB (14417274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a6444cc1ed13e98572aaf15c85e820b0ef5b704841ee7c0b1f67c6dbea66ef`  
		Last Modified: Fri, 08 May 2026 16:40:39 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4768db37e754a6d93cc79ac0a31a2ea1f70184527bcd68959c2ab652d02d1c9`  
		Last Modified: Fri, 08 May 2026 16:40:40 GMT  
		Size: 19.7 MB (19697128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f957f930966405369a831e03ca98d7ba85c480752557629a73a620ffe0d90c`  
		Last Modified: Fri, 08 May 2026 16:40:40 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1427b05be5ea97cb6c0e772bc00d53506512fe29ee3be3e18c369541c419e929`  
		Last Modified: Fri, 08 May 2026 16:40:40 GMT  
		Size: 23.2 KB (23197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dff3060bb020b0473474d4cb9fdd4803f80e08b9cb2f4ea223d8c47157e504`  
		Last Modified: Fri, 08 May 2026 17:17:17 GMT  
		Size: 32.7 MB (32665130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e491c1151f322528ac8da5713503882aa94b82e54abcfa9f69617d54bbeca985`  
		Last Modified: Fri, 08 May 2026 17:17:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc745588e596fde362f8c52dfa19dddd1cf9246f31b3ef3996b1ffc1ee43f6e`  
		Last Modified: Fri, 08 May 2026 17:17:17 GMT  
		Size: 1.0 MB (1021009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b05442fa40f67a80fbab357e3df30103fdc4a61691ed44913bf29bb1399c15`  
		Last Modified: Fri, 08 May 2026 17:17:17 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96154d4dfff66bad1ef878d986e6586487cdd509d291703f58ec0a18f6adc944`  
		Last Modified: Fri, 08 May 2026 17:17:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:cb8787c6d483c7ef737b88b7bb3a9b629d1d8bdb24365a44d4bb732c16447ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f95bafc6309e007d8e4f38c71a8327894ba5bd97f02638330ec37d277bbd1a`

```dockerfile
```

-	Layers:
	-	`sha256:da5b01da4e7fa686621bc3af7fac04b24513974542ccfa5799f5d68e2ceb1293`  
		Last Modified: Fri, 08 May 2026 17:17:16 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9` - linux; arm variant v7

```console
$ docker pull composer@sha256:cc5f9d74347953922012cb33c56431b1474184be21bbad0c50aca87942ba3319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71765815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff801114ce25400a1404f7598ff059edddcc5da4ac7b1e70f7d7c5a9cc377c21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:44:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:44:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:44:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:44:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:44:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:44:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:44:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:44:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:47:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:47:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:47:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:47:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:47:48 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:17:51 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:17:51 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:18:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:18:14 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:18:14 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:18:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:18:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:18:14 GMT
WORKDIR /app
# Fri, 08 May 2026 17:18:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:18:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad56310a751a6c77d98383a79b8b40902a76cd99bbf031203cb5e50009a7e21`  
		Last Modified: Fri, 08 May 2026 16:47:56 GMT  
		Size: 3.3 MB (3343518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c349e30aca535b108f20451e16f49be87dafc29ff25aa3cb46d835f1cfd79c`  
		Last Modified: Fri, 08 May 2026 16:47:55 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a86d13cd318b8c71ed9e3d842909aef3bd247db089054a734caf702a4494e7a`  
		Last Modified: Fri, 08 May 2026 16:47:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e0ebb3537ef57ac21c0136ab9d86c6cf673686a1758c7dccf2e0507677c4ca`  
		Last Modified: Fri, 08 May 2026 16:47:56 GMT  
		Size: 14.4 MB (14417282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630cde6decb0613f633233436ae8d90ee7ac540ee35fdcc79a02830b44cde2d9`  
		Last Modified: Fri, 08 May 2026 16:47:57 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe23a1ee2edd4df1b0b2cb1b55f49f366672aee55411cf4f3a2482a5ef63859e`  
		Last Modified: Fri, 08 May 2026 16:47:57 GMT  
		Size: 18.6 MB (18586006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a83f016507951154ecee1da8a8a702c4913bcf89a5352f214180fd893ee7e`  
		Last Modified: Fri, 08 May 2026 16:47:57 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aacec4ecdb1ac54d3f59f543d94f4d982681fee3b6017409510c7db02a56cd3`  
		Last Modified: Fri, 08 May 2026 16:47:58 GMT  
		Size: 23.2 KB (23207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1609486e3fbc531402cdafca7c4d66bbe99aec7a16c658fba42c842dfffc4d15`  
		Last Modified: Fri, 08 May 2026 17:18:24 GMT  
		Size: 31.1 MB (31096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b2f2f550ad5a55cc50fd37619e858e9520c81e24b5ab12d8740ed3f9774744`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de963be19db260c4d1ecaa29abea921afae50d8596803e760b6cdbddcf47fa4f`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 1.0 MB (1011442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2626607b68a635ac9532e2b9a5a9b58eb8e1b1831ae92813511c3ac726b744`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1848b8c9ab7b90543a2747f0793762ca2e39358956a467811dcce1b1538039d5`  
		Last Modified: Fri, 08 May 2026 17:18:24 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:463c12dfc3c1783ddd7df87a857010aedb0227ff78ad920ee0e5bb3bd04b274e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434eab32ce67c1bb0264ed8065a6f1baf42a44b342102b2028e449774550a13f`

```dockerfile
```

-	Layers:
	-	`sha256:0b0e7f2b324a71b90066d60e3576a4be7bc93787f1cf62c76dc1fe9c6fc61023`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 2.2 MB (2178328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283190992301d9998ab0ef9162d01dc8b93c6cbe1171e49b615dd1351af7f233`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 30.8 KB (30773 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:16fc896e904662ba6b82db1a156864c97a42083b456cefca413e44d2d5d48d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78144594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76ff5069c100e0c2bab675679be74b6c604790ea8e3fb69eb52f9d1c83a220a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:41:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:41:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:41:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:41:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:41:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:41:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:41:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:45:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:45:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:45:21 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:13:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:13:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:13:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:13:28 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:13:28 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:13:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:13:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:13:28 GMT
WORKDIR /app
# Fri, 08 May 2026 17:13:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:13:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fccd1681e76186ece96de411a47fcf0a2ea8b3a42bea388612e2ad17682df83`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 3.6 MB (3596160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b123c2ad03bae81cac30c7ce6c83449c58af169a38e2769582cf57b4bd5fec2`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19e0156c658a50f56baef5e593490b5422a02e961c8c72379e3ecfec4bbe8f`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882cd6a9aa6b8d82c2bd2475162ef7321121ed51bd6227365f4118b9ee016d51`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 14.4 MB (14417265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dd7533a619b5ba3534670946cde6191553e5eeba6399d44b5d1b0902176a5a`  
		Last Modified: Fri, 08 May 2026 16:45:30 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e4c9ba7c6c87f5254867ebaa82b91c46bfb66fc18f43dee2582724cc72d33c`  
		Last Modified: Fri, 08 May 2026 16:45:31 GMT  
		Size: 21.9 MB (21912560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2023c08468a22348b2f976f9c71b54d7afc2b0d8f0c5abba36494ff090f157`  
		Last Modified: Fri, 08 May 2026 16:45:31 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea47019ff974219dca03451a8728ab2d8389f57d08ae0db784f0a0b68f3d5739`  
		Last Modified: Fri, 08 May 2026 16:45:31 GMT  
		Size: 23.2 KB (23210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc79e203ef84c43f54c47df5625b30a4bfaadb6fd2098d4645b6ade1b6cae86f`  
		Last Modified: Fri, 08 May 2026 17:13:39 GMT  
		Size: 33.0 MB (32970871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e04d47530b717eb87b2d3cb3ad54c6275aaec2527b39d824839db9a79dc66e`  
		Last Modified: Fri, 08 May 2026 17:13:37 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d044ee4a5c5e3f1126f849352857799eaffbc5be36bf6c1201083713111971`  
		Last Modified: Fri, 08 May 2026 17:13:38 GMT  
		Size: 1.0 MB (1019808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe82d1d4338e8583db891c7f71bdfd70b97c6e2ecf06e3e87679821668892af`  
		Last Modified: Fri, 08 May 2026 17:13:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8dd62b0c5bf51f6d305cc43debbaeb5ff5403e72d5b8533a80aa562d7c33b3`  
		Last Modified: Fri, 08 May 2026 17:13:39 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:a3b00a48da16f5c9b1bc08f29f178f82170ca2567b3caadc5db6e1abf5668dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ae42e0cdb89975c6c9f1c106c094a38e5f1b52ad00abc05b83adbde915ec5c`

```dockerfile
```

-	Layers:
	-	`sha256:353d3c7c3f15f78cb51d5c3773b552c563d10916326a051b5d4503c11b4f6623`  
		Last Modified: Fri, 08 May 2026 17:13:37 GMT  
		Size: 2.2 MB (2178158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38cd920e5244111e906a24374c25aaa430b0df481f42512fa6593471e763c19f`  
		Last Modified: Fri, 08 May 2026 17:13:37 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9` - linux; 386

```console
$ docker pull composer@sha256:c7684d3fed68105ad4f06bc286b2bcfb932ccfd4465899af81ecc7441e59088f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79333375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b598f10979ecabbbecd2fbeca22124ace9a9ace399cda7e378aae0af918c2c33`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:45:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:45:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:45:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:45:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:45:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:45:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:45:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:49:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:49:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:49:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:49:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:49:23 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:12:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:12:50 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:13:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:13:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:13:06 GMT
WORKDIR /app
# Fri, 08 May 2026 17:13:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:13:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5f818fb7c09d275f57b0be232e3327c598854c2cd8c1af2e5536f47c030109`  
		Last Modified: Fri, 08 May 2026 16:49:31 GMT  
		Size: 3.6 MB (3625695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bde2dbfa2d2a3c95dc2eb8f7e57ce0c5861a36e95ff913cab891df185c56779`  
		Last Modified: Fri, 08 May 2026 16:49:31 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f7ce7672df1bccaf696725c7cf018abd4fcce22df9ddd66674d1d181d1fb1`  
		Last Modified: Fri, 08 May 2026 16:49:31 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c78a34ca66f37347555dd11601a37b28fb5dc7b9164650aef7bbcdc265237d`  
		Last Modified: Fri, 08 May 2026 16:49:32 GMT  
		Size: 14.4 MB (14417249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d49058f5e508fbedf7c1761ed74c3488a1b66aa1c53245df6f5c202bd01e68`  
		Last Modified: Fri, 08 May 2026 16:49:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0d59880de31c08bb1c82cab93a0766a728df6e6f0b2f8b018340e1f90e839e`  
		Last Modified: Fri, 08 May 2026 16:49:33 GMT  
		Size: 23.2 MB (23185462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b3fdeafdda5d52745fb055ae2c3da55119fc9058b9c9ac2880f1358ed8790`  
		Last Modified: Fri, 08 May 2026 16:49:33 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179dc4512664e42fc76b4cbd3cb62d559b6534581642050bc82876d631c7be5c`  
		Last Modified: Fri, 08 May 2026 16:49:33 GMT  
		Size: 23.4 KB (23378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7d15ac4f12ca126a295236e4d7d0544b30ba61b18f042c1b2b3c1c5f5c1894`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 33.4 MB (33353595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c445445a600188721e5cd81fe3fc287d738e58cffc77ebe8e25ba5cce6155f86`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88601221afe1744e48943b5c1fe721cb5ac894586745c4a3780ac3f588ad7a`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 1.0 MB (1032700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b04c9c8d07dca7ff58a463258a23075b5124f8dc39586c413c774fdd43ca7`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ec74ff474580cdfb131bba3665bbe4d30f27af1621c5765f8d129184953152`  
		Last Modified: Fri, 08 May 2026 17:13:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:7c6caa805b56d2cf26b35c94546e7ef1d5a5dec144b18729498db946dbcd9c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc0ec7f96942e271b7d7631c3b46d6dbb800d5d898b2c6fe6ebd881faddd386`

```dockerfile
```

-	Layers:
	-	`sha256:030ced0a8be99eea3c9b9fd78f0393f312863b389dc7a53d3d17f94c8431c692`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 2.2 MB (2178442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b33345f3941243a749471efabde80bc10e90cfaea692daa3fe8531fae4a866`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 30.6 KB (30631 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9` - linux; ppc64le

```console
$ docker pull composer@sha256:3a37fd68a6042cb82fd1c521b31aef4ca1d26d867c7b9c13d7401784777eeff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80378812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765290965180ecbca7e191081d78c709ff334540dff4504dc828ba8496da13ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:20:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:20:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.5.6
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 19:47:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 19:47:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:52:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:52:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:52:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:52:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:52:48 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 22:31:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 22:31:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 22:32:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 22:32:37 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 22:32:37 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 22:32:37 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 22:32:37 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 22:32:37 GMT
WORKDIR /app
# Fri, 08 May 2026 22:32:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 22:32:37 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59216db1edcf64b90905df63416f821bfacdba590544dcdb3c340ea538567c`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 3.8 MB (3767095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dbb332183b4f53eb48b10e61f11a67b23c5647a6901cf35be6037e209a0f51`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd758015c67cd7fae70202df89f7e42a01ff424cadf0cd92070805333b28821`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5702960144fbb228318e4c40ca2e9c98158a8c7b9f71390320236bda898ca95`  
		Last Modified: Fri, 08 May 2026 19:53:03 GMT  
		Size: 14.4 MB (14417280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358ab27e77a70ddec9b84d07b8f7d4afdddd40d4273150e0f53f745558ec45e`  
		Last Modified: Fri, 08 May 2026 19:53:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d790c857f23d764dbb55c79e470cb965a5e1400d248610a1b021e5da4b086f`  
		Last Modified: Fri, 08 May 2026 19:53:04 GMT  
		Size: 23.1 MB (23128501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d767ccb38fac4728b8964553352783881ac8482bff309e0e7a49475c1c68d10`  
		Last Modified: Fri, 08 May 2026 19:53:03 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792fe8cb0c39c5be7986dfbc108e720fbe9f5b205a09ea9e786278ca7d2d3b11`  
		Last Modified: Fri, 08 May 2026 19:53:04 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2594f5b2cc2f273332e529c87042778906a76cf847c1bbbfb0afb3a53554b1b5`  
		Last Modified: Fri, 08 May 2026 22:32:56 GMT  
		Size: 34.2 MB (34180303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ac582f80c6a79ddb5212f9a4b1ef780331e87889d7c30fee1b86fc32cdbbc0`  
		Last Modified: Fri, 08 May 2026 22:32:54 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72388f9529399090e5800a46557ae5093e9aeacd27281f855788291ddb37069e`  
		Last Modified: Fri, 08 May 2026 22:32:55 GMT  
		Size: 1.0 MB (1026571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25f9d92287139c4c82a3bac211848cb7a07d6f2aa71ce60801c76d1ef214beb`  
		Last Modified: Fri, 08 May 2026 22:32:54 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a103edbe4df44409e697cd61db384f5cdfb624730e03035597985b13bda6a050`  
		Last Modified: Fri, 08 May 2026 22:32:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:a2d34893c3a2c5fb4746092fe95ba67b9c6f72589696f5b80baa03608007418a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7e76daebcc65909e955a1b3934377e39f50689ddeeae82674e6453d372226d`

```dockerfile
```

-	Layers:
	-	`sha256:10d3d3b85cb1245b350e666620671874ef164948262ea04701a0e063108eab93`  
		Last Modified: Fri, 08 May 2026 22:32:54 GMT  
		Size: 2.2 MB (2178515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01f2d29228b635dc3ef228ece64bda988eaad8b7fa7fcca684415e671fea1d47`  
		Last Modified: Fri, 08 May 2026 22:32:54 GMT  
		Size: 30.7 KB (30715 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9` - linux; riscv64

```console
$ docker pull composer@sha256:201fb227742eda84c3920f1565e36deec0155cc20c27503627daad12fcc76545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75255480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16f0073e3ec90e47a472eea73f9e48783013f33733be9a1a6b00ca52915ef16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 16 Apr 2026 00:30:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Apr 2026 00:30:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_VERSION=8.5.6
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 21:51:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 21:51:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:52:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 22:52:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:52:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 22:52:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 22:52:16 GMT
CMD ["php" "-a"]
# Mon, 11 May 2026 00:57:44 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 11 May 2026 00:57:45 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 11 May 2026 01:01:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 11 May 2026 01:01:09 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 11 May 2026 01:01:09 GMT
ENV COMPOSER_VERSION=2.9.7
# Mon, 11 May 2026 01:01:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 11 May 2026 01:01:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 11 May 2026 01:01:09 GMT
WORKDIR /app
# Mon, 11 May 2026 01:01:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 01:01:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78828518b8b5af0bc74ba3bd169a5c835b32f2a1452a7cd03ad8117a0128165b`  
		Last Modified: Thu, 16 Apr 2026 01:32:16 GMT  
		Size: 3.7 MB (3734242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1c9b4ddefe159b602dd6cdf3bcfff1bf48c922a0f1047bb5402dc2c6c988b`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2a62067bd9660d4987f0df8c18a9ac2818a33d0443ac9c5c806eb7925b9957`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b300791544e0c87f44b461c514787bf7d38ce6f5ad1d34bad34bc1c4782d3f`  
		Last Modified: Fri, 08 May 2026 22:53:24 GMT  
		Size: 14.4 MB (14417294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a331978dcb7855b965e50fa41230cb7f963d49113c956b0e49057d02df423466`  
		Last Modified: Fri, 08 May 2026 22:53:20 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcc286c95072e0d8d8b60f5e888859a51d02c496556840b68e28764a6173ecd`  
		Last Modified: Fri, 08 May 2026 22:53:25 GMT  
		Size: 21.2 MB (21171065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9799a7293faac913a8c2e0ba1a7628be32b2a5ea0e7dd2d76b844e7dfce47ad`  
		Last Modified: Fri, 08 May 2026 22:53:19 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb29c91c88ab86cb8131cb830f2bb49a8ffa2614cedc1c31b69e2c77a975695d`  
		Last Modified: Fri, 08 May 2026 22:53:21 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c65261e37a7d3f9ee21b1c9a9bd5ea90cb040884d3cbfb68f7150999f038c4`  
		Last Modified: Mon, 11 May 2026 01:02:48 GMT  
		Size: 31.3 MB (31299460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4361abd2c1daef5f4b6053d114136340df2419298fa403e48ae9996cced2b79`  
		Last Modified: Mon, 11 May 2026 01:02:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4e9a5a183a412aeab22b9bd7a35dbe3ddf399a681f5635e496b9c528121cc1`  
		Last Modified: Mon, 11 May 2026 01:02:44 GMT  
		Size: 1.0 MB (1017615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7681fc7957bbd94bf344f9bd1d7d20f834516ef48691c0bdd749d92ec99fdf2`  
		Last Modified: Mon, 11 May 2026 01:02:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1a9a59e18e5374c9718c827255af5499b066d9dfa2132339e54344c31bf500`  
		Last Modified: Mon, 11 May 2026 01:01:23 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:a328837c6987cad2823792a27dcb579f1e02ff98360d0fdeab5bddf78b5dc12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9b86e0d7a6aeb07175f26c5e648750546e24b473d1dbd38b2478b319c806d2`

```dockerfile
```

-	Layers:
	-	`sha256:1c6aabf396b9034e4e8398ae6b930e4fed5f617e38493e2d4a2c36ce315be2ef`  
		Last Modified: Mon, 11 May 2026 01:02:44 GMT  
		Size: 2.2 MB (2177456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a51e1cba29e30595a491fb536a64e76d162dab7ff375b5848e32937d4358e2`  
		Last Modified: Mon, 11 May 2026 01:02:43 GMT  
		Size: 30.7 KB (30715 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9` - linux; s390x

```console
$ docker pull composer@sha256:99863cc662e4b5958234f74730006b98c072da8266d99f0688188349ebee9e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76696548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc203f97b83b8715f9a920330a5325d8ed4a3edcf20ded5cb7f3adfe1a85676`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:41:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 May 2026 23:41:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 05 May 2026 23:41:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 05 May 2026 23:41:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 May 2026 23:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 May 2026 23:41:50 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_VERSION=8.5.6
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:51:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:57:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:57:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:57:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:57:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:57:50 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:14:56 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:14:56 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:15:21 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:15:21 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:15:21 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:15:21 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:15:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:15:21 GMT
WORKDIR /app
# Fri, 08 May 2026 17:15:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:15:21 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e5b23cd7e08583775ca52654782b3eb898be0895811ff074d0b60e2bdabdca`  
		Last Modified: Tue, 05 May 2026 23:50:39 GMT  
		Size: 3.8 MB (3787468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f70f6e1cd967f35b17107285a2dc3920f6cf2d49ba0521083fa3949317113`  
		Last Modified: Tue, 05 May 2026 23:50:38 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cc64825ed6643492e29ef55789e3eb5ed14b413945792b7bc86db5b7c4e70c`  
		Last Modified: Tue, 05 May 2026 23:50:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70b8b3c23d4b9513ddce760870ee58e711276bb86bdaa74045eafcaf6ae2dc`  
		Last Modified: Fri, 08 May 2026 16:58:06 GMT  
		Size: 14.4 MB (14417277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a38b097c90d256a49ef7bdca140fa8da69c874c923a1dfdd3513846d669f87`  
		Last Modified: Fri, 08 May 2026 16:58:06 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31050156e2ccbc94f9c20b8bcc6638051971128034fb34ad2fdcd18496bf5ec`  
		Last Modified: Fri, 08 May 2026 16:58:07 GMT  
		Size: 21.6 MB (21596857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac685bed84db73eb81d30fa0fa48e67ef3dc625228c72a0ebbc4c8799811eb2`  
		Last Modified: Fri, 08 May 2026 16:58:06 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3171cf62ee41e70bb40f0a98476a7b9f2b6ae9b42d0846873babe98b876b5b60`  
		Last Modified: Fri, 08 May 2026 16:58:07 GMT  
		Size: 23.2 KB (23211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a5b3a5457c384d521a0679d9ad0cfe2efd36175f48ece0b87ed81ff481849`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 32.1 MB (32116524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d567a1a4fa1f8f4985421d4acd4135b3ad52ef380c3f5b44f0291c750cc47c`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82f007fb94228f94c86d027e3598ca58aa08111593d3ca64f403e622325a629`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 1.0 MB (1023820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a42c97b56e0830eede2e46fb214d069afd35578b2e1aee6d27d8af45f256707`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7726d52575774721ccc577d8e854ec56153c76f536b5ef5e8556ab5cbb039ee`  
		Last Modified: Fri, 08 May 2026 17:15:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:40436a63296c0d39fd5eb482c639272e706d6913e9f9203bee69df14cc3a4c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e856da7070e174ec6524a5c1bb2e68da3bac933ad4ae559cc7b63fdbb0b523c1`

```dockerfile
```

-	Layers:
	-	`sha256:97ee1766c209a040ea17e116ebf93e681b06c3c47dcb4f0063bbe36c36e6d312`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 2.2 MB (2177238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4e44f195d88ce08505dfde243f4efde4685113a38414e45fde22d52cd50add6`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.9.8`

**does not exist** (yet?)

## `composer:latest`

```console
$ docker pull composer@sha256:02062f7719ec9433a9d4256cfba1c792db96dc9db60a4a92e48264c9e166b877
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
$ docker pull composer@sha256:53cf0b9d41bdaeecf5d8a77c68e29261f94882e967d938857bf71fd2e34b3f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78484055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff46f57437edc2ca4595a7a8d78662fa8244cb1d42613e67f18b9955fbb809ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:42:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:42:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:42:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:42:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:42:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:42:09 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:42:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:42:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:45:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:45:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:45:39 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:12:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:12:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:13:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:13:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:13:06 GMT
WORKDIR /app
# Fri, 08 May 2026 17:13:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:13:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b654640ed6c037ccdd1a25b2ae62a871ca0e1bf5f618ba969849b3b37e41af9`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 3.6 MB (3587616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40dc33330cb19d83115d1ae026d5d72ac32bd8f837cb79fd478c41aa3f53402`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e446c9444036d9a2b21592e04a74826d4671da791aae6d29163a697fac95881`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876fc8d6931dd52d5f7c4f3cc4c919d4d1322fe96fb1fd86cfcf7263dc5d76e`  
		Last Modified: Fri, 08 May 2026 16:45:48 GMT  
		Size: 14.4 MB (14417256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc09d7abe17a7b63967addd04a8285ed821149aaf96abb091020b22dfc68da0`  
		Last Modified: Fri, 08 May 2026 16:45:48 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7df31be2e3d6e83e0a06d7db20dd2ed43de7db70f1f45922f5c9f31516c2e0`  
		Last Modified: Fri, 08 May 2026 16:45:49 GMT  
		Size: 22.7 MB (22737297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82f0392f38de2fe157b97e8b3e797cc29975af6582edfbe95f905610501469d`  
		Last Modified: Fri, 08 May 2026 16:45:49 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d06dd6155739ed0fdc8c2b8f504f010792857d77998808592321d2f069d66`  
		Last Modified: Fri, 08 May 2026 16:45:49 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de747511d75dae581727a208d63cfb5dea9e1fc1abcecacab949f5b12312bfd`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 32.8 MB (32828492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269a50648c44005c9ce75745a80fe4eeba16e58075b02faaba9167dd62f94f6c`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f99f1add8b2e47ef4c93e3ef8db7e4ee1ff4f1ddec9668a7dc678dcae1a761`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 1.0 MB (1020970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54e359a2490a0cfb8cf0abd62ae66660b8bd29c46d0188821477f2793f5c779`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ec74ff474580cdfb131bba3665bbe4d30f27af1621c5765f8d129184953152`  
		Last Modified: Fri, 08 May 2026 17:13:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:b2e58d5d24fd4b4f29ea1a2909f182c866afb66581e952e0ab448cd5149b75ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753008aac0ec509459ba1b22c11c5f9fcb0c6b33ebf6b6a64460232c39a621d1`

```dockerfile
```

-	Layers:
	-	`sha256:746c6fb2ee8c17dcbc39cb6c9c0556a4a7e6ebad1896dc253fb9af81cd91d091`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 2.2 MB (2178657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0ae0ecb79efd72ef7fb43faccb0213b01a36a52ce2b4406756c7343383482d5`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:d8f4737995e55f7ee7537b83414ec0ddd381fb5c791509eca6170ef062676e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74944089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f509acb9370fd0b773b49d03f931dd6c664361af2afcea51e8c940bcb200416b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:37:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:37:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:37:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:37:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:37:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:37:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:37:13 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:37:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:37:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:40:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:40:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:40:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:40:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:40:33 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:16:45 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:16:45 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:17:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:17:09 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:17:09 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:17:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:17:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:17:09 GMT
WORKDIR /app
# Fri, 08 May 2026 17:17:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:17:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7063123be49bca3c998dd15fff3e6bf8b9037bf5d865219ec15d07a6a71f28dc`  
		Last Modified: Fri, 08 May 2026 16:40:39 GMT  
		Size: 3.5 MB (3543633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9796ddaa8b110e8c816d869c6bc6fdcd20ddfbdc2639897f4ea4e471eb76d9da`  
		Last Modified: Fri, 08 May 2026 16:40:38 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d042438a1f97af109fca616efe49b3235d7670aed6e54b7ac442be53baf34b9`  
		Last Modified: Fri, 08 May 2026 16:40:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f0c23d67858d02523a626ed972e24d143da08132aca3dc630277e8583931d8`  
		Last Modified: Fri, 08 May 2026 16:40:39 GMT  
		Size: 14.4 MB (14417274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a6444cc1ed13e98572aaf15c85e820b0ef5b704841ee7c0b1f67c6dbea66ef`  
		Last Modified: Fri, 08 May 2026 16:40:39 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4768db37e754a6d93cc79ac0a31a2ea1f70184527bcd68959c2ab652d02d1c9`  
		Last Modified: Fri, 08 May 2026 16:40:40 GMT  
		Size: 19.7 MB (19697128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f957f930966405369a831e03ca98d7ba85c480752557629a73a620ffe0d90c`  
		Last Modified: Fri, 08 May 2026 16:40:40 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1427b05be5ea97cb6c0e772bc00d53506512fe29ee3be3e18c369541c419e929`  
		Last Modified: Fri, 08 May 2026 16:40:40 GMT  
		Size: 23.2 KB (23197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dff3060bb020b0473474d4cb9fdd4803f80e08b9cb2f4ea223d8c47157e504`  
		Last Modified: Fri, 08 May 2026 17:17:17 GMT  
		Size: 32.7 MB (32665130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e491c1151f322528ac8da5713503882aa94b82e54abcfa9f69617d54bbeca985`  
		Last Modified: Fri, 08 May 2026 17:17:16 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc745588e596fde362f8c52dfa19dddd1cf9246f31b3ef3996b1ffc1ee43f6e`  
		Last Modified: Fri, 08 May 2026 17:17:17 GMT  
		Size: 1.0 MB (1021009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b05442fa40f67a80fbab357e3df30103fdc4a61691ed44913bf29bb1399c15`  
		Last Modified: Fri, 08 May 2026 17:17:17 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96154d4dfff66bad1ef878d986e6586487cdd509d291703f58ec0a18f6adc944`  
		Last Modified: Fri, 08 May 2026 17:17:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:cb8787c6d483c7ef737b88b7bb3a9b629d1d8bdb24365a44d4bb732c16447ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f95bafc6309e007d8e4f38c71a8327894ba5bd97f02638330ec37d277bbd1a`

```dockerfile
```

-	Layers:
	-	`sha256:da5b01da4e7fa686621bc3af7fac04b24513974542ccfa5799f5d68e2ceb1293`  
		Last Modified: Fri, 08 May 2026 17:17:16 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:cc5f9d74347953922012cb33c56431b1474184be21bbad0c50aca87942ba3319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71765815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff801114ce25400a1404f7598ff059edddcc5da4ac7b1e70f7d7c5a9cc377c21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:44:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:44:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:44:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:44:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:44:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:44:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:44:35 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:44:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:44:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:47:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:47:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:47:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:47:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:47:48 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:17:51 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:17:51 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:18:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:18:14 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:18:14 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:18:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:18:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:18:14 GMT
WORKDIR /app
# Fri, 08 May 2026 17:18:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:18:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad56310a751a6c77d98383a79b8b40902a76cd99bbf031203cb5e50009a7e21`  
		Last Modified: Fri, 08 May 2026 16:47:56 GMT  
		Size: 3.3 MB (3343518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c349e30aca535b108f20451e16f49be87dafc29ff25aa3cb46d835f1cfd79c`  
		Last Modified: Fri, 08 May 2026 16:47:55 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a86d13cd318b8c71ed9e3d842909aef3bd247db089054a734caf702a4494e7a`  
		Last Modified: Fri, 08 May 2026 16:47:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e0ebb3537ef57ac21c0136ab9d86c6cf673686a1758c7dccf2e0507677c4ca`  
		Last Modified: Fri, 08 May 2026 16:47:56 GMT  
		Size: 14.4 MB (14417282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630cde6decb0613f633233436ae8d90ee7ac540ee35fdcc79a02830b44cde2d9`  
		Last Modified: Fri, 08 May 2026 16:47:57 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe23a1ee2edd4df1b0b2cb1b55f49f366672aee55411cf4f3a2482a5ef63859e`  
		Last Modified: Fri, 08 May 2026 16:47:57 GMT  
		Size: 18.6 MB (18586006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68a83f016507951154ecee1da8a8a702c4913bcf89a5352f214180fd893ee7e`  
		Last Modified: Fri, 08 May 2026 16:47:57 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aacec4ecdb1ac54d3f59f543d94f4d982681fee3b6017409510c7db02a56cd3`  
		Last Modified: Fri, 08 May 2026 16:47:58 GMT  
		Size: 23.2 KB (23207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1609486e3fbc531402cdafca7c4d66bbe99aec7a16c658fba42c842dfffc4d15`  
		Last Modified: Fri, 08 May 2026 17:18:24 GMT  
		Size: 31.1 MB (31096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b2f2f550ad5a55cc50fd37619e858e9520c81e24b5ab12d8740ed3f9774744`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de963be19db260c4d1ecaa29abea921afae50d8596803e760b6cdbddcf47fa4f`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 1.0 MB (1011442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2626607b68a635ac9532e2b9a5a9b58eb8e1b1831ae92813511c3ac726b744`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1848b8c9ab7b90543a2747f0793762ca2e39358956a467811dcce1b1538039d5`  
		Last Modified: Fri, 08 May 2026 17:18:24 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:463c12dfc3c1783ddd7df87a857010aedb0227ff78ad920ee0e5bb3bd04b274e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434eab32ce67c1bb0264ed8065a6f1baf42a44b342102b2028e449774550a13f`

```dockerfile
```

-	Layers:
	-	`sha256:0b0e7f2b324a71b90066d60e3576a4be7bc93787f1cf62c76dc1fe9c6fc61023`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 2.2 MB (2178328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283190992301d9998ab0ef9162d01dc8b93c6cbe1171e49b615dd1351af7f233`  
		Last Modified: Fri, 08 May 2026 17:18:23 GMT  
		Size: 30.8 KB (30773 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:16fc896e904662ba6b82db1a156864c97a42083b456cefca413e44d2d5d48d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78144594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76ff5069c100e0c2bab675679be74b6c604790ea8e3fb69eb52f9d1c83a220a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:41:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:41:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:41:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:41:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:41:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:41:55 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:41:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:41:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:45:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:45:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:45:21 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:13:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:13:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:13:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:13:28 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:13:28 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:13:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:13:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:13:28 GMT
WORKDIR /app
# Fri, 08 May 2026 17:13:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:13:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fccd1681e76186ece96de411a47fcf0a2ea8b3a42bea388612e2ad17682df83`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 3.6 MB (3596160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b123c2ad03bae81cac30c7ce6c83449c58af169a38e2769582cf57b4bd5fec2`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19e0156c658a50f56baef5e593490b5422a02e961c8c72379e3ecfec4bbe8f`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882cd6a9aa6b8d82c2bd2475162ef7321121ed51bd6227365f4118b9ee016d51`  
		Last Modified: Fri, 08 May 2026 16:45:29 GMT  
		Size: 14.4 MB (14417265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dd7533a619b5ba3534670946cde6191553e5eeba6399d44b5d1b0902176a5a`  
		Last Modified: Fri, 08 May 2026 16:45:30 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e4c9ba7c6c87f5254867ebaa82b91c46bfb66fc18f43dee2582724cc72d33c`  
		Last Modified: Fri, 08 May 2026 16:45:31 GMT  
		Size: 21.9 MB (21912560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2023c08468a22348b2f976f9c71b54d7afc2b0d8f0c5abba36494ff090f157`  
		Last Modified: Fri, 08 May 2026 16:45:31 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea47019ff974219dca03451a8728ab2d8389f57d08ae0db784f0a0b68f3d5739`  
		Last Modified: Fri, 08 May 2026 16:45:31 GMT  
		Size: 23.2 KB (23210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc79e203ef84c43f54c47df5625b30a4bfaadb6fd2098d4645b6ade1b6cae86f`  
		Last Modified: Fri, 08 May 2026 17:13:39 GMT  
		Size: 33.0 MB (32970871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e04d47530b717eb87b2d3cb3ad54c6275aaec2527b39d824839db9a79dc66e`  
		Last Modified: Fri, 08 May 2026 17:13:37 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d044ee4a5c5e3f1126f849352857799eaffbc5be36bf6c1201083713111971`  
		Last Modified: Fri, 08 May 2026 17:13:38 GMT  
		Size: 1.0 MB (1019808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe82d1d4338e8583db891c7f71bdfd70b97c6e2ecf06e3e87679821668892af`  
		Last Modified: Fri, 08 May 2026 17:13:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8dd62b0c5bf51f6d305cc43debbaeb5ff5403e72d5b8533a80aa562d7c33b3`  
		Last Modified: Fri, 08 May 2026 17:13:39 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:a3b00a48da16f5c9b1bc08f29f178f82170ca2567b3caadc5db6e1abf5668dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ae42e0cdb89975c6c9f1c106c094a38e5f1b52ad00abc05b83adbde915ec5c`

```dockerfile
```

-	Layers:
	-	`sha256:353d3c7c3f15f78cb51d5c3773b552c563d10916326a051b5d4503c11b4f6623`  
		Last Modified: Fri, 08 May 2026 17:13:37 GMT  
		Size: 2.2 MB (2178158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38cd920e5244111e906a24374c25aaa430b0df481f42512fa6593471e763c19f`  
		Last Modified: Fri, 08 May 2026 17:13:37 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:c7684d3fed68105ad4f06bc286b2bcfb932ccfd4465899af81ecc7441e59088f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79333375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b598f10979ecabbbecd2fbeca22124ace9a9ace399cda7e378aae0af918c2c33`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:45:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:45:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:45:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:45:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:45:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:45:52 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:45:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:45:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:49:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:49:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:49:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:49:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:49:23 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:12:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:12:50 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:13:06 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:13:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:13:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:13:06 GMT
WORKDIR /app
# Fri, 08 May 2026 17:13:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:13:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5f818fb7c09d275f57b0be232e3327c598854c2cd8c1af2e5536f47c030109`  
		Last Modified: Fri, 08 May 2026 16:49:31 GMT  
		Size: 3.6 MB (3625695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bde2dbfa2d2a3c95dc2eb8f7e57ce0c5861a36e95ff913cab891df185c56779`  
		Last Modified: Fri, 08 May 2026 16:49:31 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f7ce7672df1bccaf696725c7cf018abd4fcce22df9ddd66674d1d181d1fb1`  
		Last Modified: Fri, 08 May 2026 16:49:31 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c78a34ca66f37347555dd11601a37b28fb5dc7b9164650aef7bbcdc265237d`  
		Last Modified: Fri, 08 May 2026 16:49:32 GMT  
		Size: 14.4 MB (14417249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d49058f5e508fbedf7c1761ed74c3488a1b66aa1c53245df6f5c202bd01e68`  
		Last Modified: Fri, 08 May 2026 16:49:32 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0d59880de31c08bb1c82cab93a0766a728df6e6f0b2f8b018340e1f90e839e`  
		Last Modified: Fri, 08 May 2026 16:49:33 GMT  
		Size: 23.2 MB (23185462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b3fdeafdda5d52745fb055ae2c3da55119fc9058b9c9ac2880f1358ed8790`  
		Last Modified: Fri, 08 May 2026 16:49:33 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179dc4512664e42fc76b4cbd3cb62d559b6534581642050bc82876d631c7be5c`  
		Last Modified: Fri, 08 May 2026 16:49:33 GMT  
		Size: 23.4 KB (23378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7d15ac4f12ca126a295236e4d7d0544b30ba61b18f042c1b2b3c1c5f5c1894`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 33.4 MB (33353595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c445445a600188721e5cd81fe3fc287d738e58cffc77ebe8e25ba5cce6155f86`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88601221afe1744e48943b5c1fe721cb5ac894586745c4a3780ac3f588ad7a`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 1.0 MB (1032700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b04c9c8d07dca7ff58a463258a23075b5124f8dc39586c413c774fdd43ca7`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ec74ff474580cdfb131bba3665bbe4d30f27af1621c5765f8d129184953152`  
		Last Modified: Fri, 08 May 2026 17:13:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:7c6caa805b56d2cf26b35c94546e7ef1d5a5dec144b18729498db946dbcd9c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc0ec7f96942e271b7d7631c3b46d6dbb800d5d898b2c6fe6ebd881faddd386`

```dockerfile
```

-	Layers:
	-	`sha256:030ced0a8be99eea3c9b9fd78f0393f312863b389dc7a53d3d17f94c8431c692`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 2.2 MB (2178442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b33345f3941243a749471efabde80bc10e90cfaea692daa3fe8531fae4a866`  
		Last Modified: Fri, 08 May 2026 17:13:15 GMT  
		Size: 30.6 KB (30631 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:3a37fd68a6042cb82fd1c521b31aef4ca1d26d867c7b9c13d7401784777eeff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80378812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765290965180ecbca7e191081d78c709ff334540dff4504dc828ba8496da13ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:20:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:20:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.5.6
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 19:47:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 19:47:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:52:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:52:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:52:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:52:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:52:48 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 22:31:58 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 22:31:58 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 22:32:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 22:32:37 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 22:32:37 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 22:32:37 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 22:32:37 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 22:32:37 GMT
WORKDIR /app
# Fri, 08 May 2026 22:32:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 22:32:37 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59216db1edcf64b90905df63416f821bfacdba590544dcdb3c340ea538567c`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 3.8 MB (3767095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dbb332183b4f53eb48b10e61f11a67b23c5647a6901cf35be6037e209a0f51`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd758015c67cd7fae70202df89f7e42a01ff424cadf0cd92070805333b28821`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5702960144fbb228318e4c40ca2e9c98158a8c7b9f71390320236bda898ca95`  
		Last Modified: Fri, 08 May 2026 19:53:03 GMT  
		Size: 14.4 MB (14417280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358ab27e77a70ddec9b84d07b8f7d4afdddd40d4273150e0f53f745558ec45e`  
		Last Modified: Fri, 08 May 2026 19:53:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d790c857f23d764dbb55c79e470cb965a5e1400d248610a1b021e5da4b086f`  
		Last Modified: Fri, 08 May 2026 19:53:04 GMT  
		Size: 23.1 MB (23128501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d767ccb38fac4728b8964553352783881ac8482bff309e0e7a49475c1c68d10`  
		Last Modified: Fri, 08 May 2026 19:53:03 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792fe8cb0c39c5be7986dfbc108e720fbe9f5b205a09ea9e786278ca7d2d3b11`  
		Last Modified: Fri, 08 May 2026 19:53:04 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2594f5b2cc2f273332e529c87042778906a76cf847c1bbbfb0afb3a53554b1b5`  
		Last Modified: Fri, 08 May 2026 22:32:56 GMT  
		Size: 34.2 MB (34180303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ac582f80c6a79ddb5212f9a4b1ef780331e87889d7c30fee1b86fc32cdbbc0`  
		Last Modified: Fri, 08 May 2026 22:32:54 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72388f9529399090e5800a46557ae5093e9aeacd27281f855788291ddb37069e`  
		Last Modified: Fri, 08 May 2026 22:32:55 GMT  
		Size: 1.0 MB (1026571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25f9d92287139c4c82a3bac211848cb7a07d6f2aa71ce60801c76d1ef214beb`  
		Last Modified: Fri, 08 May 2026 22:32:54 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a103edbe4df44409e697cd61db384f5cdfb624730e03035597985b13bda6a050`  
		Last Modified: Fri, 08 May 2026 22:32:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:a2d34893c3a2c5fb4746092fe95ba67b9c6f72589696f5b80baa03608007418a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7e76daebcc65909e955a1b3934377e39f50689ddeeae82674e6453d372226d`

```dockerfile
```

-	Layers:
	-	`sha256:10d3d3b85cb1245b350e666620671874ef164948262ea04701a0e063108eab93`  
		Last Modified: Fri, 08 May 2026 22:32:54 GMT  
		Size: 2.2 MB (2178515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01f2d29228b635dc3ef228ece64bda988eaad8b7fa7fcca684415e671fea1d47`  
		Last Modified: Fri, 08 May 2026 22:32:54 GMT  
		Size: 30.7 KB (30715 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:201fb227742eda84c3920f1565e36deec0155cc20c27503627daad12fcc76545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75255480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16f0073e3ec90e47a472eea73f9e48783013f33733be9a1a6b00ca52915ef16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 16 Apr 2026 00:30:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Apr 2026 00:30:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_VERSION=8.5.6
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 21:51:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 21:51:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:52:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 22:52:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:52:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 22:52:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 22:52:16 GMT
CMD ["php" "-a"]
# Mon, 11 May 2026 00:57:44 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 11 May 2026 00:57:45 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 11 May 2026 01:01:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 11 May 2026 01:01:09 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 11 May 2026 01:01:09 GMT
ENV COMPOSER_VERSION=2.9.7
# Mon, 11 May 2026 01:01:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 11 May 2026 01:01:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 11 May 2026 01:01:09 GMT
WORKDIR /app
# Mon, 11 May 2026 01:01:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 May 2026 01:01:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78828518b8b5af0bc74ba3bd169a5c835b32f2a1452a7cd03ad8117a0128165b`  
		Last Modified: Thu, 16 Apr 2026 01:32:16 GMT  
		Size: 3.7 MB (3734242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1c9b4ddefe159b602dd6cdf3bcfff1bf48c922a0f1047bb5402dc2c6c988b`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2a62067bd9660d4987f0df8c18a9ac2818a33d0443ac9c5c806eb7925b9957`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b300791544e0c87f44b461c514787bf7d38ce6f5ad1d34bad34bc1c4782d3f`  
		Last Modified: Fri, 08 May 2026 22:53:24 GMT  
		Size: 14.4 MB (14417294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a331978dcb7855b965e50fa41230cb7f963d49113c956b0e49057d02df423466`  
		Last Modified: Fri, 08 May 2026 22:53:20 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcc286c95072e0d8d8b60f5e888859a51d02c496556840b68e28764a6173ecd`  
		Last Modified: Fri, 08 May 2026 22:53:25 GMT  
		Size: 21.2 MB (21171065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9799a7293faac913a8c2e0ba1a7628be32b2a5ea0e7dd2d76b844e7dfce47ad`  
		Last Modified: Fri, 08 May 2026 22:53:19 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb29c91c88ab86cb8131cb830f2bb49a8ffa2614cedc1c31b69e2c77a975695d`  
		Last Modified: Fri, 08 May 2026 22:53:21 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c65261e37a7d3f9ee21b1c9a9bd5ea90cb040884d3cbfb68f7150999f038c4`  
		Last Modified: Mon, 11 May 2026 01:02:48 GMT  
		Size: 31.3 MB (31299460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4361abd2c1daef5f4b6053d114136340df2419298fa403e48ae9996cced2b79`  
		Last Modified: Mon, 11 May 2026 01:02:44 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4e9a5a183a412aeab22b9bd7a35dbe3ddf399a681f5635e496b9c528121cc1`  
		Last Modified: Mon, 11 May 2026 01:02:44 GMT  
		Size: 1.0 MB (1017615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7681fc7957bbd94bf344f9bd1d7d20f834516ef48691c0bdd749d92ec99fdf2`  
		Last Modified: Mon, 11 May 2026 01:02:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1a9a59e18e5374c9718c827255af5499b066d9dfa2132339e54344c31bf500`  
		Last Modified: Mon, 11 May 2026 01:01:23 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:a328837c6987cad2823792a27dcb579f1e02ff98360d0fdeab5bddf78b5dc12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9b86e0d7a6aeb07175f26c5e648750546e24b473d1dbd38b2478b319c806d2`

```dockerfile
```

-	Layers:
	-	`sha256:1c6aabf396b9034e4e8398ae6b930e4fed5f617e38493e2d4a2c36ce315be2ef`  
		Last Modified: Mon, 11 May 2026 01:02:44 GMT  
		Size: 2.2 MB (2177456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a51e1cba29e30595a491fb536a64e76d162dab7ff375b5848e32937d4358e2`  
		Last Modified: Mon, 11 May 2026 01:02:43 GMT  
		Size: 30.7 KB (30715 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:99863cc662e4b5958234f74730006b98c072da8266d99f0688188349ebee9e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76696548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc203f97b83b8715f9a920330a5325d8ed4a3edcf20ded5cb7f3adfe1a85676`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:41:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 May 2026 23:41:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 05 May 2026 23:41:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 05 May 2026 23:41:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 May 2026 23:41:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 May 2026 23:41:50 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_VERSION=8.5.6
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Tue, 05 May 2026 23:41:50 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:51:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:57:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:57:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:57:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:57:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:57:50 GMT
CMD ["php" "-a"]
# Fri, 08 May 2026 17:14:56 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 08 May 2026 17:14:56 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 08 May 2026 17:15:21 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:15:21 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 08 May 2026 17:15:21 GMT
ENV COMPOSER_VERSION=2.9.7
# Fri, 08 May 2026 17:15:21 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 08 May 2026 17:15:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 17:15:21 GMT
WORKDIR /app
# Fri, 08 May 2026 17:15:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 17:15:21 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e5b23cd7e08583775ca52654782b3eb898be0895811ff074d0b60e2bdabdca`  
		Last Modified: Tue, 05 May 2026 23:50:39 GMT  
		Size: 3.8 MB (3787468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f70f6e1cd967f35b17107285a2dc3920f6cf2d49ba0521083fa3949317113`  
		Last Modified: Tue, 05 May 2026 23:50:38 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cc64825ed6643492e29ef55789e3eb5ed14b413945792b7bc86db5b7c4e70c`  
		Last Modified: Tue, 05 May 2026 23:50:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c70b8b3c23d4b9513ddce760870ee58e711276bb86bdaa74045eafcaf6ae2dc`  
		Last Modified: Fri, 08 May 2026 16:58:06 GMT  
		Size: 14.4 MB (14417277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a38b097c90d256a49ef7bdca140fa8da69c874c923a1dfdd3513846d669f87`  
		Last Modified: Fri, 08 May 2026 16:58:06 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31050156e2ccbc94f9c20b8bcc6638051971128034fb34ad2fdcd18496bf5ec`  
		Last Modified: Fri, 08 May 2026 16:58:07 GMT  
		Size: 21.6 MB (21596857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac685bed84db73eb81d30fa0fa48e67ef3dc625228c72a0ebbc4c8799811eb2`  
		Last Modified: Fri, 08 May 2026 16:58:06 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3171cf62ee41e70bb40f0a98476a7b9f2b6ae9b42d0846873babe98b876b5b60`  
		Last Modified: Fri, 08 May 2026 16:58:07 GMT  
		Size: 23.2 KB (23211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a5b3a5457c384d521a0679d9ad0cfe2efd36175f48ece0b87ed81ff481849`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 32.1 MB (32116524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d567a1a4fa1f8f4985421d4acd4135b3ad52ef380c3f5b44f0291c750cc47c`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82f007fb94228f94c86d027e3598ca58aa08111593d3ca64f403e622325a629`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 1.0 MB (1023820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a42c97b56e0830eede2e46fb214d069afd35578b2e1aee6d27d8af45f256707`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7726d52575774721ccc577d8e854ec56153c76f536b5ef5e8556ab5cbb039ee`  
		Last Modified: Fri, 08 May 2026 17:15:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:40436a63296c0d39fd5eb482c639272e706d6913e9f9203bee69df14cc3a4c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e856da7070e174ec6524a5c1bb2e68da3bac933ad4ae559cc7b63fdbb0b523c1`

```dockerfile
```

-	Layers:
	-	`sha256:97ee1766c209a040ea17e116ebf93e681b06c3c47dcb4f0063bbe36c36e6d312`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 2.2 MB (2177238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4e44f195d88ce08505dfde243f4efde4685113a38414e45fde22d52cd50add6`  
		Last Modified: Fri, 08 May 2026 17:15:37 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json
