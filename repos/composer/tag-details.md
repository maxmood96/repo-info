<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.27`](#composer11027)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.25`](#composer2225)
-	[`composer:2.8`](#composer28)
-	[`composer:2.8.12`](#composer2812)
-	[`composer:latest`](#composerlatest)

## `composer:1`

```console
$ docker pull composer@sha256:5e58c743706812a87500003fdef1c22ef89a24c93263af204ddc526a2a6bb4c2
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
	-	`sha256:5a77d225a4093408ffc09f88e84ceecb9a9237fce71c0c2e253da24dba08370e`  
		Last Modified: Fri, 24 Oct 2025 20:15:47 GMT  
		Size: 33.9 MB (33947738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58861f8d0fbf31403e66960ced7a82c738d6ab53693214ff5f3fc15eaf3d6ae0`  
		Last Modified: Fri, 24 Oct 2025 20:15:44 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428d0474586e75f564c8fb583700920feb4e9cff72c624ba23af2eb21e00953f`  
		Last Modified: Fri, 24 Oct 2025 20:15:44 GMT  
		Size: 735.5 KB (735524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2b7ddc51d0e4faafc87372c0be76bf07826c6b188c8a6abdce072c69fe4c`  
		Last Modified: Fri, 24 Oct 2025 20:15:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e28c9c8dfe1ad11e48c41658e1e3aa78ead447e93a75f771f2b08463a1b21af`  
		Last Modified: Fri, 24 Oct 2025 20:15:44 GMT  
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
		Last Modified: Fri, 24 Oct 2025 22:13:38 GMT  
		Size: 2.2 MB (2171917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88fee191536e0b5f4ac3d663c892026c66bded5f02b82e74fdd35dab855aebcc`  
		Last Modified: Fri, 24 Oct 2025 22:13:39 GMT  
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
	-	`sha256:08f50ecb5de6b2a764828b7e80a55568de1f3e08b01da01bede558990e54249a`  
		Last Modified: Fri, 24 Oct 2025 20:42:45 GMT  
		Size: 33.8 MB (33817685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199fc7d3655041ca726674511a54af7aa7e06c208a7c9fc486684a943e414b28`  
		Last Modified: Fri, 24 Oct 2025 20:42:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329a763f3c1b2a9af24106880b4d662addd61836e8ba1c1d339555de3ee73f9d`  
		Last Modified: Fri, 24 Oct 2025 20:42:42 GMT  
		Size: 736.2 KB (736163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd71e2d9ab85b2f85c2579f108bfb049211c12f23b0e8a2fa7c3ffcfb84d5b55`  
		Last Modified: Fri, 24 Oct 2025 20:42:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb209078f69abb5d309cfc93d9931327093107718ad214a3c38b51dc56dd59f`  
		Last Modified: Fri, 24 Oct 2025 20:42:42 GMT  
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
		Last Modified: Fri, 24 Oct 2025 22:13:42 GMT  
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
	-	`sha256:b496992fd95d278fc615a6d681b3df6fce057c58b56c782d8236767de8085ca4`  
		Last Modified: Fri, 24 Oct 2025 20:50:41 GMT  
		Size: 32.1 MB (32097494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adda9bacbaacaf11314077d9d1f2ad447ec51704363faaca03cc3eaefccfa9a`  
		Last Modified: Fri, 24 Oct 2025 20:50:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad691cdddbcc251fb5123965de8d982c8fdf0539b96accd5e0dd06ab4bc8e62`  
		Last Modified: Fri, 24 Oct 2025 20:50:38 GMT  
		Size: 726.6 KB (726631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3df618c1f1a615a187a5a8f54b9da335dbddd69ec791d1c32be5b7342c5e9`  
		Last Modified: Fri, 24 Oct 2025 20:50:38 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b838b6672c3ea31406ab925fd8b445cfa08369f57c2b4a5b90c51cbe53087bf9`  
		Last Modified: Fri, 24 Oct 2025 20:50:38 GMT  
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
		Last Modified: Fri, 24 Oct 2025 22:13:46 GMT  
		Size: 2.2 MB (2172233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d202613b539ab5cb3e6f61290c58ad176ef5daafe4af103009faa4827863d0`  
		Last Modified: Fri, 24 Oct 2025 22:13:46 GMT  
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
	-	`sha256:c47e0817c1589b3a8c31cfd8f21fcd9d1d5a1bce7621341675d4824d0652be50`  
		Last Modified: Fri, 24 Oct 2025 20:19:21 GMT  
		Size: 34.0 MB (34036569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d1ebc8aa7aaa83d0b7718ebbcc1afadbab8007c29947b3a5ce90c9a9ba5ef4`  
		Last Modified: Fri, 24 Oct 2025 20:19:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608cbc8ecfe727dbd2ede43881a759a4343d037d71cf6bb6638d3bc665889446`  
		Last Modified: Fri, 24 Oct 2025 20:19:17 GMT  
		Size: 735.5 KB (735507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071babbe10a242439c89a9e6ad25c50e8f7dfc4ba73cd4d39f3a72319b317b9`  
		Last Modified: Fri, 24 Oct 2025 20:19:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f90b53632aee8eb5358956bff199a14db4c27d27191d47115ee8792fb44483`  
		Last Modified: Fri, 24 Oct 2025 20:19:17 GMT  
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
		Last Modified: Fri, 24 Oct 2025 22:13:50 GMT  
		Size: 2.2 MB (2172057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b94b1cdb98ebfd7140d88cb296f595e57246ec42cb3a366d1536879d21e13eb`  
		Last Modified: Fri, 24 Oct 2025 22:13:51 GMT  
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
	-	`sha256:836a5d5dc2ba5d6b83f610c968f5f78e537c713046bc3dfc23e1118c481dd21a`  
		Last Modified: Fri, 24 Oct 2025 19:20:45 GMT  
		Size: 34.5 MB (34468602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b7ea9d567b4cf490dd161bf3907e23a29c3d22680cc8bca898abf4e05d1a90`  
		Last Modified: Fri, 24 Oct 2025 19:20:41 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1d5f987256f0839ccbdcdebe7345e065c5e9e2cc80cddcb505b88e03d3a598`  
		Last Modified: Fri, 24 Oct 2025 19:20:41 GMT  
		Size: 747.4 KB (747393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c28bc494b31382832a91c6bf7ce60699575866f4aa870fd2f833d5eea0da9cc`  
		Last Modified: Fri, 24 Oct 2025 19:20:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2de9e6df9ee11c875c4fb5488b02e6f8fc352cb8fb9f4776478e13e1a3a32d0`  
		Last Modified: Fri, 24 Oct 2025 19:20:41 GMT  
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
		Last Modified: Fri, 24 Oct 2025 22:13:55 GMT  
		Size: 2.2 MB (2171705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ab52739d09a0d44bcf8d60ac6468c70f60454a4dd190d164cc71554fd76e5e`  
		Last Modified: Fri, 24 Oct 2025 22:13:56 GMT  
		Size: 31.3 KB (31325 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:c416ed5f2f8f09d0d8c8509687056bf37e8b3718596697fbed8a00c3e4065b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77896026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421fb4400f520cd72bf4465036f9a6731090631cfa151a9551bab73aae6f894c`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:08c541cc61ee10a80b399d52e1f4bb8a5279855a7fa2c9a76b046ab010b008a3`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccbe14cfb5f112f9165213e6c598f4ea32a7c520ab6aa2a8b2e62b24a58478a`  
		Last Modified: Thu, 09 Oct 2025 01:16:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03340f1e3e44fd83f3b7db1acc126ffeb5a590f53bdab6ca579db0ae5fa52f6c`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 20.9 MB (20858704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de31c9e8e61a6c9596dd41c2b70045f4d409bb66963fba6e71103aa5056ea81`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71522eac8e5e3d7e2dbd1df9937339ed30d1ec9b9680938e271a69acdb62839b`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b073119ff38c21d5615a254aaa7d93099fc3d9ffa24ba1014d9a4e26028463`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e998d65137a46960c8059678b90d25f2a77f449a0a44119c66532fb5f8f5f167`  
		Last Modified: Thu, 09 Oct 2025 05:58:29 GMT  
		Size: 742.4 KB (742403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bbd5ac72432bf87c159972d572f1739ff678e1655f14b21a99093998fd43d6`  
		Last Modified: Thu, 09 Oct 2025 05:58:28 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613c29e6ca40c556a4aff54c2d10401c5b940ff3589615473258dc824be6c8a7`  
		Last Modified: Thu, 09 Oct 2025 05:58:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:cc26fff65a01f87cc64e9dd846f89d74ede5e3fb236ceb922614f9b0d3ec66c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd282959229cefd4bf2b7fb6fe6845ed8ac4c32dccfae157f390827fa39dbd0`

```dockerfile
```

-	Layers:
	-	`sha256:838bd75f5cf1f94b6e95ac7430ca27b98b1d63fa61e73b27146412e7a6e5de7a`  
		Last Modified: Thu, 09 Oct 2025 07:13:32 GMT  
		Size: 2.2 MB (2170474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a93244b3dab0b93c5c1716ec6b34e6802d86a7fdcf329c4692361dfafe96a62c`  
		Last Modified: Thu, 09 Oct 2025 07:13:33 GMT  
		Size: 31.4 KB (31398 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:8df8a10715f611da7ce3e4b64a5fc5bdffd080e64b592ef37bfeb00a8cf93336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72046742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9666c55e3f3fb2b6be2f4fce499473aa54ef57d661f9657a2efa8b7667e6c5bf`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:9ffe3756686e8121120603c46e2bcc7c25a6a0c923bdc47741ddd8ac23f7505c`  
		Last Modified: Thu, 09 Oct 2025 12:23:13 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66a307993ff99b5b3658ed178834c47681fdc3296384c58149d6a03f07ef86`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f92261afff37de278981985cbf1b23f5b946658937d6f613c95988742502fc1`  
		Last Modified: Thu, 09 Oct 2025 12:23:11 GMT  
		Size: 19.4 MB (19373788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f739a05185d11834b1e53840782634f634ce0d1eca4746926c47033d6cf1ded8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be024fc29f2390a64fe4d73fb0873a93a6ccb37995d0b252dd9bb174cd1e4895`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8011cdcf4f7bc91f25ad15e332853b7a1c42a076454400c738594f3962209b8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49955161ff3f60e3060e3064936558be7775fe3ee8780e3b391f05a302a87979`  
		Last Modified: Mon, 13 Oct 2025 06:30:16 GMT  
		Size: 31.1 MB (31112421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f659ae5d89daae889e03a88d8619444d53a5725d6a2ce755f2cf115f095c55a7`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5724999b64109398de22747ba6e012d0e9ad3387ad16ffdb7943a53f2fd0a59c`  
		Last Modified: Mon, 13 Oct 2025 06:40:05 GMT  
		Size: 733.1 KB (733138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7ba16217290f4a9dbd9bb19f3fe1d5be094a3e4b9e632bb6c5e55cb6d24f92`  
		Last Modified: Mon, 13 Oct 2025 06:40:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e4688382fc54311ae90c69483d0bf321ef24662a7261511df4948ccb3f5a67`  
		Last Modified: Mon, 13 Oct 2025 06:40:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:e9f0acce903510027d73e1596cb7f3d28635151734e5f592a6af2a39fd32419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b656f946856ddd5749db26af41212893b0824430d08cfb8321a65c29892088`

```dockerfile
```

-	Layers:
	-	`sha256:44e9d220b66fb38026b595318ee86bd1e0c7be0f9a903c821c5d17bf1a66ec7e`  
		Last Modified: Mon, 13 Oct 2025 07:13:37 GMT  
		Size: 2.2 MB (2168741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86da2ed96cd420a8cd2f512457d675e47db04e18f5375e1cf8747b519babd44`  
		Last Modified: Mon, 13 Oct 2025 07:13:38 GMT  
		Size: 31.4 KB (31397 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:26408d88508f4f7cb19ba479978f4635e80dda89d665193eb42b55542d2c7436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73603507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab568f50e9d7c0a246ea3ce15cee6528be46cd6c3de8aa431a198a14fc3e1de3`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:b695282d592a178e4c36aa152fd59e9134e630400a7f212f7414d972457a8035`  
		Last Modified: Thu, 09 Oct 2025 01:06:21 GMT  
		Size: 13.7 MB (13667331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874309b732361867c2db5075f339f7d251d35a1999132dcbd51c4fe56c9f89b`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e822974d38b51bcdf4e8d50473316964925d3354c2f94b653b31f9886cf6a`  
		Last Modified: Thu, 09 Oct 2025 01:06:20 GMT  
		Size: 20.0 MB (19969497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a883aae99b872ee9827b2eaacabac2e42e262e2db3ecbfa459de9906907f78`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4dd335651ea2da6132f7a2def407e03ec362587a03fe3560afdcc27f769573`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 19.9 KB (19874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f5a27fa65467dec23807b65f8edbd31acd8a6a19f0fcfbeafd66e63326096`  
		Last Modified: Thu, 09 Oct 2025 01:06:19 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac75b7b2c1b476a0d8ac230e1cad683ecc1f114063aa0796f12aadff29c06016`  
		Last Modified: Thu, 09 Oct 2025 08:08:19 GMT  
		Size: 738.8 KB (738767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f88ca6b9cba1d8764e1fbb641ddabc71c96313aeadc6777def8c92ccee0034b`  
		Last Modified: Thu, 09 Oct 2025 08:08:18 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59816c81f47bedb9d02df0b3667757e756dcc9c91c55f7de36e3950801f70e3`  
		Last Modified: Thu, 09 Oct 2025 08:08:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:dcc172465f65803e48404584778813d264b0cfc5d742098907b3205dd0e72c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042c9a57e84213e673789fa653a3acb6c9523aefd01dbe422f34091aafa0ab8b`

```dockerfile
```

-	Layers:
	-	`sha256:c117b90ca2d5a440239665a540ac370fdaa697c6c0ffbc7a917938590f1bfeed`  
		Last Modified: Thu, 09 Oct 2025 10:13:50 GMT  
		Size: 2.2 MB (2168529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c0794e0dece018c8ee4067cba4af5748868b849f1ab33f153e325bb35f7d26`  
		Last Modified: Thu, 09 Oct 2025 10:13:51 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:5e58c743706812a87500003fdef1c22ef89a24c93263af204ddc526a2a6bb4c2
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
	-	`sha256:5a77d225a4093408ffc09f88e84ceecb9a9237fce71c0c2e253da24dba08370e`  
		Last Modified: Fri, 24 Oct 2025 20:15:47 GMT  
		Size: 33.9 MB (33947738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58861f8d0fbf31403e66960ced7a82c738d6ab53693214ff5f3fc15eaf3d6ae0`  
		Last Modified: Fri, 24 Oct 2025 20:15:44 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428d0474586e75f564c8fb583700920feb4e9cff72c624ba23af2eb21e00953f`  
		Last Modified: Fri, 24 Oct 2025 20:15:44 GMT  
		Size: 735.5 KB (735524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2b7ddc51d0e4faafc87372c0be76bf07826c6b188c8a6abdce072c69fe4c`  
		Last Modified: Fri, 24 Oct 2025 20:15:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e28c9c8dfe1ad11e48c41658e1e3aa78ead447e93a75f771f2b08463a1b21af`  
		Last Modified: Fri, 24 Oct 2025 20:15:44 GMT  
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
		Last Modified: Fri, 24 Oct 2025 22:13:38 GMT  
		Size: 2.2 MB (2171917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88fee191536e0b5f4ac3d663c892026c66bded5f02b82e74fdd35dab855aebcc`  
		Last Modified: Fri, 24 Oct 2025 22:13:39 GMT  
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
	-	`sha256:08f50ecb5de6b2a764828b7e80a55568de1f3e08b01da01bede558990e54249a`  
		Last Modified: Fri, 24 Oct 2025 20:42:45 GMT  
		Size: 33.8 MB (33817685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199fc7d3655041ca726674511a54af7aa7e06c208a7c9fc486684a943e414b28`  
		Last Modified: Fri, 24 Oct 2025 20:42:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329a763f3c1b2a9af24106880b4d662addd61836e8ba1c1d339555de3ee73f9d`  
		Last Modified: Fri, 24 Oct 2025 20:42:42 GMT  
		Size: 736.2 KB (736163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd71e2d9ab85b2f85c2579f108bfb049211c12f23b0e8a2fa7c3ffcfb84d5b55`  
		Last Modified: Fri, 24 Oct 2025 20:42:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb209078f69abb5d309cfc93d9931327093107718ad214a3c38b51dc56dd59f`  
		Last Modified: Fri, 24 Oct 2025 20:42:42 GMT  
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
		Last Modified: Fri, 24 Oct 2025 22:13:42 GMT  
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
	-	`sha256:b496992fd95d278fc615a6d681b3df6fce057c58b56c782d8236767de8085ca4`  
		Last Modified: Fri, 24 Oct 2025 20:50:41 GMT  
		Size: 32.1 MB (32097494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adda9bacbaacaf11314077d9d1f2ad447ec51704363faaca03cc3eaefccfa9a`  
		Last Modified: Fri, 24 Oct 2025 20:50:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad691cdddbcc251fb5123965de8d982c8fdf0539b96accd5e0dd06ab4bc8e62`  
		Last Modified: Fri, 24 Oct 2025 20:50:38 GMT  
		Size: 726.6 KB (726631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3df618c1f1a615a187a5a8f54b9da335dbddd69ec791d1c32be5b7342c5e9`  
		Last Modified: Fri, 24 Oct 2025 20:50:38 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b838b6672c3ea31406ab925fd8b445cfa08369f57c2b4a5b90c51cbe53087bf9`  
		Last Modified: Fri, 24 Oct 2025 20:50:38 GMT  
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
		Last Modified: Fri, 24 Oct 2025 22:13:46 GMT  
		Size: 2.2 MB (2172233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d202613b539ab5cb3e6f61290c58ad176ef5daafe4af103009faa4827863d0`  
		Last Modified: Fri, 24 Oct 2025 22:13:46 GMT  
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
	-	`sha256:c47e0817c1589b3a8c31cfd8f21fcd9d1d5a1bce7621341675d4824d0652be50`  
		Last Modified: Fri, 24 Oct 2025 20:19:21 GMT  
		Size: 34.0 MB (34036569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d1ebc8aa7aaa83d0b7718ebbcc1afadbab8007c29947b3a5ce90c9a9ba5ef4`  
		Last Modified: Fri, 24 Oct 2025 20:19:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608cbc8ecfe727dbd2ede43881a759a4343d037d71cf6bb6638d3bc665889446`  
		Last Modified: Fri, 24 Oct 2025 20:19:17 GMT  
		Size: 735.5 KB (735507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071babbe10a242439c89a9e6ad25c50e8f7dfc4ba73cd4d39f3a72319b317b9`  
		Last Modified: Fri, 24 Oct 2025 20:19:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f90b53632aee8eb5358956bff199a14db4c27d27191d47115ee8792fb44483`  
		Last Modified: Fri, 24 Oct 2025 20:19:17 GMT  
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
		Last Modified: Fri, 24 Oct 2025 22:13:50 GMT  
		Size: 2.2 MB (2172057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b94b1cdb98ebfd7140d88cb296f595e57246ec42cb3a366d1536879d21e13eb`  
		Last Modified: Fri, 24 Oct 2025 22:13:51 GMT  
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
	-	`sha256:836a5d5dc2ba5d6b83f610c968f5f78e537c713046bc3dfc23e1118c481dd21a`  
		Last Modified: Fri, 24 Oct 2025 19:20:45 GMT  
		Size: 34.5 MB (34468602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b7ea9d567b4cf490dd161bf3907e23a29c3d22680cc8bca898abf4e05d1a90`  
		Last Modified: Fri, 24 Oct 2025 19:20:41 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1d5f987256f0839ccbdcdebe7345e065c5e9e2cc80cddcb505b88e03d3a598`  
		Last Modified: Fri, 24 Oct 2025 19:20:41 GMT  
		Size: 747.4 KB (747393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c28bc494b31382832a91c6bf7ce60699575866f4aa870fd2f833d5eea0da9cc`  
		Last Modified: Fri, 24 Oct 2025 19:20:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2de9e6df9ee11c875c4fb5488b02e6f8fc352cb8fb9f4776478e13e1a3a32d0`  
		Last Modified: Fri, 24 Oct 2025 19:20:41 GMT  
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
		Last Modified: Fri, 24 Oct 2025 22:13:55 GMT  
		Size: 2.2 MB (2171705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ab52739d09a0d44bcf8d60ac6468c70f60454a4dd190d164cc71554fd76e5e`  
		Last Modified: Fri, 24 Oct 2025 22:13:56 GMT  
		Size: 31.3 KB (31325 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:c416ed5f2f8f09d0d8c8509687056bf37e8b3718596697fbed8a00c3e4065b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77896026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421fb4400f520cd72bf4465036f9a6731090631cfa151a9551bab73aae6f894c`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:08c541cc61ee10a80b399d52e1f4bb8a5279855a7fa2c9a76b046ab010b008a3`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccbe14cfb5f112f9165213e6c598f4ea32a7c520ab6aa2a8b2e62b24a58478a`  
		Last Modified: Thu, 09 Oct 2025 01:16:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03340f1e3e44fd83f3b7db1acc126ffeb5a590f53bdab6ca579db0ae5fa52f6c`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 20.9 MB (20858704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de31c9e8e61a6c9596dd41c2b70045f4d409bb66963fba6e71103aa5056ea81`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71522eac8e5e3d7e2dbd1df9937339ed30d1ec9b9680938e271a69acdb62839b`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b073119ff38c21d5615a254aaa7d93099fc3d9ffa24ba1014d9a4e26028463`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e998d65137a46960c8059678b90d25f2a77f449a0a44119c66532fb5f8f5f167`  
		Last Modified: Thu, 09 Oct 2025 05:58:29 GMT  
		Size: 742.4 KB (742403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bbd5ac72432bf87c159972d572f1739ff678e1655f14b21a99093998fd43d6`  
		Last Modified: Thu, 09 Oct 2025 05:58:28 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613c29e6ca40c556a4aff54c2d10401c5b940ff3589615473258dc824be6c8a7`  
		Last Modified: Thu, 09 Oct 2025 05:58:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:cc26fff65a01f87cc64e9dd846f89d74ede5e3fb236ceb922614f9b0d3ec66c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd282959229cefd4bf2b7fb6fe6845ed8ac4c32dccfae157f390827fa39dbd0`

```dockerfile
```

-	Layers:
	-	`sha256:838bd75f5cf1f94b6e95ac7430ca27b98b1d63fa61e73b27146412e7a6e5de7a`  
		Last Modified: Thu, 09 Oct 2025 07:13:32 GMT  
		Size: 2.2 MB (2170474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a93244b3dab0b93c5c1716ec6b34e6802d86a7fdcf329c4692361dfafe96a62c`  
		Last Modified: Thu, 09 Oct 2025 07:13:33 GMT  
		Size: 31.4 KB (31398 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:8df8a10715f611da7ce3e4b64a5fc5bdffd080e64b592ef37bfeb00a8cf93336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72046742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9666c55e3f3fb2b6be2f4fce499473aa54ef57d661f9657a2efa8b7667e6c5bf`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:9ffe3756686e8121120603c46e2bcc7c25a6a0c923bdc47741ddd8ac23f7505c`  
		Last Modified: Thu, 09 Oct 2025 12:23:13 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66a307993ff99b5b3658ed178834c47681fdc3296384c58149d6a03f07ef86`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f92261afff37de278981985cbf1b23f5b946658937d6f613c95988742502fc1`  
		Last Modified: Thu, 09 Oct 2025 12:23:11 GMT  
		Size: 19.4 MB (19373788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f739a05185d11834b1e53840782634f634ce0d1eca4746926c47033d6cf1ded8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be024fc29f2390a64fe4d73fb0873a93a6ccb37995d0b252dd9bb174cd1e4895`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8011cdcf4f7bc91f25ad15e332853b7a1c42a076454400c738594f3962209b8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49955161ff3f60e3060e3064936558be7775fe3ee8780e3b391f05a302a87979`  
		Last Modified: Mon, 13 Oct 2025 06:30:16 GMT  
		Size: 31.1 MB (31112421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f659ae5d89daae889e03a88d8619444d53a5725d6a2ce755f2cf115f095c55a7`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5724999b64109398de22747ba6e012d0e9ad3387ad16ffdb7943a53f2fd0a59c`  
		Last Modified: Mon, 13 Oct 2025 06:40:05 GMT  
		Size: 733.1 KB (733138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7ba16217290f4a9dbd9bb19f3fe1d5be094a3e4b9e632bb6c5e55cb6d24f92`  
		Last Modified: Mon, 13 Oct 2025 06:40:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e4688382fc54311ae90c69483d0bf321ef24662a7261511df4948ccb3f5a67`  
		Last Modified: Mon, 13 Oct 2025 06:40:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:e9f0acce903510027d73e1596cb7f3d28635151734e5f592a6af2a39fd32419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b656f946856ddd5749db26af41212893b0824430d08cfb8321a65c29892088`

```dockerfile
```

-	Layers:
	-	`sha256:44e9d220b66fb38026b595318ee86bd1e0c7be0f9a903c821c5d17bf1a66ec7e`  
		Last Modified: Mon, 13 Oct 2025 07:13:37 GMT  
		Size: 2.2 MB (2168741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86da2ed96cd420a8cd2f512457d675e47db04e18f5375e1cf8747b519babd44`  
		Last Modified: Mon, 13 Oct 2025 07:13:38 GMT  
		Size: 31.4 KB (31397 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:26408d88508f4f7cb19ba479978f4635e80dda89d665193eb42b55542d2c7436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73603507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab568f50e9d7c0a246ea3ce15cee6528be46cd6c3de8aa431a198a14fc3e1de3`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:b695282d592a178e4c36aa152fd59e9134e630400a7f212f7414d972457a8035`  
		Last Modified: Thu, 09 Oct 2025 01:06:21 GMT  
		Size: 13.7 MB (13667331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874309b732361867c2db5075f339f7d251d35a1999132dcbd51c4fe56c9f89b`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e822974d38b51bcdf4e8d50473316964925d3354c2f94b653b31f9886cf6a`  
		Last Modified: Thu, 09 Oct 2025 01:06:20 GMT  
		Size: 20.0 MB (19969497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a883aae99b872ee9827b2eaacabac2e42e262e2db3ecbfa459de9906907f78`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4dd335651ea2da6132f7a2def407e03ec362587a03fe3560afdcc27f769573`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 19.9 KB (19874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f5a27fa65467dec23807b65f8edbd31acd8a6a19f0fcfbeafd66e63326096`  
		Last Modified: Thu, 09 Oct 2025 01:06:19 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac75b7b2c1b476a0d8ac230e1cad683ecc1f114063aa0796f12aadff29c06016`  
		Last Modified: Thu, 09 Oct 2025 08:08:19 GMT  
		Size: 738.8 KB (738767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f88ca6b9cba1d8764e1fbb641ddabc71c96313aeadc6777def8c92ccee0034b`  
		Last Modified: Thu, 09 Oct 2025 08:08:18 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59816c81f47bedb9d02df0b3667757e756dcc9c91c55f7de36e3950801f70e3`  
		Last Modified: Thu, 09 Oct 2025 08:08:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:dcc172465f65803e48404584778813d264b0cfc5d742098907b3205dd0e72c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042c9a57e84213e673789fa653a3acb6c9523aefd01dbe422f34091aafa0ab8b`

```dockerfile
```

-	Layers:
	-	`sha256:c117b90ca2d5a440239665a540ac370fdaa697c6c0ffbc7a917938590f1bfeed`  
		Last Modified: Thu, 09 Oct 2025 10:13:50 GMT  
		Size: 2.2 MB (2168529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c0794e0dece018c8ee4067cba4af5748868b849f1ab33f153e325bb35f7d26`  
		Last Modified: Thu, 09 Oct 2025 10:13:51 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:5e58c743706812a87500003fdef1c22ef89a24c93263af204ddc526a2a6bb4c2
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
	-	`sha256:5a77d225a4093408ffc09f88e84ceecb9a9237fce71c0c2e253da24dba08370e`  
		Last Modified: Fri, 24 Oct 2025 20:15:47 GMT  
		Size: 33.9 MB (33947738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58861f8d0fbf31403e66960ced7a82c738d6ab53693214ff5f3fc15eaf3d6ae0`  
		Last Modified: Fri, 24 Oct 2025 20:15:44 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428d0474586e75f564c8fb583700920feb4e9cff72c624ba23af2eb21e00953f`  
		Last Modified: Fri, 24 Oct 2025 20:15:44 GMT  
		Size: 735.5 KB (735524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf2b7ddc51d0e4faafc87372c0be76bf07826c6b188c8a6abdce072c69fe4c`  
		Last Modified: Fri, 24 Oct 2025 20:15:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e28c9c8dfe1ad11e48c41658e1e3aa78ead447e93a75f771f2b08463a1b21af`  
		Last Modified: Fri, 24 Oct 2025 20:15:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

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
		Last Modified: Fri, 24 Oct 2025 22:13:38 GMT  
		Size: 2.2 MB (2171917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88fee191536e0b5f4ac3d663c892026c66bded5f02b82e74fdd35dab855aebcc`  
		Last Modified: Fri, 24 Oct 2025 22:13:39 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v6

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
	-	`sha256:08f50ecb5de6b2a764828b7e80a55568de1f3e08b01da01bede558990e54249a`  
		Last Modified: Fri, 24 Oct 2025 20:42:45 GMT  
		Size: 33.8 MB (33817685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199fc7d3655041ca726674511a54af7aa7e06c208a7c9fc486684a943e414b28`  
		Last Modified: Fri, 24 Oct 2025 20:42:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329a763f3c1b2a9af24106880b4d662addd61836e8ba1c1d339555de3ee73f9d`  
		Last Modified: Fri, 24 Oct 2025 20:42:42 GMT  
		Size: 736.2 KB (736163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd71e2d9ab85b2f85c2579f108bfb049211c12f23b0e8a2fa7c3ffcfb84d5b55`  
		Last Modified: Fri, 24 Oct 2025 20:42:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb209078f69abb5d309cfc93d9931327093107718ad214a3c38b51dc56dd59f`  
		Last Modified: Fri, 24 Oct 2025 20:42:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

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
		Last Modified: Fri, 24 Oct 2025 22:13:42 GMT  
		Size: 31.2 KB (31239 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v7

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
	-	`sha256:b496992fd95d278fc615a6d681b3df6fce057c58b56c782d8236767de8085ca4`  
		Last Modified: Fri, 24 Oct 2025 20:50:41 GMT  
		Size: 32.1 MB (32097494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adda9bacbaacaf11314077d9d1f2ad447ec51704363faaca03cc3eaefccfa9a`  
		Last Modified: Fri, 24 Oct 2025 20:50:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad691cdddbcc251fb5123965de8d982c8fdf0539b96accd5e0dd06ab4bc8e62`  
		Last Modified: Fri, 24 Oct 2025 20:50:38 GMT  
		Size: 726.6 KB (726631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3df618c1f1a615a187a5a8f54b9da335dbddd69ec791d1c32be5b7342c5e9`  
		Last Modified: Fri, 24 Oct 2025 20:50:38 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b838b6672c3ea31406ab925fd8b445cfa08369f57c2b4a5b90c51cbe53087bf9`  
		Last Modified: Fri, 24 Oct 2025 20:50:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

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
		Last Modified: Fri, 24 Oct 2025 22:13:46 GMT  
		Size: 2.2 MB (2172233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8d202613b539ab5cb3e6f61290c58ad176ef5daafe4af103009faa4827863d0`  
		Last Modified: Fri, 24 Oct 2025 22:13:46 GMT  
		Size: 31.5 KB (31453 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm64 variant v8

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
	-	`sha256:c47e0817c1589b3a8c31cfd8f21fcd9d1d5a1bce7621341675d4824d0652be50`  
		Last Modified: Fri, 24 Oct 2025 20:19:21 GMT  
		Size: 34.0 MB (34036569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d1ebc8aa7aaa83d0b7718ebbcc1afadbab8007c29947b3a5ce90c9a9ba5ef4`  
		Last Modified: Fri, 24 Oct 2025 20:19:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608cbc8ecfe727dbd2ede43881a759a4343d037d71cf6bb6638d3bc665889446`  
		Last Modified: Fri, 24 Oct 2025 20:19:17 GMT  
		Size: 735.5 KB (735507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071babbe10a242439c89a9e6ad25c50e8f7dfc4ba73cd4d39f3a72319b317b9`  
		Last Modified: Fri, 24 Oct 2025 20:19:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f90b53632aee8eb5358956bff199a14db4c27d27191d47115ee8792fb44483`  
		Last Modified: Fri, 24 Oct 2025 20:19:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

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
		Last Modified: Fri, 24 Oct 2025 22:13:50 GMT  
		Size: 2.2 MB (2172057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b94b1cdb98ebfd7140d88cb296f595e57246ec42cb3a366d1536879d21e13eb`  
		Last Modified: Fri, 24 Oct 2025 22:13:51 GMT  
		Size: 31.5 KB (31478 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; 386

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
	-	`sha256:836a5d5dc2ba5d6b83f610c968f5f78e537c713046bc3dfc23e1118c481dd21a`  
		Last Modified: Fri, 24 Oct 2025 19:20:45 GMT  
		Size: 34.5 MB (34468602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b7ea9d567b4cf490dd161bf3907e23a29c3d22680cc8bca898abf4e05d1a90`  
		Last Modified: Fri, 24 Oct 2025 19:20:41 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1d5f987256f0839ccbdcdebe7345e065c5e9e2cc80cddcb505b88e03d3a598`  
		Last Modified: Fri, 24 Oct 2025 19:20:41 GMT  
		Size: 747.4 KB (747393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c28bc494b31382832a91c6bf7ce60699575866f4aa870fd2f833d5eea0da9cc`  
		Last Modified: Fri, 24 Oct 2025 19:20:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2de9e6df9ee11c875c4fb5488b02e6f8fc352cb8fb9f4776478e13e1a3a32d0`  
		Last Modified: Fri, 24 Oct 2025 19:20:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

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
		Last Modified: Fri, 24 Oct 2025 22:13:55 GMT  
		Size: 2.2 MB (2171705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ab52739d09a0d44bcf8d60ac6468c70f60454a4dd190d164cc71554fd76e5e`  
		Last Modified: Fri, 24 Oct 2025 22:13:56 GMT  
		Size: 31.3 KB (31325 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; ppc64le

```console
$ docker pull composer@sha256:c416ed5f2f8f09d0d8c8509687056bf37e8b3718596697fbed8a00c3e4065b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77896026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421fb4400f520cd72bf4465036f9a6731090631cfa151a9551bab73aae6f894c`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:08c541cc61ee10a80b399d52e1f4bb8a5279855a7fa2c9a76b046ab010b008a3`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccbe14cfb5f112f9165213e6c598f4ea32a7c520ab6aa2a8b2e62b24a58478a`  
		Last Modified: Thu, 09 Oct 2025 01:16:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03340f1e3e44fd83f3b7db1acc126ffeb5a590f53bdab6ca579db0ae5fa52f6c`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 20.9 MB (20858704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de31c9e8e61a6c9596dd41c2b70045f4d409bb66963fba6e71103aa5056ea81`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71522eac8e5e3d7e2dbd1df9937339ed30d1ec9b9680938e271a69acdb62839b`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b073119ff38c21d5615a254aaa7d93099fc3d9ffa24ba1014d9a4e26028463`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e998d65137a46960c8059678b90d25f2a77f449a0a44119c66532fb5f8f5f167`  
		Last Modified: Thu, 09 Oct 2025 05:58:29 GMT  
		Size: 742.4 KB (742403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bbd5ac72432bf87c159972d572f1739ff678e1655f14b21a99093998fd43d6`  
		Last Modified: Thu, 09 Oct 2025 05:58:28 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613c29e6ca40c556a4aff54c2d10401c5b940ff3589615473258dc824be6c8a7`  
		Last Modified: Thu, 09 Oct 2025 05:58:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:cc26fff65a01f87cc64e9dd846f89d74ede5e3fb236ceb922614f9b0d3ec66c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd282959229cefd4bf2b7fb6fe6845ed8ac4c32dccfae157f390827fa39dbd0`

```dockerfile
```

-	Layers:
	-	`sha256:838bd75f5cf1f94b6e95ac7430ca27b98b1d63fa61e73b27146412e7a6e5de7a`  
		Last Modified: Thu, 09 Oct 2025 07:13:32 GMT  
		Size: 2.2 MB (2170474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a93244b3dab0b93c5c1716ec6b34e6802d86a7fdcf329c4692361dfafe96a62c`  
		Last Modified: Thu, 09 Oct 2025 07:13:33 GMT  
		Size: 31.4 KB (31398 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; riscv64

```console
$ docker pull composer@sha256:8df8a10715f611da7ce3e4b64a5fc5bdffd080e64b592ef37bfeb00a8cf93336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72046742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9666c55e3f3fb2b6be2f4fce499473aa54ef57d661f9657a2efa8b7667e6c5bf`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:9ffe3756686e8121120603c46e2bcc7c25a6a0c923bdc47741ddd8ac23f7505c`  
		Last Modified: Thu, 09 Oct 2025 12:23:13 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66a307993ff99b5b3658ed178834c47681fdc3296384c58149d6a03f07ef86`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f92261afff37de278981985cbf1b23f5b946658937d6f613c95988742502fc1`  
		Last Modified: Thu, 09 Oct 2025 12:23:11 GMT  
		Size: 19.4 MB (19373788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f739a05185d11834b1e53840782634f634ce0d1eca4746926c47033d6cf1ded8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be024fc29f2390a64fe4d73fb0873a93a6ccb37995d0b252dd9bb174cd1e4895`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8011cdcf4f7bc91f25ad15e332853b7a1c42a076454400c738594f3962209b8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49955161ff3f60e3060e3064936558be7775fe3ee8780e3b391f05a302a87979`  
		Last Modified: Mon, 13 Oct 2025 06:30:16 GMT  
		Size: 31.1 MB (31112421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f659ae5d89daae889e03a88d8619444d53a5725d6a2ce755f2cf115f095c55a7`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5724999b64109398de22747ba6e012d0e9ad3387ad16ffdb7943a53f2fd0a59c`  
		Last Modified: Mon, 13 Oct 2025 06:40:05 GMT  
		Size: 733.1 KB (733138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7ba16217290f4a9dbd9bb19f3fe1d5be094a3e4b9e632bb6c5e55cb6d24f92`  
		Last Modified: Mon, 13 Oct 2025 06:40:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e4688382fc54311ae90c69483d0bf321ef24662a7261511df4948ccb3f5a67`  
		Last Modified: Mon, 13 Oct 2025 06:40:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:e9f0acce903510027d73e1596cb7f3d28635151734e5f592a6af2a39fd32419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b656f946856ddd5749db26af41212893b0824430d08cfb8321a65c29892088`

```dockerfile
```

-	Layers:
	-	`sha256:44e9d220b66fb38026b595318ee86bd1e0c7be0f9a903c821c5d17bf1a66ec7e`  
		Last Modified: Mon, 13 Oct 2025 07:13:37 GMT  
		Size: 2.2 MB (2168741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86da2ed96cd420a8cd2f512457d675e47db04e18f5375e1cf8747b519babd44`  
		Last Modified: Mon, 13 Oct 2025 07:13:38 GMT  
		Size: 31.4 KB (31397 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; s390x

```console
$ docker pull composer@sha256:26408d88508f4f7cb19ba479978f4635e80dda89d665193eb42b55542d2c7436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73603507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab568f50e9d7c0a246ea3ce15cee6528be46cd6c3de8aa431a198a14fc3e1de3`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:b695282d592a178e4c36aa152fd59e9134e630400a7f212f7414d972457a8035`  
		Last Modified: Thu, 09 Oct 2025 01:06:21 GMT  
		Size: 13.7 MB (13667331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874309b732361867c2db5075f339f7d251d35a1999132dcbd51c4fe56c9f89b`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e822974d38b51bcdf4e8d50473316964925d3354c2f94b653b31f9886cf6a`  
		Last Modified: Thu, 09 Oct 2025 01:06:20 GMT  
		Size: 20.0 MB (19969497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a883aae99b872ee9827b2eaacabac2e42e262e2db3ecbfa459de9906907f78`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4dd335651ea2da6132f7a2def407e03ec362587a03fe3560afdcc27f769573`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 19.9 KB (19874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f5a27fa65467dec23807b65f8edbd31acd8a6a19f0fcfbeafd66e63326096`  
		Last Modified: Thu, 09 Oct 2025 01:06:19 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac75b7b2c1b476a0d8ac230e1cad683ecc1f114063aa0796f12aadff29c06016`  
		Last Modified: Thu, 09 Oct 2025 08:08:19 GMT  
		Size: 738.8 KB (738767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f88ca6b9cba1d8764e1fbb641ddabc71c96313aeadc6777def8c92ccee0034b`  
		Last Modified: Thu, 09 Oct 2025 08:08:18 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59816c81f47bedb9d02df0b3667757e756dcc9c91c55f7de36e3950801f70e3`  
		Last Modified: Thu, 09 Oct 2025 08:08:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:dcc172465f65803e48404584778813d264b0cfc5d742098907b3205dd0e72c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042c9a57e84213e673789fa653a3acb6c9523aefd01dbe422f34091aafa0ab8b`

```dockerfile
```

-	Layers:
	-	`sha256:c117b90ca2d5a440239665a540ac370fdaa697c6c0ffbc7a917938590f1bfeed`  
		Last Modified: Thu, 09 Oct 2025 10:13:50 GMT  
		Size: 2.2 MB (2168529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c0794e0dece018c8ee4067cba4af5748868b849f1ab33f153e325bb35f7d26`  
		Last Modified: Thu, 09 Oct 2025 10:13:51 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:24f538daf6d1e33e0859033ca2b50955b68fa69f7f3d2d1cba9a51b6cfdcf606
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
$ docker pull composer@sha256:0d264a0f1e5be23ba363447768df7b30c33d542711ea12e37770ed7b13bf4eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75854318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805d739ba8da4383b57f6a4598ebda6df35143471694058b52abb2f86b2a5fc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:d9c585fc0858fb182174b42e967fd91eba8f0c5fe46c0b8474a14a97ba00f9b2`  
		Last Modified: Fri, 24 Oct 2025 20:19:32 GMT  
		Size: 33.9 MB (33947500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554aa2fcd32d16117f10c09421ba2fefb8c6b62265e19c47aeff94a9a50deec8`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f21bf3d69502cdd5dd65e973522f62173298ce2c1cf733ba7570f1abbd3da8`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 974.2 KB (974204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e3b4ee80e6d8bd5ea2e0a6ee500ea0d4d914f4446a9eef230e6700da8ed8bc`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fa2707690f38f404a79ec9eca786e5f68c185bcaf824c7c6d9536839799046`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:c4e94577e3a79c265c3b2a19f013354fef208adf26f0e0b1ebf47de3299a3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300f9917da97bf0e9648cc7b1c32bdc1789a60247c2cefd1d2c0fa0b03d73e75`

```dockerfile
```

-	Layers:
	-	`sha256:f2dba5f611989bd14c743453e097ff55c3c4f04f5419790f3b03ebf0d0d0f708`  
		Last Modified: Fri, 24 Oct 2025 22:14:06 GMT  
		Size: 2.2 MB (2173415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c869f9ec9d58986a24b0a14f8d5d09e6e4cca043718593fc4d7f08cbf310879`  
		Last Modified: Fri, 24 Oct 2025 22:14:07 GMT  
		Size: 31.7 KB (31655 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:9204b9a7a9df81968c806f2b0ef4c9d8d8dbe51a43797588433645283b229763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73494680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e3b4574492ba4221f5bd32b26fcca99fdf67fcaaf16fb5f7b911e3ef00f9a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:677016e4a05cd9d7caa1de3ce5e214bb0f617ca04ddbe3ef67db12b83329c7b3`  
		Last Modified: Fri, 24 Oct 2025 20:42:36 GMT  
		Size: 33.8 MB (33817487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a74822dc5a1fff34f9cd0fc67c8071e7ecc6f1c05d7d960c05a30227ca7480`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32a2a61df1c0cf8de1f5d45fb41e404e4d47a7e0899c82d04d59f3170950fc`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 974.2 KB (974168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bb94e5ae85307dce2a049277d148fc7b9a6387ea8b247ba6861a3744de1226`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20bd3e81699adb6432acb1e3cdbd1bff47ab55f32a5650efff530ee60571771`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:9343c2cda94fd20ada22030f5317069866d7b954df251513f7035211ebb2043c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0858cebf9952fd446c0059e4836ad9bae408b15609d537ae27514ca4176ef99d`

```dockerfile
```

-	Layers:
	-	`sha256:124be63b687d3a7df1473e92ea5c6127c5e773e521e4afcf9f69219aed73d2e5`  
		Last Modified: Fri, 24 Oct 2025 22:14:11 GMT  
		Size: 31.5 KB (31546 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:11ef398e69d694688e37308b9e5080fed84e7c2eb3946d65f9b73947a1d1e9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70289253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306418dfd2976851ded90c22f09ab197aa633e78ce6f338f00e2b9cc5625dfb4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:e134e14d05100f43b1098cfe83dac4d1878e0011c90ebea8acb37fa0a034d56b`  
		Last Modified: Fri, 24 Oct 2025 20:50:30 GMT  
		Size: 32.1 MB (32097758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f37f8bb32b419173ac9421577528609a45422416c2fff8e18dc40cf26213b5a`  
		Last Modified: Fri, 24 Oct 2025 20:50:28 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e07052daa224ff10334146da5f8f819196b02cec75c0c697f74311642a71ba`  
		Last Modified: Fri, 24 Oct 2025 20:50:29 GMT  
		Size: 964.9 KB (964860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331e7b0382791466edbeebc26238c70f8de5b5ac274927a704e94f6df404e43e`  
		Last Modified: Fri, 24 Oct 2025 20:50:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168e3fc3448c5dddeb7cd2161898c590b6e0e2578d3cda47fed790dbc5c6e7d1`  
		Last Modified: Fri, 24 Oct 2025 20:50:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:d6fe4ee5ea5bca1674b479111c3508c6a073e4c2ff0f2f0d32128d61536654da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46df73f1ab448a2b152e0b688d749d065da3a1708443b9a519d3463fc3e92e2`

```dockerfile
```

-	Layers:
	-	`sha256:2fd2d9b3e5ae585128615abee4b9f96aaf8d7086ad7ae7847ff06bda446b1833`  
		Last Modified: Fri, 24 Oct 2025 22:14:14 GMT  
		Size: 2.2 MB (2173739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5182947cb87494b1e77c08965e298a8b09163adf95e7a1320c7e822e8c9c3db4`  
		Last Modified: Fri, 24 Oct 2025 22:14:15 GMT  
		Size: 31.8 KB (31761 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:cc2fd435c5dd57485421bc19c3e9226c29417f8065c00dcef2b2e361090f3c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75830669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96f81949775bd3e6004fd0cf0fc55607a2da42e6b9b26002e13a4b623d4994e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:413b61f8cb24ed8752e8cda1bdaef2720fa5a54ee5a47aedefbbdd3961a07c52`  
		Last Modified: Fri, 24 Oct 2025 20:19:12 GMT  
		Size: 34.0 MB (34036686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e877f4e26235bcebeb5785c987aafe66e1fb9b1e46cf1b31486e3f8d8895f2d`  
		Last Modified: Fri, 24 Oct 2025 20:19:06 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c02e3b72fe4e2884dc77540236af7c7ffc6d17f0279a2343e1134e04a48e40`  
		Last Modified: Fri, 24 Oct 2025 20:19:06 GMT  
		Size: 973.8 KB (973838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5275291d5a13a86a4848ebf143e11d59a8a3fa2d4beea8f15499913ba77d10`  
		Last Modified: Fri, 24 Oct 2025 20:19:06 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1974defaeb30f0d935ea55aa0c03c0b1de7093bf188fe4c3feb4522ffb682b`  
		Last Modified: Fri, 24 Oct 2025 20:19:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:fdb14d3db55f7fcff98bd67c452d6b8ead015d1ab9eaf75733f814144b8f5b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f060eb14b7cab778cc76b4e75dee2379b4d1f103236776a11ceeea19704e292`

```dockerfile
```

-	Layers:
	-	`sha256:f69adc6fe0d49623ae5e79ccb6c02183265f418c07f5533d89065ee043120d95`  
		Last Modified: Fri, 24 Oct 2025 22:14:18 GMT  
		Size: 2.2 MB (2173567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f52a286937f1b728814e34ee3fd26ebc7da67aa2f5adab8473787bfc2e9a147`  
		Last Modified: Fri, 24 Oct 2025 22:14:19 GMT  
		Size: 31.8 KB (31789 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:089d747cdd596158dbb2d452bba33226ef7292f92ac5d09c44ffd343ae12b731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76796681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc29e7b010e01ab322670b822facc07e95152e99e917b4001127510506e872dd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:35e85a8d646dc17d692c7f4cdcc4e046f87a0e099d6d44d870b7de3c100dbdd1`  
		Last Modified: Fri, 24 Oct 2025 19:20:40 GMT  
		Size: 34.5 MB (34468366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7722d6eade39bd814b4fa8e278fd98603c7e6dad8fd33cb15c33917af5b6971f`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3381ca837f505d8a1fbded8daa098e03586f7511456078d4038c51c54c2ea83`  
		Last Modified: Fri, 24 Oct 2025 19:20:37 GMT  
		Size: 988.2 KB (988165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2927bd6eda562337b286187b19d702a1a9f557709d6064a8c2d728de3a4b96ee`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49a2d382dfa044f0f8dd680d2676d662e4b527dad096f9a0e8604b025c13d73`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:06a9a7469d1a02aaeac3f00d918558b958dca4f918289c723e807fcde1b99fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f7debe4722e173e422e260956be67adcbf2bbd9c567ad64f95096695dec5ed`

```dockerfile
```

-	Layers:
	-	`sha256:2b69994a499c47d3aed365b77ec99dc221049da9ca33e7f72fe2ba67daea7b09`  
		Last Modified: Fri, 24 Oct 2025 22:14:24 GMT  
		Size: 2.2 MB (2173198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce7ed4d16291f6dc0e7fae788e7678c1b917b04e3ec46eaeb5e9916670f31ff5`  
		Last Modified: Fri, 24 Oct 2025 22:14:24 GMT  
		Size: 31.6 KB (31619 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:7ab8f18c7690e96c4b2c0f98ca57e42441737139252d67b4213aa405cfadaeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78134372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf72e7a7216358538fcfc4866b29268353f4cb0bf3c5f8cd1e41b25e84f7ca00`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:08c541cc61ee10a80b399d52e1f4bb8a5279855a7fa2c9a76b046ab010b008a3`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccbe14cfb5f112f9165213e6c598f4ea32a7c520ab6aa2a8b2e62b24a58478a`  
		Last Modified: Thu, 09 Oct 2025 01:16:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03340f1e3e44fd83f3b7db1acc126ffeb5a590f53bdab6ca579db0ae5fa52f6c`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 20.9 MB (20858704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de31c9e8e61a6c9596dd41c2b70045f4d409bb66963fba6e71103aa5056ea81`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71522eac8e5e3d7e2dbd1df9937339ed30d1ec9b9680938e271a69acdb62839b`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b073119ff38c21d5615a254aaa7d93099fc3d9ffa24ba1014d9a4e26028463`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7069cbe03c650f9a782b558ea0c7b6eecf0b31471b705b90de9c985fc0584766`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 980.7 KB (980738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c9dfb2c75ab180a836d1a22b7399619b9d8544f6da246eac510b495b3be44b`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b721d4ea96a39181ad8693b4a8d88fb1845f909261dbf8a034cd63e16768dd99`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:11e9c625adf643934ca29589b3d294bb86103370ed72644386527ce5e5e3df3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05059bd123cffb6b560400732d38d0b86867c15100aba79c3223f2169599616d`

```dockerfile
```

-	Layers:
	-	`sha256:765e6400901500e644e76705796817786597f0dba11e9dca3548e9d777025dae`  
		Last Modified: Thu, 09 Oct 2025 07:13:45 GMT  
		Size: 2.2 MB (2171978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c016add85054c3cb7f2c16c4beb8f8dcc5bffc8fb5f7477d3a53ac2a593a2b85`  
		Last Modified: Thu, 09 Oct 2025 07:13:46 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:d9454c3c75d02d24624d2d6741cbf61c1e896287265625736f0b7891039fafff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72285489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adec28a4a63fd7cc8cd54b34ddc6d53a178b2da922c574247c327397407ef119`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:9ffe3756686e8121120603c46e2bcc7c25a6a0c923bdc47741ddd8ac23f7505c`  
		Last Modified: Thu, 09 Oct 2025 12:23:13 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66a307993ff99b5b3658ed178834c47681fdc3296384c58149d6a03f07ef86`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f92261afff37de278981985cbf1b23f5b946658937d6f613c95988742502fc1`  
		Last Modified: Thu, 09 Oct 2025 12:23:11 GMT  
		Size: 19.4 MB (19373788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f739a05185d11834b1e53840782634f634ce0d1eca4746926c47033d6cf1ded8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be024fc29f2390a64fe4d73fb0873a93a6ccb37995d0b252dd9bb174cd1e4895`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8011cdcf4f7bc91f25ad15e332853b7a1c42a076454400c738594f3962209b8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49955161ff3f60e3060e3064936558be7775fe3ee8780e3b391f05a302a87979`  
		Last Modified: Mon, 13 Oct 2025 06:30:16 GMT  
		Size: 31.1 MB (31112421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f659ae5d89daae889e03a88d8619444d53a5725d6a2ce755f2cf115f095c55a7`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0947ceefd087c282c2cbd108a398739e126987182016113328633d16f6ef0e41`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 971.9 KB (971874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2a9e4844376d9dbbd6e414a8788a4d4985d6d092f498d319b5153812ef0450`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b667872090bb1420eafe05f6e33ce208d93749d7699c74ea351a9aa875a0049`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:662e721ba6de44ed649520b09fe9f80302e5cd1802270931cb9eab71954ace21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6c7c6b16c8e6358c55869f649ef0545603f856581b0e13395e2da4d38c3bf2`

```dockerfile
```

-	Layers:
	-	`sha256:8aae531408035419e447caef87ce80412c07e31343314679ba4856567d8d78eb`  
		Last Modified: Mon, 13 Oct 2025 07:13:49 GMT  
		Size: 2.2 MB (2170245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c72ebd04f61bd95eefa1e9eed6a74683833f088e8007e539cc0c33298f8e582d`  
		Last Modified: Mon, 13 Oct 2025 07:13:50 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:05595a53f3002bbd2ba712d1885651be62400b12bd14119f40191f7ae3aef015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73841920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502f45c09a39566b91313513de05acd6f1490e3c336a2c7fd24cac084ddf44dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:b695282d592a178e4c36aa152fd59e9134e630400a7f212f7414d972457a8035`  
		Last Modified: Thu, 09 Oct 2025 01:06:21 GMT  
		Size: 13.7 MB (13667331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874309b732361867c2db5075f339f7d251d35a1999132dcbd51c4fe56c9f89b`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e822974d38b51bcdf4e8d50473316964925d3354c2f94b653b31f9886cf6a`  
		Last Modified: Thu, 09 Oct 2025 01:06:20 GMT  
		Size: 20.0 MB (19969497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a883aae99b872ee9827b2eaacabac2e42e262e2db3ecbfa459de9906907f78`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4dd335651ea2da6132f7a2def407e03ec362587a03fe3560afdcc27f769573`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 19.9 KB (19874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f5a27fa65467dec23807b65f8edbd31acd8a6a19f0fcfbeafd66e63326096`  
		Last Modified: Thu, 09 Oct 2025 01:06:19 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b3763f27effcdcc686b244b630554f55656ad8f43c1abc3b8c8d516d707acd`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 977.2 KB (977171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e53287954018bc60f63bea842b06e6a30715c50a10e7021e3bad0e4ea802725`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3888304b21042155b83dc5bbfb55b5a62ecaa2401bd061ba507b2c2bfd3fa7d`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:a1dd369e5929c064afc2005875b7732ba60490562cbaf47c857940c7b8e6bc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ea6c568cc3c0b5074248845f5f93c92bb29da444b2c7be0d1529405b9ec94`

```dockerfile
```

-	Layers:
	-	`sha256:a19650be819af7eb6ff88e79275de8056eac5a7f961dda45b1832e83ffd71794`  
		Last Modified: Thu, 09 Oct 2025 10:14:06 GMT  
		Size: 2.2 MB (2170027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136b3d48a9b0c3a1e679291b71cf94a1e413d4692a883077c8c2fd3fc32b15cc`  
		Last Modified: Thu, 09 Oct 2025 10:14:07 GMT  
		Size: 31.7 KB (31654 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:33aaceb2b06b41064f20f5ca1e5477c86ed8622af3c4e2e5c01593b2843962a8
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
$ docker pull composer@sha256:8c7d5eca6feea12539e2e108ec71461dfa74c5686c9916eaa55bdd4ec27226b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75700688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c127fcd46b1bc5147b6ba0dde34ca1f8969021da6993636490aea060aed3aac`
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
	-	`sha256:5a77d225a4093408ffc09f88e84ceecb9a9237fce71c0c2e253da24dba08370e`  
		Last Modified: Fri, 24 Oct 2025 20:15:47 GMT  
		Size: 33.9 MB (33947738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58861f8d0fbf31403e66960ced7a82c738d6ab53693214ff5f3fc15eaf3d6ae0`  
		Last Modified: Fri, 24 Oct 2025 20:15:44 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c291376f53e14cd4c0e9528b0b9e3dc5ccdbe3548f92960940facf6d363728`  
		Last Modified: Fri, 24 Oct 2025 20:19:18 GMT  
		Size: 820.3 KB (820334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fa3f5e2308293091dfa85ad522ed3c2eb8c5fcb68f327b72fea26b3fe9d29e`  
		Last Modified: Fri, 24 Oct 2025 20:19:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49322550fc27692b200e32365e5bf3262ce94d26d0bea2c87cd2d9ccef90917`  
		Last Modified: Fri, 24 Oct 2025 20:19:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:72aca128f00a7e75e1626beb7c259a034ca982243a29d930fb694385d2f3c334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c0ac5f58a37f62f90f45bb5f163409e6add17cff755cd177185af36f9ff0dd`

```dockerfile
```

-	Layers:
	-	`sha256:5e864baab4e081fd7c36861475337f03dab1469abcb1c4f674a8951a72f00923`  
		Last Modified: Fri, 24 Oct 2025 22:14:27 GMT  
		Size: 2.2 MB (2172821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1064260eec93edc28d27a56300c1e6ee7dcf55fb7e58bd738977d2c059ad433c`  
		Last Modified: Fri, 24 Oct 2025 22:14:28 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:f4652a14cb90179d8e35933ecda8422e7e1abb55e0cd629c0f7d9e11c40bc080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73341130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41464fd22f87a916531cfe5e2f875cf3a5c1b2a2e97ef2c1b4cfc839e5360e0e`
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
	-	`sha256:0eba8d1d9af1ebec8f8b2ffb5b13a97e27a05a44a1eb4b5f75b3a140e7597122`  
		Last Modified: Fri, 24 Oct 2025 20:42:40 GMT  
		Size: 33.8 MB (33817626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14353f3125e394685a10261bccb9e542e450ad41f181cbc5a9d47aea3f1a1c58`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a89a9ed252aad7e58c8e15584f109cd420e3f74b0ba4f25f2fafe91ebc23e73`  
		Last Modified: Fri, 24 Oct 2025 20:42:33 GMT  
		Size: 820.5 KB (820480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e107a163902663efe344bc656cdc22f7b29d3203a8a6ca51e027b714f3a22b26`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224ffd73570aeb30fca2663938ebfaf5def9aab8ffb44003a90d30b4d5a8d098`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:18d73bc5f4ccf45d4a9e923f47a5a3904f1928695d9a245a2d09b66dc82bff35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502337aac3f33740cf9beb2e575878a472145cf0164a56c9eaad8cede5d82ab2`

```dockerfile
```

-	Layers:
	-	`sha256:e6f79fe95846cd92ae41281f79727cd39b23504461849c68fb1c928388224b9b`  
		Last Modified: Fri, 24 Oct 2025 22:14:31 GMT  
		Size: 30.9 KB (30926 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:032cf3f2e8ed3df34ad4397601d1731071b6c0808e86ba33abfbbfeb9a85dd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70134782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738eecccaf61a7eefa54ef68628fa428388268648f99df970a09bdd61f9c76a1`
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
	-	`sha256:1ac6f93bdf659fa5dda94cf2902862b30b30cd76018296e8dfdea390346031a7`  
		Last Modified: Fri, 24 Oct 2025 23:01:35 GMT  
		Size: 32.1 MB (32097299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c31c93ca002cd3db3e231cfcdd840b08fd983f9ae87e96b46323eebda203e9`  
		Last Modified: Fri, 24 Oct 2025 20:50:34 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19bcce18ef8aa673f3ccab7c5d1c783fbe5cfb076a2352c2ba02c0dac6ff158`  
		Last Modified: Fri, 24 Oct 2025 20:50:34 GMT  
		Size: 810.9 KB (810851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cc008cc0c13026576984ecc92c0ad7488f154443a350c09afd7fcbe58d01ca`  
		Last Modified: Fri, 24 Oct 2025 20:50:34 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613564a5f7f109bfabaaa1de6fb7cd468c39c36c3b45e22ab76631ad6f3ab862`  
		Last Modified: Fri, 24 Oct 2025 20:50:35 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:bb1d3d6db2dd737cb587eaa5acd0f439ee91a19df517e81b891a775ec9c074a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01059bf22abe0cd7ee79617534c594886d81db1a3f81083aed9b2e78147d8274`

```dockerfile
```

-	Layers:
	-	`sha256:48335a007ba3ca92d9340fd30a282248a3fa1e3d1d6e26b661734abacf04c358`  
		Last Modified: Fri, 24 Oct 2025 22:14:35 GMT  
		Size: 2.2 MB (2173129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eba3797bee9f1b682bcf444ff22d09f75c751488ce7b7e45b4ec481f7b23dc8`  
		Last Modified: Fri, 24 Oct 2025 22:14:35 GMT  
		Size: 31.1 KB (31142 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:c24332ef55e5df089821fc6f1b9dba558c23fce860e7ce2b623aeded5dcd2b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75676805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f0793e6c6aed9b7490166dbb12b3ed29676b0c91cf5d540f8ae6ecb0102582`
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
	-	`sha256:aab2209a4ff4ee851bd30909b385d15e2c50b0d0b09d9729235b0642e82d4987`  
		Last Modified: Fri, 24 Oct 2025 21:32:42 GMT  
		Size: 34.0 MB (34036622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb9cfe1d1abe423df0a7581d3ced0d933a433c82a92dcb36438aa9445b29fb`  
		Last Modified: Fri, 24 Oct 2025 21:05:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163b466f76902d70f10b6de0a78780630b59787b46fb7beb284e0702fe81809b`  
		Last Modified: Fri, 24 Oct 2025 21:05:22 GMT  
		Size: 820.0 KB (820041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2d92d01215d7f31b7984437c69d51664ca300be0a0ad6045a46230b310d4c`  
		Last Modified: Fri, 24 Oct 2025 21:05:21 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e692cbced7026e66c2e1501bca019dc5b938ea85c5862059c8d415db5bc7ba`  
		Last Modified: Fri, 24 Oct 2025 21:05:21 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:5d0b32f5992d78931b51a445fab1b65f9ef84943ea180598d0fc89acda580bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60228bed543753de586b82247bf43cb0944b931e46e0c1e247c9ec30c8f2f099`

```dockerfile
```

-	Layers:
	-	`sha256:47ff30fa7bb372be0b2d83065dcfb07733973816c2ba541969c551a17f024f86`  
		Last Modified: Fri, 24 Oct 2025 22:14:39 GMT  
		Size: 2.2 MB (2172949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89acb599a1276a742bbe37f87f538c8ae943d566e025acd77acc3f6d7bf12c40`  
		Last Modified: Fri, 24 Oct 2025 22:14:40 GMT  
		Size: 31.2 KB (31161 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:aa8556b722a999def625d37906496be7756accaf5f215a35126195273d969cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76642740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397a1b96a2818ea4f63400439fddb6f93018fd1171c1e2af4b0412c14cef2009`
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
	-	`sha256:a1aec3092e295871b9448c78589e5342430d2db8265ce2092c8e039d2a0d64be`  
		Last Modified: Fri, 24 Oct 2025 23:02:42 GMT  
		Size: 34.5 MB (34468328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7a6241d7332f0cda454bc814e36f96b734382b816ae9328bfb4eaa8a83ea4d`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e0fdaeba1611f85c8e2cb7f62db468b01ca91aa2b777b2709c4e1691a36e91`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 834.3 KB (834260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772d0676385d39f41c28cf0dc361eda1f0a0e148c2203caac0e54ee22587761d`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9994da28bb3c96709b3c34d041c3ddeb6fef45f67212e292b008dc03b9068f67`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:790d068b6f12ad879eef5d40bfa70a98977e82d1f89de172d56d89fe5609d187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6a7c10c16c6072ba5b5628c2b16b9f16131fdd54fa4de5461f0a565f4a01d7`

```dockerfile
```

-	Layers:
	-	`sha256:b4d1f3e77b15c85da3421de21224757ec321732bb650112a4c7815d1fac17814`  
		Last Modified: Fri, 24 Oct 2025 22:14:43 GMT  
		Size: 2.2 MB (2172614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7237cfc7181d7e4202d07f90eaec326743549d09e59621d42494f7346a2ba8bd`  
		Last Modified: Fri, 24 Oct 2025 22:14:44 GMT  
		Size: 31.0 KB (31026 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:267d948789f1e8ba32cd6c41d2d7c2e7f47b99ff376989cfec7d686580aa7db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77980496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a844aaec8a96a60c5fdc3fbb39e4112ecd4d81e9c30d44f6ab529364b233833`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:08c541cc61ee10a80b399d52e1f4bb8a5279855a7fa2c9a76b046ab010b008a3`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccbe14cfb5f112f9165213e6c598f4ea32a7c520ab6aa2a8b2e62b24a58478a`  
		Last Modified: Thu, 09 Oct 2025 01:16:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03340f1e3e44fd83f3b7db1acc126ffeb5a590f53bdab6ca579db0ae5fa52f6c`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 20.9 MB (20858704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de31c9e8e61a6c9596dd41c2b70045f4d409bb66963fba6e71103aa5056ea81`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71522eac8e5e3d7e2dbd1df9937339ed30d1ec9b9680938e271a69acdb62839b`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b073119ff38c21d5615a254aaa7d93099fc3d9ffa24ba1014d9a4e26028463`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd01430c925e9bd74329f8c7402b67430ebd0095258f6391d5871865462ab45f`  
		Last Modified: Thu, 09 Oct 2025 05:57:27 GMT  
		Size: 826.9 KB (826863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde899e55f9456e44648f217589cdd59dea02a52ff0559202e0b126d0af8906d`  
		Last Modified: Thu, 09 Oct 2025 05:57:27 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31207cd067ce60336a44109182e5fd7c56a5e49782e4279d6da7042776c941e9`  
		Last Modified: Thu, 09 Oct 2025 05:57:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:0c145e84e5a67b29c59c9876f199eb3cdbe4174dd7a1a19a4e1c2ce05bf15567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5b716ecda48acad1ac905c3c3a5e753f362ed822fb6302eaea2b7fd19b487e`

```dockerfile
```

-	Layers:
	-	`sha256:4c5b326fc1172de42accb95fd5eb0f14dfdaed8af440a3c57ef3550af56628c9`  
		Last Modified: Thu, 09 Oct 2025 07:13:52 GMT  
		Size: 2.2 MB (2171372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91da73e4223b24a5c15a122491267b152c515232ed5594db74a1db1c66cf6138`  
		Last Modified: Thu, 09 Oct 2025 07:13:53 GMT  
		Size: 31.1 KB (31088 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:7327310627d6b7d4e8caafcd67ae31c6c93c6efcdd2c1f2d9baa3919f6933b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72131616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6980c3ff13a9f02e427f6ba874939a94d99d4dfb200a39d1f0e3a9d9cac3269b`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:9ffe3756686e8121120603c46e2bcc7c25a6a0c923bdc47741ddd8ac23f7505c`  
		Last Modified: Thu, 09 Oct 2025 12:23:13 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66a307993ff99b5b3658ed178834c47681fdc3296384c58149d6a03f07ef86`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f92261afff37de278981985cbf1b23f5b946658937d6f613c95988742502fc1`  
		Last Modified: Thu, 09 Oct 2025 12:23:11 GMT  
		Size: 19.4 MB (19373788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f739a05185d11834b1e53840782634f634ce0d1eca4746926c47033d6cf1ded8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be024fc29f2390a64fe4d73fb0873a93a6ccb37995d0b252dd9bb174cd1e4895`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8011cdcf4f7bc91f25ad15e332853b7a1c42a076454400c738594f3962209b8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49955161ff3f60e3060e3064936558be7775fe3ee8780e3b391f05a302a87979`  
		Last Modified: Mon, 13 Oct 2025 06:30:16 GMT  
		Size: 31.1 MB (31112421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f659ae5d89daae889e03a88d8619444d53a5725d6a2ce755f2cf115f095c55a7`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53efee6d3e96229253c3a7725735789bf4a70b9a1330437f621da92eff26cf2`  
		Last Modified: Mon, 13 Oct 2025 06:35:07 GMT  
		Size: 818.0 KB (818001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5879ecbff9e99be6f4d887eb042e4c14f2bfe151121663593cb91a690f5704e`  
		Last Modified: Mon, 13 Oct 2025 06:35:07 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb37fdc8a5665d9ebd473e8cbc864f88305bb2237b89358c206142c3fba8973`  
		Last Modified: Mon, 13 Oct 2025 06:34:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:b2f3b28fde2e1acb5c6daa4e33a1aad229ea857c426174e9d2fcdacf4fac1fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06193ec23089bc241dbbebc222be01177af691b99b495986be6c29b48672740`

```dockerfile
```

-	Layers:
	-	`sha256:35a1e26915edb1bacf502fd9bbab1b2aa6acf7eb54c746f0819d073867b96028`  
		Last Modified: Mon, 13 Oct 2025 07:13:56 GMT  
		Size: 2.2 MB (2169639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87dfd1fa998c3011fb0a530c011f8eaef40b52d80446c4b11b26a2ebd1627ab4`  
		Last Modified: Mon, 13 Oct 2025 07:13:57 GMT  
		Size: 31.1 KB (31088 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:1613f51eb6e97ebe0e044364b0efc85dee0a15f781e16f868c4da86b8598eca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73688072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa9b56fa76a4083186af4f23bc2142eba8efaa43417ec7a273d17b0b99989c3`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:b695282d592a178e4c36aa152fd59e9134e630400a7f212f7414d972457a8035`  
		Last Modified: Thu, 09 Oct 2025 01:06:21 GMT  
		Size: 13.7 MB (13667331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874309b732361867c2db5075f339f7d251d35a1999132dcbd51c4fe56c9f89b`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e822974d38b51bcdf4e8d50473316964925d3354c2f94b653b31f9886cf6a`  
		Last Modified: Thu, 09 Oct 2025 01:06:20 GMT  
		Size: 20.0 MB (19969497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a883aae99b872ee9827b2eaacabac2e42e262e2db3ecbfa459de9906907f78`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4dd335651ea2da6132f7a2def407e03ec362587a03fe3560afdcc27f769573`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 19.9 KB (19874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f5a27fa65467dec23807b65f8edbd31acd8a6a19f0fcfbeafd66e63326096`  
		Last Modified: Thu, 09 Oct 2025 01:06:19 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f07303d79642f1f6fb404a8362ed6ae9eddc69cd78578e51091cb475493090`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 823.3 KB (823321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2253d23f87d556dbd49a9d60e5599181400a82b367969b3240ebfec9ed62e295`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055da3fa01337a487323a552025f2674b3813f2ae6ad386ea8de35aa22f6361d`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:02d56363e74dcb994393bb3f8b0c29e018e3b0dd1b94972fae8ebe9d0c11c8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0215206443c671d7a23d81c0bfa3a6935208899dc688605e06b3892f2ab44551`

```dockerfile
```

-	Layers:
	-	`sha256:561cc1a52b71fb0fa9ed6c468b6f2da2b033fd505534e1a90ec2206346fa38ed`  
		Last Modified: Thu, 09 Oct 2025 10:14:14 GMT  
		Size: 2.2 MB (2169433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5fc09a5ef7167a9597751e5d1f89d97f7ed736db1e45b06e009d9a11fc2aa89`  
		Last Modified: Thu, 09 Oct 2025 10:14:15 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.25`

```console
$ docker pull composer@sha256:33aaceb2b06b41064f20f5ca1e5477c86ed8622af3c4e2e5c01593b2843962a8
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
$ docker pull composer@sha256:8c7d5eca6feea12539e2e108ec71461dfa74c5686c9916eaa55bdd4ec27226b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75700688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c127fcd46b1bc5147b6ba0dde34ca1f8969021da6993636490aea060aed3aac`
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
	-	`sha256:5a77d225a4093408ffc09f88e84ceecb9a9237fce71c0c2e253da24dba08370e`  
		Last Modified: Fri, 24 Oct 2025 20:15:47 GMT  
		Size: 33.9 MB (33947738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58861f8d0fbf31403e66960ced7a82c738d6ab53693214ff5f3fc15eaf3d6ae0`  
		Last Modified: Fri, 24 Oct 2025 20:15:44 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c291376f53e14cd4c0e9528b0b9e3dc5ccdbe3548f92960940facf6d363728`  
		Last Modified: Fri, 24 Oct 2025 20:19:18 GMT  
		Size: 820.3 KB (820334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fa3f5e2308293091dfa85ad522ed3c2eb8c5fcb68f327b72fea26b3fe9d29e`  
		Last Modified: Fri, 24 Oct 2025 20:19:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49322550fc27692b200e32365e5bf3262ce94d26d0bea2c87cd2d9ccef90917`  
		Last Modified: Fri, 24 Oct 2025 20:19:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:72aca128f00a7e75e1626beb7c259a034ca982243a29d930fb694385d2f3c334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c0ac5f58a37f62f90f45bb5f163409e6add17cff755cd177185af36f9ff0dd`

```dockerfile
```

-	Layers:
	-	`sha256:5e864baab4e081fd7c36861475337f03dab1469abcb1c4f674a8951a72f00923`  
		Last Modified: Fri, 24 Oct 2025 22:14:27 GMT  
		Size: 2.2 MB (2172821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1064260eec93edc28d27a56300c1e6ee7dcf55fb7e58bd738977d2c059ad433c`  
		Last Modified: Fri, 24 Oct 2025 22:14:28 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v6

```console
$ docker pull composer@sha256:f4652a14cb90179d8e35933ecda8422e7e1abb55e0cd629c0f7d9e11c40bc080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73341130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41464fd22f87a916531cfe5e2f875cf3a5c1b2a2e97ef2c1b4cfc839e5360e0e`
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
	-	`sha256:0eba8d1d9af1ebec8f8b2ffb5b13a97e27a05a44a1eb4b5f75b3a140e7597122`  
		Last Modified: Fri, 24 Oct 2025 20:42:40 GMT  
		Size: 33.8 MB (33817626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14353f3125e394685a10261bccb9e542e450ad41f181cbc5a9d47aea3f1a1c58`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a89a9ed252aad7e58c8e15584f109cd420e3f74b0ba4f25f2fafe91ebc23e73`  
		Last Modified: Fri, 24 Oct 2025 20:42:33 GMT  
		Size: 820.5 KB (820480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e107a163902663efe344bc656cdc22f7b29d3203a8a6ca51e027b714f3a22b26`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224ffd73570aeb30fca2663938ebfaf5def9aab8ffb44003a90d30b4d5a8d098`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:18d73bc5f4ccf45d4a9e923f47a5a3904f1928695d9a245a2d09b66dc82bff35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502337aac3f33740cf9beb2e575878a472145cf0164a56c9eaad8cede5d82ab2`

```dockerfile
```

-	Layers:
	-	`sha256:e6f79fe95846cd92ae41281f79727cd39b23504461849c68fb1c928388224b9b`  
		Last Modified: Fri, 24 Oct 2025 22:14:31 GMT  
		Size: 30.9 KB (30926 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v7

```console
$ docker pull composer@sha256:032cf3f2e8ed3df34ad4397601d1731071b6c0808e86ba33abfbbfeb9a85dd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70134782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738eecccaf61a7eefa54ef68628fa428388268648f99df970a09bdd61f9c76a1`
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
	-	`sha256:1ac6f93bdf659fa5dda94cf2902862b30b30cd76018296e8dfdea390346031a7`  
		Last Modified: Fri, 24 Oct 2025 23:01:35 GMT  
		Size: 32.1 MB (32097299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c31c93ca002cd3db3e231cfcdd840b08fd983f9ae87e96b46323eebda203e9`  
		Last Modified: Fri, 24 Oct 2025 20:50:34 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19bcce18ef8aa673f3ccab7c5d1c783fbe5cfb076a2352c2ba02c0dac6ff158`  
		Last Modified: Fri, 24 Oct 2025 20:50:34 GMT  
		Size: 810.9 KB (810851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cc008cc0c13026576984ecc92c0ad7488f154443a350c09afd7fcbe58d01ca`  
		Last Modified: Fri, 24 Oct 2025 20:50:34 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613564a5f7f109bfabaaa1de6fb7cd468c39c36c3b45e22ab76631ad6f3ab862`  
		Last Modified: Fri, 24 Oct 2025 20:50:35 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:bb1d3d6db2dd737cb587eaa5acd0f439ee91a19df517e81b891a775ec9c074a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01059bf22abe0cd7ee79617534c594886d81db1a3f81083aed9b2e78147d8274`

```dockerfile
```

-	Layers:
	-	`sha256:48335a007ba3ca92d9340fd30a282248a3fa1e3d1d6e26b661734abacf04c358`  
		Last Modified: Fri, 24 Oct 2025 22:14:35 GMT  
		Size: 2.2 MB (2173129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eba3797bee9f1b682bcf444ff22d09f75c751488ce7b7e45b4ec481f7b23dc8`  
		Last Modified: Fri, 24 Oct 2025 22:14:35 GMT  
		Size: 31.1 KB (31142 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:c24332ef55e5df089821fc6f1b9dba558c23fce860e7ce2b623aeded5dcd2b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75676805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f0793e6c6aed9b7490166dbb12b3ed29676b0c91cf5d540f8ae6ecb0102582`
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
	-	`sha256:aab2209a4ff4ee851bd30909b385d15e2c50b0d0b09d9729235b0642e82d4987`  
		Last Modified: Fri, 24 Oct 2025 21:32:42 GMT  
		Size: 34.0 MB (34036622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb9cfe1d1abe423df0a7581d3ced0d933a433c82a92dcb36438aa9445b29fb`  
		Last Modified: Fri, 24 Oct 2025 21:05:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163b466f76902d70f10b6de0a78780630b59787b46fb7beb284e0702fe81809b`  
		Last Modified: Fri, 24 Oct 2025 21:05:22 GMT  
		Size: 820.0 KB (820041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2d92d01215d7f31b7984437c69d51664ca300be0a0ad6045a46230b310d4c`  
		Last Modified: Fri, 24 Oct 2025 21:05:21 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e692cbced7026e66c2e1501bca019dc5b938ea85c5862059c8d415db5bc7ba`  
		Last Modified: Fri, 24 Oct 2025 21:05:21 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:5d0b32f5992d78931b51a445fab1b65f9ef84943ea180598d0fc89acda580bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60228bed543753de586b82247bf43cb0944b931e46e0c1e247c9ec30c8f2f099`

```dockerfile
```

-	Layers:
	-	`sha256:47ff30fa7bb372be0b2d83065dcfb07733973816c2ba541969c551a17f024f86`  
		Last Modified: Fri, 24 Oct 2025 22:14:39 GMT  
		Size: 2.2 MB (2172949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89acb599a1276a742bbe37f87f538c8ae943d566e025acd77acc3f6d7bf12c40`  
		Last Modified: Fri, 24 Oct 2025 22:14:40 GMT  
		Size: 31.2 KB (31161 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; 386

```console
$ docker pull composer@sha256:aa8556b722a999def625d37906496be7756accaf5f215a35126195273d969cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76642740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397a1b96a2818ea4f63400439fddb6f93018fd1171c1e2af4b0412c14cef2009`
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
	-	`sha256:a1aec3092e295871b9448c78589e5342430d2db8265ce2092c8e039d2a0d64be`  
		Last Modified: Fri, 24 Oct 2025 23:02:42 GMT  
		Size: 34.5 MB (34468328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7a6241d7332f0cda454bc814e36f96b734382b816ae9328bfb4eaa8a83ea4d`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e0fdaeba1611f85c8e2cb7f62db468b01ca91aa2b777b2709c4e1691a36e91`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 834.3 KB (834260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772d0676385d39f41c28cf0dc361eda1f0a0e148c2203caac0e54ee22587761d`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9994da28bb3c96709b3c34d041c3ddeb6fef45f67212e292b008dc03b9068f67`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:790d068b6f12ad879eef5d40bfa70a98977e82d1f89de172d56d89fe5609d187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6a7c10c16c6072ba5b5628c2b16b9f16131fdd54fa4de5461f0a565f4a01d7`

```dockerfile
```

-	Layers:
	-	`sha256:b4d1f3e77b15c85da3421de21224757ec321732bb650112a4c7815d1fac17814`  
		Last Modified: Fri, 24 Oct 2025 22:14:43 GMT  
		Size: 2.2 MB (2172614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7237cfc7181d7e4202d07f90eaec326743549d09e59621d42494f7346a2ba8bd`  
		Last Modified: Fri, 24 Oct 2025 22:14:44 GMT  
		Size: 31.0 KB (31026 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; ppc64le

```console
$ docker pull composer@sha256:267d948789f1e8ba32cd6c41d2d7c2e7f47b99ff376989cfec7d686580aa7db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77980496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a844aaec8a96a60c5fdc3fbb39e4112ecd4d81e9c30d44f6ab529364b233833`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:08c541cc61ee10a80b399d52e1f4bb8a5279855a7fa2c9a76b046ab010b008a3`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccbe14cfb5f112f9165213e6c598f4ea32a7c520ab6aa2a8b2e62b24a58478a`  
		Last Modified: Thu, 09 Oct 2025 01:16:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03340f1e3e44fd83f3b7db1acc126ffeb5a590f53bdab6ca579db0ae5fa52f6c`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 20.9 MB (20858704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de31c9e8e61a6c9596dd41c2b70045f4d409bb66963fba6e71103aa5056ea81`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71522eac8e5e3d7e2dbd1df9937339ed30d1ec9b9680938e271a69acdb62839b`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b073119ff38c21d5615a254aaa7d93099fc3d9ffa24ba1014d9a4e26028463`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd01430c925e9bd74329f8c7402b67430ebd0095258f6391d5871865462ab45f`  
		Last Modified: Thu, 09 Oct 2025 05:57:27 GMT  
		Size: 826.9 KB (826863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde899e55f9456e44648f217589cdd59dea02a52ff0559202e0b126d0af8906d`  
		Last Modified: Thu, 09 Oct 2025 05:57:27 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31207cd067ce60336a44109182e5fd7c56a5e49782e4279d6da7042776c941e9`  
		Last Modified: Thu, 09 Oct 2025 05:57:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:0c145e84e5a67b29c59c9876f199eb3cdbe4174dd7a1a19a4e1c2ce05bf15567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5b716ecda48acad1ac905c3c3a5e753f362ed822fb6302eaea2b7fd19b487e`

```dockerfile
```

-	Layers:
	-	`sha256:4c5b326fc1172de42accb95fd5eb0f14dfdaed8af440a3c57ef3550af56628c9`  
		Last Modified: Thu, 09 Oct 2025 07:13:52 GMT  
		Size: 2.2 MB (2171372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91da73e4223b24a5c15a122491267b152c515232ed5594db74a1db1c66cf6138`  
		Last Modified: Thu, 09 Oct 2025 07:13:53 GMT  
		Size: 31.1 KB (31088 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; riscv64

```console
$ docker pull composer@sha256:7327310627d6b7d4e8caafcd67ae31c6c93c6efcdd2c1f2d9baa3919f6933b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72131616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6980c3ff13a9f02e427f6ba874939a94d99d4dfb200a39d1f0e3a9d9cac3269b`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:9ffe3756686e8121120603c46e2bcc7c25a6a0c923bdc47741ddd8ac23f7505c`  
		Last Modified: Thu, 09 Oct 2025 12:23:13 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66a307993ff99b5b3658ed178834c47681fdc3296384c58149d6a03f07ef86`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f92261afff37de278981985cbf1b23f5b946658937d6f613c95988742502fc1`  
		Last Modified: Thu, 09 Oct 2025 12:23:11 GMT  
		Size: 19.4 MB (19373788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f739a05185d11834b1e53840782634f634ce0d1eca4746926c47033d6cf1ded8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be024fc29f2390a64fe4d73fb0873a93a6ccb37995d0b252dd9bb174cd1e4895`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8011cdcf4f7bc91f25ad15e332853b7a1c42a076454400c738594f3962209b8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49955161ff3f60e3060e3064936558be7775fe3ee8780e3b391f05a302a87979`  
		Last Modified: Mon, 13 Oct 2025 06:30:16 GMT  
		Size: 31.1 MB (31112421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f659ae5d89daae889e03a88d8619444d53a5725d6a2ce755f2cf115f095c55a7`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53efee6d3e96229253c3a7725735789bf4a70b9a1330437f621da92eff26cf2`  
		Last Modified: Mon, 13 Oct 2025 06:35:07 GMT  
		Size: 818.0 KB (818001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5879ecbff9e99be6f4d887eb042e4c14f2bfe151121663593cb91a690f5704e`  
		Last Modified: Mon, 13 Oct 2025 06:35:07 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb37fdc8a5665d9ebd473e8cbc864f88305bb2237b89358c206142c3fba8973`  
		Last Modified: Mon, 13 Oct 2025 06:34:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:b2f3b28fde2e1acb5c6daa4e33a1aad229ea857c426174e9d2fcdacf4fac1fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06193ec23089bc241dbbebc222be01177af691b99b495986be6c29b48672740`

```dockerfile
```

-	Layers:
	-	`sha256:35a1e26915edb1bacf502fd9bbab1b2aa6acf7eb54c746f0819d073867b96028`  
		Last Modified: Mon, 13 Oct 2025 07:13:56 GMT  
		Size: 2.2 MB (2169639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87dfd1fa998c3011fb0a530c011f8eaef40b52d80446c4b11b26a2ebd1627ab4`  
		Last Modified: Mon, 13 Oct 2025 07:13:57 GMT  
		Size: 31.1 KB (31088 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; s390x

```console
$ docker pull composer@sha256:1613f51eb6e97ebe0e044364b0efc85dee0a15f781e16f868c4da86b8598eca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73688072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa9b56fa76a4083186af4f23bc2142eba8efaa43417ec7a273d17b0b99989c3`
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
ENV PHP_VERSION=8.4.13
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:b695282d592a178e4c36aa152fd59e9134e630400a7f212f7414d972457a8035`  
		Last Modified: Thu, 09 Oct 2025 01:06:21 GMT  
		Size: 13.7 MB (13667331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874309b732361867c2db5075f339f7d251d35a1999132dcbd51c4fe56c9f89b`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e822974d38b51bcdf4e8d50473316964925d3354c2f94b653b31f9886cf6a`  
		Last Modified: Thu, 09 Oct 2025 01:06:20 GMT  
		Size: 20.0 MB (19969497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a883aae99b872ee9827b2eaacabac2e42e262e2db3ecbfa459de9906907f78`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4dd335651ea2da6132f7a2def407e03ec362587a03fe3560afdcc27f769573`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 19.9 KB (19874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f5a27fa65467dec23807b65f8edbd31acd8a6a19f0fcfbeafd66e63326096`  
		Last Modified: Thu, 09 Oct 2025 01:06:19 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f07303d79642f1f6fb404a8362ed6ae9eddc69cd78578e51091cb475493090`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 823.3 KB (823321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2253d23f87d556dbd49a9d60e5599181400a82b367969b3240ebfec9ed62e295`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055da3fa01337a487323a552025f2674b3813f2ae6ad386ea8de35aa22f6361d`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:02d56363e74dcb994393bb3f8b0c29e018e3b0dd1b94972fae8ebe9d0c11c8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0215206443c671d7a23d81c0bfa3a6935208899dc688605e06b3892f2ab44551`

```dockerfile
```

-	Layers:
	-	`sha256:561cc1a52b71fb0fa9ed6c468b6f2da2b033fd505534e1a90ec2206346fa38ed`  
		Last Modified: Thu, 09 Oct 2025 10:14:14 GMT  
		Size: 2.2 MB (2169433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5fc09a5ef7167a9597751e5d1f89d97f7ed736db1e45b06e009d9a11fc2aa89`  
		Last Modified: Thu, 09 Oct 2025 10:14:15 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8`

```console
$ docker pull composer@sha256:24f538daf6d1e33e0859033ca2b50955b68fa69f7f3d2d1cba9a51b6cfdcf606
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
$ docker pull composer@sha256:0d264a0f1e5be23ba363447768df7b30c33d542711ea12e37770ed7b13bf4eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75854318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805d739ba8da4383b57f6a4598ebda6df35143471694058b52abb2f86b2a5fc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:d9c585fc0858fb182174b42e967fd91eba8f0c5fe46c0b8474a14a97ba00f9b2`  
		Last Modified: Fri, 24 Oct 2025 20:19:32 GMT  
		Size: 33.9 MB (33947500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554aa2fcd32d16117f10c09421ba2fefb8c6b62265e19c47aeff94a9a50deec8`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f21bf3d69502cdd5dd65e973522f62173298ce2c1cf733ba7570f1abbd3da8`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 974.2 KB (974204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e3b4ee80e6d8bd5ea2e0a6ee500ea0d4d914f4446a9eef230e6700da8ed8bc`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fa2707690f38f404a79ec9eca786e5f68c185bcaf824c7c6d9536839799046`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:c4e94577e3a79c265c3b2a19f013354fef208adf26f0e0b1ebf47de3299a3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300f9917da97bf0e9648cc7b1c32bdc1789a60247c2cefd1d2c0fa0b03d73e75`

```dockerfile
```

-	Layers:
	-	`sha256:f2dba5f611989bd14c743453e097ff55c3c4f04f5419790f3b03ebf0d0d0f708`  
		Last Modified: Fri, 24 Oct 2025 22:14:06 GMT  
		Size: 2.2 MB (2173415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c869f9ec9d58986a24b0a14f8d5d09e6e4cca043718593fc4d7f08cbf310879`  
		Last Modified: Fri, 24 Oct 2025 22:14:07 GMT  
		Size: 31.7 KB (31655 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:9204b9a7a9df81968c806f2b0ef4c9d8d8dbe51a43797588433645283b229763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73494680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e3b4574492ba4221f5bd32b26fcca99fdf67fcaaf16fb5f7b911e3ef00f9a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:677016e4a05cd9d7caa1de3ce5e214bb0f617ca04ddbe3ef67db12b83329c7b3`  
		Last Modified: Fri, 24 Oct 2025 20:42:36 GMT  
		Size: 33.8 MB (33817487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a74822dc5a1fff34f9cd0fc67c8071e7ecc6f1c05d7d960c05a30227ca7480`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32a2a61df1c0cf8de1f5d45fb41e404e4d47a7e0899c82d04d59f3170950fc`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 974.2 KB (974168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bb94e5ae85307dce2a049277d148fc7b9a6387ea8b247ba6861a3744de1226`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20bd3e81699adb6432acb1e3cdbd1bff47ab55f32a5650efff530ee60571771`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:9343c2cda94fd20ada22030f5317069866d7b954df251513f7035211ebb2043c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0858cebf9952fd446c0059e4836ad9bae408b15609d537ae27514ca4176ef99d`

```dockerfile
```

-	Layers:
	-	`sha256:124be63b687d3a7df1473e92ea5c6127c5e773e521e4afcf9f69219aed73d2e5`  
		Last Modified: Fri, 24 Oct 2025 22:14:11 GMT  
		Size: 31.5 KB (31546 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:11ef398e69d694688e37308b9e5080fed84e7c2eb3946d65f9b73947a1d1e9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70289253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306418dfd2976851ded90c22f09ab197aa633e78ce6f338f00e2b9cc5625dfb4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:e134e14d05100f43b1098cfe83dac4d1878e0011c90ebea8acb37fa0a034d56b`  
		Last Modified: Fri, 24 Oct 2025 20:50:30 GMT  
		Size: 32.1 MB (32097758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f37f8bb32b419173ac9421577528609a45422416c2fff8e18dc40cf26213b5a`  
		Last Modified: Fri, 24 Oct 2025 20:50:28 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e07052daa224ff10334146da5f8f819196b02cec75c0c697f74311642a71ba`  
		Last Modified: Fri, 24 Oct 2025 20:50:29 GMT  
		Size: 964.9 KB (964860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331e7b0382791466edbeebc26238c70f8de5b5ac274927a704e94f6df404e43e`  
		Last Modified: Fri, 24 Oct 2025 20:50:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168e3fc3448c5dddeb7cd2161898c590b6e0e2578d3cda47fed790dbc5c6e7d1`  
		Last Modified: Fri, 24 Oct 2025 20:50:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:d6fe4ee5ea5bca1674b479111c3508c6a073e4c2ff0f2f0d32128d61536654da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46df73f1ab448a2b152e0b688d749d065da3a1708443b9a519d3463fc3e92e2`

```dockerfile
```

-	Layers:
	-	`sha256:2fd2d9b3e5ae585128615abee4b9f96aaf8d7086ad7ae7847ff06bda446b1833`  
		Last Modified: Fri, 24 Oct 2025 22:14:14 GMT  
		Size: 2.2 MB (2173739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5182947cb87494b1e77c08965e298a8b09163adf95e7a1320c7e822e8c9c3db4`  
		Last Modified: Fri, 24 Oct 2025 22:14:15 GMT  
		Size: 31.8 KB (31761 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:cc2fd435c5dd57485421bc19c3e9226c29417f8065c00dcef2b2e361090f3c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75830669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96f81949775bd3e6004fd0cf0fc55607a2da42e6b9b26002e13a4b623d4994e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:413b61f8cb24ed8752e8cda1bdaef2720fa5a54ee5a47aedefbbdd3961a07c52`  
		Last Modified: Fri, 24 Oct 2025 20:19:12 GMT  
		Size: 34.0 MB (34036686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e877f4e26235bcebeb5785c987aafe66e1fb9b1e46cf1b31486e3f8d8895f2d`  
		Last Modified: Fri, 24 Oct 2025 20:19:06 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c02e3b72fe4e2884dc77540236af7c7ffc6d17f0279a2343e1134e04a48e40`  
		Last Modified: Fri, 24 Oct 2025 20:19:06 GMT  
		Size: 973.8 KB (973838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5275291d5a13a86a4848ebf143e11d59a8a3fa2d4beea8f15499913ba77d10`  
		Last Modified: Fri, 24 Oct 2025 20:19:06 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1974defaeb30f0d935ea55aa0c03c0b1de7093bf188fe4c3feb4522ffb682b`  
		Last Modified: Fri, 24 Oct 2025 20:19:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:fdb14d3db55f7fcff98bd67c452d6b8ead015d1ab9eaf75733f814144b8f5b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f060eb14b7cab778cc76b4e75dee2379b4d1f103236776a11ceeea19704e292`

```dockerfile
```

-	Layers:
	-	`sha256:f69adc6fe0d49623ae5e79ccb6c02183265f418c07f5533d89065ee043120d95`  
		Last Modified: Fri, 24 Oct 2025 22:14:18 GMT  
		Size: 2.2 MB (2173567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f52a286937f1b728814e34ee3fd26ebc7da67aa2f5adab8473787bfc2e9a147`  
		Last Modified: Fri, 24 Oct 2025 22:14:19 GMT  
		Size: 31.8 KB (31789 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; 386

```console
$ docker pull composer@sha256:089d747cdd596158dbb2d452bba33226ef7292f92ac5d09c44ffd343ae12b731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76796681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc29e7b010e01ab322670b822facc07e95152e99e917b4001127510506e872dd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:35e85a8d646dc17d692c7f4cdcc4e046f87a0e099d6d44d870b7de3c100dbdd1`  
		Last Modified: Fri, 24 Oct 2025 19:20:40 GMT  
		Size: 34.5 MB (34468366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7722d6eade39bd814b4fa8e278fd98603c7e6dad8fd33cb15c33917af5b6971f`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3381ca837f505d8a1fbded8daa098e03586f7511456078d4038c51c54c2ea83`  
		Last Modified: Fri, 24 Oct 2025 19:20:37 GMT  
		Size: 988.2 KB (988165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2927bd6eda562337b286187b19d702a1a9f557709d6064a8c2d728de3a4b96ee`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49a2d382dfa044f0f8dd680d2676d662e4b527dad096f9a0e8604b025c13d73`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:06a9a7469d1a02aaeac3f00d918558b958dca4f918289c723e807fcde1b99fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f7debe4722e173e422e260956be67adcbf2bbd9c567ad64f95096695dec5ed`

```dockerfile
```

-	Layers:
	-	`sha256:2b69994a499c47d3aed365b77ec99dc221049da9ca33e7f72fe2ba67daea7b09`  
		Last Modified: Fri, 24 Oct 2025 22:14:24 GMT  
		Size: 2.2 MB (2173198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce7ed4d16291f6dc0e7fae788e7678c1b917b04e3ec46eaeb5e9916670f31ff5`  
		Last Modified: Fri, 24 Oct 2025 22:14:24 GMT  
		Size: 31.6 KB (31619 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; ppc64le

```console
$ docker pull composer@sha256:7ab8f18c7690e96c4b2c0f98ca57e42441737139252d67b4213aa405cfadaeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78134372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf72e7a7216358538fcfc4866b29268353f4cb0bf3c5f8cd1e41b25e84f7ca00`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:08c541cc61ee10a80b399d52e1f4bb8a5279855a7fa2c9a76b046ab010b008a3`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccbe14cfb5f112f9165213e6c598f4ea32a7c520ab6aa2a8b2e62b24a58478a`  
		Last Modified: Thu, 09 Oct 2025 01:16:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03340f1e3e44fd83f3b7db1acc126ffeb5a590f53bdab6ca579db0ae5fa52f6c`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 20.9 MB (20858704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de31c9e8e61a6c9596dd41c2b70045f4d409bb66963fba6e71103aa5056ea81`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71522eac8e5e3d7e2dbd1df9937339ed30d1ec9b9680938e271a69acdb62839b`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b073119ff38c21d5615a254aaa7d93099fc3d9ffa24ba1014d9a4e26028463`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7069cbe03c650f9a782b558ea0c7b6eecf0b31471b705b90de9c985fc0584766`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 980.7 KB (980738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c9dfb2c75ab180a836d1a22b7399619b9d8544f6da246eac510b495b3be44b`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b721d4ea96a39181ad8693b4a8d88fb1845f909261dbf8a034cd63e16768dd99`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:11e9c625adf643934ca29589b3d294bb86103370ed72644386527ce5e5e3df3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05059bd123cffb6b560400732d38d0b86867c15100aba79c3223f2169599616d`

```dockerfile
```

-	Layers:
	-	`sha256:765e6400901500e644e76705796817786597f0dba11e9dca3548e9d777025dae`  
		Last Modified: Thu, 09 Oct 2025 07:13:45 GMT  
		Size: 2.2 MB (2171978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c016add85054c3cb7f2c16c4beb8f8dcc5bffc8fb5f7477d3a53ac2a593a2b85`  
		Last Modified: Thu, 09 Oct 2025 07:13:46 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; riscv64

```console
$ docker pull composer@sha256:d9454c3c75d02d24624d2d6741cbf61c1e896287265625736f0b7891039fafff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72285489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adec28a4a63fd7cc8cd54b34ddc6d53a178b2da922c574247c327397407ef119`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:9ffe3756686e8121120603c46e2bcc7c25a6a0c923bdc47741ddd8ac23f7505c`  
		Last Modified: Thu, 09 Oct 2025 12:23:13 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66a307993ff99b5b3658ed178834c47681fdc3296384c58149d6a03f07ef86`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f92261afff37de278981985cbf1b23f5b946658937d6f613c95988742502fc1`  
		Last Modified: Thu, 09 Oct 2025 12:23:11 GMT  
		Size: 19.4 MB (19373788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f739a05185d11834b1e53840782634f634ce0d1eca4746926c47033d6cf1ded8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be024fc29f2390a64fe4d73fb0873a93a6ccb37995d0b252dd9bb174cd1e4895`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8011cdcf4f7bc91f25ad15e332853b7a1c42a076454400c738594f3962209b8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49955161ff3f60e3060e3064936558be7775fe3ee8780e3b391f05a302a87979`  
		Last Modified: Mon, 13 Oct 2025 06:30:16 GMT  
		Size: 31.1 MB (31112421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f659ae5d89daae889e03a88d8619444d53a5725d6a2ce755f2cf115f095c55a7`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0947ceefd087c282c2cbd108a398739e126987182016113328633d16f6ef0e41`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 971.9 KB (971874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2a9e4844376d9dbbd6e414a8788a4d4985d6d092f498d319b5153812ef0450`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b667872090bb1420eafe05f6e33ce208d93749d7699c74ea351a9aa875a0049`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:662e721ba6de44ed649520b09fe9f80302e5cd1802270931cb9eab71954ace21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6c7c6b16c8e6358c55869f649ef0545603f856581b0e13395e2da4d38c3bf2`

```dockerfile
```

-	Layers:
	-	`sha256:8aae531408035419e447caef87ce80412c07e31343314679ba4856567d8d78eb`  
		Last Modified: Mon, 13 Oct 2025 07:13:49 GMT  
		Size: 2.2 MB (2170245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c72ebd04f61bd95eefa1e9eed6a74683833f088e8007e539cc0c33298f8e582d`  
		Last Modified: Mon, 13 Oct 2025 07:13:50 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; s390x

```console
$ docker pull composer@sha256:05595a53f3002bbd2ba712d1885651be62400b12bd14119f40191f7ae3aef015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73841920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502f45c09a39566b91313513de05acd6f1490e3c336a2c7fd24cac084ddf44dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:b695282d592a178e4c36aa152fd59e9134e630400a7f212f7414d972457a8035`  
		Last Modified: Thu, 09 Oct 2025 01:06:21 GMT  
		Size: 13.7 MB (13667331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874309b732361867c2db5075f339f7d251d35a1999132dcbd51c4fe56c9f89b`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e822974d38b51bcdf4e8d50473316964925d3354c2f94b653b31f9886cf6a`  
		Last Modified: Thu, 09 Oct 2025 01:06:20 GMT  
		Size: 20.0 MB (19969497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a883aae99b872ee9827b2eaacabac2e42e262e2db3ecbfa459de9906907f78`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4dd335651ea2da6132f7a2def407e03ec362587a03fe3560afdcc27f769573`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 19.9 KB (19874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f5a27fa65467dec23807b65f8edbd31acd8a6a19f0fcfbeafd66e63326096`  
		Last Modified: Thu, 09 Oct 2025 01:06:19 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b3763f27effcdcc686b244b630554f55656ad8f43c1abc3b8c8d516d707acd`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 977.2 KB (977171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e53287954018bc60f63bea842b06e6a30715c50a10e7021e3bad0e4ea802725`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3888304b21042155b83dc5bbfb55b5a62ecaa2401bd061ba507b2c2bfd3fa7d`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:a1dd369e5929c064afc2005875b7732ba60490562cbaf47c857940c7b8e6bc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ea6c568cc3c0b5074248845f5f93c92bb29da444b2c7be0d1529405b9ec94`

```dockerfile
```

-	Layers:
	-	`sha256:a19650be819af7eb6ff88e79275de8056eac5a7f961dda45b1832e83ffd71794`  
		Last Modified: Thu, 09 Oct 2025 10:14:06 GMT  
		Size: 2.2 MB (2170027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136b3d48a9b0c3a1e679291b71cf94a1e413d4692a883077c8c2fd3fc32b15cc`  
		Last Modified: Thu, 09 Oct 2025 10:14:07 GMT  
		Size: 31.7 KB (31654 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8.12`

```console
$ docker pull composer@sha256:24f538daf6d1e33e0859033ca2b50955b68fa69f7f3d2d1cba9a51b6cfdcf606
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

### `composer:2.8.12` - linux; amd64

```console
$ docker pull composer@sha256:0d264a0f1e5be23ba363447768df7b30c33d542711ea12e37770ed7b13bf4eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75854318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805d739ba8da4383b57f6a4598ebda6df35143471694058b52abb2f86b2a5fc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:d9c585fc0858fb182174b42e967fd91eba8f0c5fe46c0b8474a14a97ba00f9b2`  
		Last Modified: Fri, 24 Oct 2025 20:19:32 GMT  
		Size: 33.9 MB (33947500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554aa2fcd32d16117f10c09421ba2fefb8c6b62265e19c47aeff94a9a50deec8`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f21bf3d69502cdd5dd65e973522f62173298ce2c1cf733ba7570f1abbd3da8`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 974.2 KB (974204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e3b4ee80e6d8bd5ea2e0a6ee500ea0d4d914f4446a9eef230e6700da8ed8bc`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fa2707690f38f404a79ec9eca786e5f68c185bcaf824c7c6d9536839799046`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:c4e94577e3a79c265c3b2a19f013354fef208adf26f0e0b1ebf47de3299a3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300f9917da97bf0e9648cc7b1c32bdc1789a60247c2cefd1d2c0fa0b03d73e75`

```dockerfile
```

-	Layers:
	-	`sha256:f2dba5f611989bd14c743453e097ff55c3c4f04f5419790f3b03ebf0d0d0f708`  
		Last Modified: Fri, 24 Oct 2025 22:14:06 GMT  
		Size: 2.2 MB (2173415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c869f9ec9d58986a24b0a14f8d5d09e6e4cca043718593fc4d7f08cbf310879`  
		Last Modified: Fri, 24 Oct 2025 22:14:07 GMT  
		Size: 31.7 KB (31655 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.12` - linux; arm variant v6

```console
$ docker pull composer@sha256:9204b9a7a9df81968c806f2b0ef4c9d8d8dbe51a43797588433645283b229763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73494680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e3b4574492ba4221f5bd32b26fcca99fdf67fcaaf16fb5f7b911e3ef00f9a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:677016e4a05cd9d7caa1de3ce5e214bb0f617ca04ddbe3ef67db12b83329c7b3`  
		Last Modified: Fri, 24 Oct 2025 20:42:36 GMT  
		Size: 33.8 MB (33817487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a74822dc5a1fff34f9cd0fc67c8071e7ecc6f1c05d7d960c05a30227ca7480`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32a2a61df1c0cf8de1f5d45fb41e404e4d47a7e0899c82d04d59f3170950fc`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 974.2 KB (974168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bb94e5ae85307dce2a049277d148fc7b9a6387ea8b247ba6861a3744de1226`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20bd3e81699adb6432acb1e3cdbd1bff47ab55f32a5650efff530ee60571771`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:9343c2cda94fd20ada22030f5317069866d7b954df251513f7035211ebb2043c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0858cebf9952fd446c0059e4836ad9bae408b15609d537ae27514ca4176ef99d`

```dockerfile
```

-	Layers:
	-	`sha256:124be63b687d3a7df1473e92ea5c6127c5e773e521e4afcf9f69219aed73d2e5`  
		Last Modified: Fri, 24 Oct 2025 22:14:11 GMT  
		Size: 31.5 KB (31546 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.12` - linux; arm variant v7

```console
$ docker pull composer@sha256:11ef398e69d694688e37308b9e5080fed84e7c2eb3946d65f9b73947a1d1e9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70289253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306418dfd2976851ded90c22f09ab197aa633e78ce6f338f00e2b9cc5625dfb4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:e134e14d05100f43b1098cfe83dac4d1878e0011c90ebea8acb37fa0a034d56b`  
		Last Modified: Fri, 24 Oct 2025 20:50:30 GMT  
		Size: 32.1 MB (32097758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f37f8bb32b419173ac9421577528609a45422416c2fff8e18dc40cf26213b5a`  
		Last Modified: Fri, 24 Oct 2025 20:50:28 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e07052daa224ff10334146da5f8f819196b02cec75c0c697f74311642a71ba`  
		Last Modified: Fri, 24 Oct 2025 20:50:29 GMT  
		Size: 964.9 KB (964860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331e7b0382791466edbeebc26238c70f8de5b5ac274927a704e94f6df404e43e`  
		Last Modified: Fri, 24 Oct 2025 20:50:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168e3fc3448c5dddeb7cd2161898c590b6e0e2578d3cda47fed790dbc5c6e7d1`  
		Last Modified: Fri, 24 Oct 2025 20:50:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:d6fe4ee5ea5bca1674b479111c3508c6a073e4c2ff0f2f0d32128d61536654da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46df73f1ab448a2b152e0b688d749d065da3a1708443b9a519d3463fc3e92e2`

```dockerfile
```

-	Layers:
	-	`sha256:2fd2d9b3e5ae585128615abee4b9f96aaf8d7086ad7ae7847ff06bda446b1833`  
		Last Modified: Fri, 24 Oct 2025 22:14:14 GMT  
		Size: 2.2 MB (2173739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5182947cb87494b1e77c08965e298a8b09163adf95e7a1320c7e822e8c9c3db4`  
		Last Modified: Fri, 24 Oct 2025 22:14:15 GMT  
		Size: 31.8 KB (31761 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.12` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:cc2fd435c5dd57485421bc19c3e9226c29417f8065c00dcef2b2e361090f3c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75830669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96f81949775bd3e6004fd0cf0fc55607a2da42e6b9b26002e13a4b623d4994e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:413b61f8cb24ed8752e8cda1bdaef2720fa5a54ee5a47aedefbbdd3961a07c52`  
		Last Modified: Fri, 24 Oct 2025 20:19:12 GMT  
		Size: 34.0 MB (34036686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e877f4e26235bcebeb5785c987aafe66e1fb9b1e46cf1b31486e3f8d8895f2d`  
		Last Modified: Fri, 24 Oct 2025 20:19:06 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c02e3b72fe4e2884dc77540236af7c7ffc6d17f0279a2343e1134e04a48e40`  
		Last Modified: Fri, 24 Oct 2025 20:19:06 GMT  
		Size: 973.8 KB (973838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5275291d5a13a86a4848ebf143e11d59a8a3fa2d4beea8f15499913ba77d10`  
		Last Modified: Fri, 24 Oct 2025 20:19:06 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1974defaeb30f0d935ea55aa0c03c0b1de7093bf188fe4c3feb4522ffb682b`  
		Last Modified: Fri, 24 Oct 2025 20:19:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:fdb14d3db55f7fcff98bd67c452d6b8ead015d1ab9eaf75733f814144b8f5b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f060eb14b7cab778cc76b4e75dee2379b4d1f103236776a11ceeea19704e292`

```dockerfile
```

-	Layers:
	-	`sha256:f69adc6fe0d49623ae5e79ccb6c02183265f418c07f5533d89065ee043120d95`  
		Last Modified: Fri, 24 Oct 2025 22:14:18 GMT  
		Size: 2.2 MB (2173567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f52a286937f1b728814e34ee3fd26ebc7da67aa2f5adab8473787bfc2e9a147`  
		Last Modified: Fri, 24 Oct 2025 22:14:19 GMT  
		Size: 31.8 KB (31789 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.12` - linux; 386

```console
$ docker pull composer@sha256:089d747cdd596158dbb2d452bba33226ef7292f92ac5d09c44ffd343ae12b731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76796681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc29e7b010e01ab322670b822facc07e95152e99e917b4001127510506e872dd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:35e85a8d646dc17d692c7f4cdcc4e046f87a0e099d6d44d870b7de3c100dbdd1`  
		Last Modified: Fri, 24 Oct 2025 19:20:40 GMT  
		Size: 34.5 MB (34468366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7722d6eade39bd814b4fa8e278fd98603c7e6dad8fd33cb15c33917af5b6971f`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3381ca837f505d8a1fbded8daa098e03586f7511456078d4038c51c54c2ea83`  
		Last Modified: Fri, 24 Oct 2025 19:20:37 GMT  
		Size: 988.2 KB (988165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2927bd6eda562337b286187b19d702a1a9f557709d6064a8c2d728de3a4b96ee`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49a2d382dfa044f0f8dd680d2676d662e4b527dad096f9a0e8604b025c13d73`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:06a9a7469d1a02aaeac3f00d918558b958dca4f918289c723e807fcde1b99fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f7debe4722e173e422e260956be67adcbf2bbd9c567ad64f95096695dec5ed`

```dockerfile
```

-	Layers:
	-	`sha256:2b69994a499c47d3aed365b77ec99dc221049da9ca33e7f72fe2ba67daea7b09`  
		Last Modified: Fri, 24 Oct 2025 22:14:24 GMT  
		Size: 2.2 MB (2173198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce7ed4d16291f6dc0e7fae788e7678c1b917b04e3ec46eaeb5e9916670f31ff5`  
		Last Modified: Fri, 24 Oct 2025 22:14:24 GMT  
		Size: 31.6 KB (31619 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.12` - linux; ppc64le

```console
$ docker pull composer@sha256:7ab8f18c7690e96c4b2c0f98ca57e42441737139252d67b4213aa405cfadaeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78134372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf72e7a7216358538fcfc4866b29268353f4cb0bf3c5f8cd1e41b25e84f7ca00`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:08c541cc61ee10a80b399d52e1f4bb8a5279855a7fa2c9a76b046ab010b008a3`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccbe14cfb5f112f9165213e6c598f4ea32a7c520ab6aa2a8b2e62b24a58478a`  
		Last Modified: Thu, 09 Oct 2025 01:16:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03340f1e3e44fd83f3b7db1acc126ffeb5a590f53bdab6ca579db0ae5fa52f6c`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 20.9 MB (20858704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de31c9e8e61a6c9596dd41c2b70045f4d409bb66963fba6e71103aa5056ea81`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71522eac8e5e3d7e2dbd1df9937339ed30d1ec9b9680938e271a69acdb62839b`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b073119ff38c21d5615a254aaa7d93099fc3d9ffa24ba1014d9a4e26028463`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7069cbe03c650f9a782b558ea0c7b6eecf0b31471b705b90de9c985fc0584766`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 980.7 KB (980738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c9dfb2c75ab180a836d1a22b7399619b9d8544f6da246eac510b495b3be44b`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b721d4ea96a39181ad8693b4a8d88fb1845f909261dbf8a034cd63e16768dd99`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:11e9c625adf643934ca29589b3d294bb86103370ed72644386527ce5e5e3df3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05059bd123cffb6b560400732d38d0b86867c15100aba79c3223f2169599616d`

```dockerfile
```

-	Layers:
	-	`sha256:765e6400901500e644e76705796817786597f0dba11e9dca3548e9d777025dae`  
		Last Modified: Thu, 09 Oct 2025 07:13:45 GMT  
		Size: 2.2 MB (2171978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c016add85054c3cb7f2c16c4beb8f8dcc5bffc8fb5f7477d3a53ac2a593a2b85`  
		Last Modified: Thu, 09 Oct 2025 07:13:46 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.12` - linux; riscv64

```console
$ docker pull composer@sha256:d9454c3c75d02d24624d2d6741cbf61c1e896287265625736f0b7891039fafff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72285489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adec28a4a63fd7cc8cd54b34ddc6d53a178b2da922c574247c327397407ef119`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:9ffe3756686e8121120603c46e2bcc7c25a6a0c923bdc47741ddd8ac23f7505c`  
		Last Modified: Thu, 09 Oct 2025 12:23:13 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66a307993ff99b5b3658ed178834c47681fdc3296384c58149d6a03f07ef86`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f92261afff37de278981985cbf1b23f5b946658937d6f613c95988742502fc1`  
		Last Modified: Thu, 09 Oct 2025 12:23:11 GMT  
		Size: 19.4 MB (19373788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f739a05185d11834b1e53840782634f634ce0d1eca4746926c47033d6cf1ded8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be024fc29f2390a64fe4d73fb0873a93a6ccb37995d0b252dd9bb174cd1e4895`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8011cdcf4f7bc91f25ad15e332853b7a1c42a076454400c738594f3962209b8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49955161ff3f60e3060e3064936558be7775fe3ee8780e3b391f05a302a87979`  
		Last Modified: Mon, 13 Oct 2025 06:30:16 GMT  
		Size: 31.1 MB (31112421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f659ae5d89daae889e03a88d8619444d53a5725d6a2ce755f2cf115f095c55a7`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0947ceefd087c282c2cbd108a398739e126987182016113328633d16f6ef0e41`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 971.9 KB (971874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2a9e4844376d9dbbd6e414a8788a4d4985d6d092f498d319b5153812ef0450`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b667872090bb1420eafe05f6e33ce208d93749d7699c74ea351a9aa875a0049`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:662e721ba6de44ed649520b09fe9f80302e5cd1802270931cb9eab71954ace21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6c7c6b16c8e6358c55869f649ef0545603f856581b0e13395e2da4d38c3bf2`

```dockerfile
```

-	Layers:
	-	`sha256:8aae531408035419e447caef87ce80412c07e31343314679ba4856567d8d78eb`  
		Last Modified: Mon, 13 Oct 2025 07:13:49 GMT  
		Size: 2.2 MB (2170245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c72ebd04f61bd95eefa1e9eed6a74683833f088e8007e539cc0c33298f8e582d`  
		Last Modified: Mon, 13 Oct 2025 07:13:50 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.12` - linux; s390x

```console
$ docker pull composer@sha256:05595a53f3002bbd2ba712d1885651be62400b12bd14119f40191f7ae3aef015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73841920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502f45c09a39566b91313513de05acd6f1490e3c336a2c7fd24cac084ddf44dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:b695282d592a178e4c36aa152fd59e9134e630400a7f212f7414d972457a8035`  
		Last Modified: Thu, 09 Oct 2025 01:06:21 GMT  
		Size: 13.7 MB (13667331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874309b732361867c2db5075f339f7d251d35a1999132dcbd51c4fe56c9f89b`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e822974d38b51bcdf4e8d50473316964925d3354c2f94b653b31f9886cf6a`  
		Last Modified: Thu, 09 Oct 2025 01:06:20 GMT  
		Size: 20.0 MB (19969497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a883aae99b872ee9827b2eaacabac2e42e262e2db3ecbfa459de9906907f78`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4dd335651ea2da6132f7a2def407e03ec362587a03fe3560afdcc27f769573`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 19.9 KB (19874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f5a27fa65467dec23807b65f8edbd31acd8a6a19f0fcfbeafd66e63326096`  
		Last Modified: Thu, 09 Oct 2025 01:06:19 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b3763f27effcdcc686b244b630554f55656ad8f43c1abc3b8c8d516d707acd`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 977.2 KB (977171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e53287954018bc60f63bea842b06e6a30715c50a10e7021e3bad0e4ea802725`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3888304b21042155b83dc5bbfb55b5a62ecaa2401bd061ba507b2c2bfd3fa7d`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.12` - unknown; unknown

```console
$ docker pull composer@sha256:a1dd369e5929c064afc2005875b7732ba60490562cbaf47c857940c7b8e6bc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ea6c568cc3c0b5074248845f5f93c92bb29da444b2c7be0d1529405b9ec94`

```dockerfile
```

-	Layers:
	-	`sha256:a19650be819af7eb6ff88e79275de8056eac5a7f961dda45b1832e83ffd71794`  
		Last Modified: Thu, 09 Oct 2025 10:14:06 GMT  
		Size: 2.2 MB (2170027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136b3d48a9b0c3a1e679291b71cf94a1e413d4692a883077c8c2fd3fc32b15cc`  
		Last Modified: Thu, 09 Oct 2025 10:14:07 GMT  
		Size: 31.7 KB (31654 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:24f538daf6d1e33e0859033ca2b50955b68fa69f7f3d2d1cba9a51b6cfdcf606
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
$ docker pull composer@sha256:0d264a0f1e5be23ba363447768df7b30c33d542711ea12e37770ed7b13bf4eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75854318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805d739ba8da4383b57f6a4598ebda6df35143471694058b52abb2f86b2a5fc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:d9c585fc0858fb182174b42e967fd91eba8f0c5fe46c0b8474a14a97ba00f9b2`  
		Last Modified: Fri, 24 Oct 2025 20:19:32 GMT  
		Size: 33.9 MB (33947500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554aa2fcd32d16117f10c09421ba2fefb8c6b62265e19c47aeff94a9a50deec8`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f21bf3d69502cdd5dd65e973522f62173298ce2c1cf733ba7570f1abbd3da8`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 974.2 KB (974204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e3b4ee80e6d8bd5ea2e0a6ee500ea0d4d914f4446a9eef230e6700da8ed8bc`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fa2707690f38f404a79ec9eca786e5f68c185bcaf824c7c6d9536839799046`  
		Last Modified: Fri, 24 Oct 2025 20:19:28 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:c4e94577e3a79c265c3b2a19f013354fef208adf26f0e0b1ebf47de3299a3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300f9917da97bf0e9648cc7b1c32bdc1789a60247c2cefd1d2c0fa0b03d73e75`

```dockerfile
```

-	Layers:
	-	`sha256:f2dba5f611989bd14c743453e097ff55c3c4f04f5419790f3b03ebf0d0d0f708`  
		Last Modified: Fri, 24 Oct 2025 22:14:06 GMT  
		Size: 2.2 MB (2173415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c869f9ec9d58986a24b0a14f8d5d09e6e4cca043718593fc4d7f08cbf310879`  
		Last Modified: Fri, 24 Oct 2025 22:14:07 GMT  
		Size: 31.7 KB (31655 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:9204b9a7a9df81968c806f2b0ef4c9d8d8dbe51a43797588433645283b229763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73494680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e3b4574492ba4221f5bd32b26fcca99fdf67fcaaf16fb5f7b911e3ef00f9a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:677016e4a05cd9d7caa1de3ce5e214bb0f617ca04ddbe3ef67db12b83329c7b3`  
		Last Modified: Fri, 24 Oct 2025 20:42:36 GMT  
		Size: 33.8 MB (33817487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a74822dc5a1fff34f9cd0fc67c8071e7ecc6f1c05d7d960c05a30227ca7480`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32a2a61df1c0cf8de1f5d45fb41e404e4d47a7e0899c82d04d59f3170950fc`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 974.2 KB (974168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bb94e5ae85307dce2a049277d148fc7b9a6387ea8b247ba6861a3744de1226`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20bd3e81699adb6432acb1e3cdbd1bff47ab55f32a5650efff530ee60571771`  
		Last Modified: Fri, 24 Oct 2025 20:42:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:9343c2cda94fd20ada22030f5317069866d7b954df251513f7035211ebb2043c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0858cebf9952fd446c0059e4836ad9bae408b15609d537ae27514ca4176ef99d`

```dockerfile
```

-	Layers:
	-	`sha256:124be63b687d3a7df1473e92ea5c6127c5e773e521e4afcf9f69219aed73d2e5`  
		Last Modified: Fri, 24 Oct 2025 22:14:11 GMT  
		Size: 31.5 KB (31546 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:11ef398e69d694688e37308b9e5080fed84e7c2eb3946d65f9b73947a1d1e9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70289253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306418dfd2976851ded90c22f09ab197aa633e78ce6f338f00e2b9cc5625dfb4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:e134e14d05100f43b1098cfe83dac4d1878e0011c90ebea8acb37fa0a034d56b`  
		Last Modified: Fri, 24 Oct 2025 20:50:30 GMT  
		Size: 32.1 MB (32097758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f37f8bb32b419173ac9421577528609a45422416c2fff8e18dc40cf26213b5a`  
		Last Modified: Fri, 24 Oct 2025 20:50:28 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e07052daa224ff10334146da5f8f819196b02cec75c0c697f74311642a71ba`  
		Last Modified: Fri, 24 Oct 2025 20:50:29 GMT  
		Size: 964.9 KB (964860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331e7b0382791466edbeebc26238c70f8de5b5ac274927a704e94f6df404e43e`  
		Last Modified: Fri, 24 Oct 2025 20:50:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168e3fc3448c5dddeb7cd2161898c590b6e0e2578d3cda47fed790dbc5c6e7d1`  
		Last Modified: Fri, 24 Oct 2025 20:50:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:d6fe4ee5ea5bca1674b479111c3508c6a073e4c2ff0f2f0d32128d61536654da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46df73f1ab448a2b152e0b688d749d065da3a1708443b9a519d3463fc3e92e2`

```dockerfile
```

-	Layers:
	-	`sha256:2fd2d9b3e5ae585128615abee4b9f96aaf8d7086ad7ae7847ff06bda446b1833`  
		Last Modified: Fri, 24 Oct 2025 22:14:14 GMT  
		Size: 2.2 MB (2173739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5182947cb87494b1e77c08965e298a8b09163adf95e7a1320c7e822e8c9c3db4`  
		Last Modified: Fri, 24 Oct 2025 22:14:15 GMT  
		Size: 31.8 KB (31761 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:cc2fd435c5dd57485421bc19c3e9226c29417f8065c00dcef2b2e361090f3c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75830669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96f81949775bd3e6004fd0cf0fc55607a2da42e6b9b26002e13a4b623d4994e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:413b61f8cb24ed8752e8cda1bdaef2720fa5a54ee5a47aedefbbdd3961a07c52`  
		Last Modified: Fri, 24 Oct 2025 20:19:12 GMT  
		Size: 34.0 MB (34036686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e877f4e26235bcebeb5785c987aafe66e1fb9b1e46cf1b31486e3f8d8895f2d`  
		Last Modified: Fri, 24 Oct 2025 20:19:06 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c02e3b72fe4e2884dc77540236af7c7ffc6d17f0279a2343e1134e04a48e40`  
		Last Modified: Fri, 24 Oct 2025 20:19:06 GMT  
		Size: 973.8 KB (973838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5275291d5a13a86a4848ebf143e11d59a8a3fa2d4beea8f15499913ba77d10`  
		Last Modified: Fri, 24 Oct 2025 20:19:06 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1974defaeb30f0d935ea55aa0c03c0b1de7093bf188fe4c3feb4522ffb682b`  
		Last Modified: Fri, 24 Oct 2025 20:19:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:fdb14d3db55f7fcff98bd67c452d6b8ead015d1ab9eaf75733f814144b8f5b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2205356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f060eb14b7cab778cc76b4e75dee2379b4d1f103236776a11ceeea19704e292`

```dockerfile
```

-	Layers:
	-	`sha256:f69adc6fe0d49623ae5e79ccb6c02183265f418c07f5533d89065ee043120d95`  
		Last Modified: Fri, 24 Oct 2025 22:14:18 GMT  
		Size: 2.2 MB (2173567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f52a286937f1b728814e34ee3fd26ebc7da67aa2f5adab8473787bfc2e9a147`  
		Last Modified: Fri, 24 Oct 2025 22:14:19 GMT  
		Size: 31.8 KB (31789 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:089d747cdd596158dbb2d452bba33226ef7292f92ac5d09c44ffd343ae12b731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76796681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc29e7b010e01ab322670b822facc07e95152e99e917b4001127510506e872dd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.14
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:35e85a8d646dc17d692c7f4cdcc4e046f87a0e099d6d44d870b7de3c100dbdd1`  
		Last Modified: Fri, 24 Oct 2025 19:20:40 GMT  
		Size: 34.5 MB (34468366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7722d6eade39bd814b4fa8e278fd98603c7e6dad8fd33cb15c33917af5b6971f`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3381ca837f505d8a1fbded8daa098e03586f7511456078d4038c51c54c2ea83`  
		Last Modified: Fri, 24 Oct 2025 19:20:37 GMT  
		Size: 988.2 KB (988165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2927bd6eda562337b286187b19d702a1a9f557709d6064a8c2d728de3a4b96ee`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49a2d382dfa044f0f8dd680d2676d662e4b527dad096f9a0e8604b025c13d73`  
		Last Modified: Fri, 24 Oct 2025 19:20:36 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:06a9a7469d1a02aaeac3f00d918558b958dca4f918289c723e807fcde1b99fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2204817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f7debe4722e173e422e260956be67adcbf2bbd9c567ad64f95096695dec5ed`

```dockerfile
```

-	Layers:
	-	`sha256:2b69994a499c47d3aed365b77ec99dc221049da9ca33e7f72fe2ba67daea7b09`  
		Last Modified: Fri, 24 Oct 2025 22:14:24 GMT  
		Size: 2.2 MB (2173198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce7ed4d16291f6dc0e7fae788e7678c1b917b04e3ec46eaeb5e9916670f31ff5`  
		Last Modified: Fri, 24 Oct 2025 22:14:24 GMT  
		Size: 31.6 KB (31619 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:7ab8f18c7690e96c4b2c0f98ca57e42441737139252d67b4213aa405cfadaeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78134372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf72e7a7216358538fcfc4866b29268353f4cb0bf3c5f8cd1e41b25e84f7ca00`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:08c541cc61ee10a80b399d52e1f4bb8a5279855a7fa2c9a76b046ab010b008a3`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccbe14cfb5f112f9165213e6c598f4ea32a7c520ab6aa2a8b2e62b24a58478a`  
		Last Modified: Thu, 09 Oct 2025 01:16:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03340f1e3e44fd83f3b7db1acc126ffeb5a590f53bdab6ca579db0ae5fa52f6c`  
		Last Modified: Thu, 09 Oct 2025 01:16:11 GMT  
		Size: 20.9 MB (20858704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de31c9e8e61a6c9596dd41c2b70045f4d409bb66963fba6e71103aa5056ea81`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71522eac8e5e3d7e2dbd1df9937339ed30d1ec9b9680938e271a69acdb62839b`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b073119ff38c21d5615a254aaa7d93099fc3d9ffa24ba1014d9a4e26028463`  
		Last Modified: Thu, 09 Oct 2025 01:16:10 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc750c69d5845f08b366fcf588ae6020f2df3bb4a5bf650228778ed0a9fde88`  
		Last Modified: Thu, 09 Oct 2025 05:56:38 GMT  
		Size: 35.2 MB (35236113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0dfb7c3cec49e9a0f110d7243d5d9fcce6cda1e117d0fbaa88cf3efa29c872`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7069cbe03c650f9a782b558ea0c7b6eecf0b31471b705b90de9c985fc0584766`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 980.7 KB (980738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c9dfb2c75ab180a836d1a22b7399619b9d8544f6da246eac510b495b3be44b`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b721d4ea96a39181ad8693b4a8d88fb1845f909261dbf8a034cd63e16768dd99`  
		Last Modified: Thu, 09 Oct 2025 05:56:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:11e9c625adf643934ca29589b3d294bb86103370ed72644386527ce5e5e3df3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05059bd123cffb6b560400732d38d0b86867c15100aba79c3223f2169599616d`

```dockerfile
```

-	Layers:
	-	`sha256:765e6400901500e644e76705796817786597f0dba11e9dca3548e9d777025dae`  
		Last Modified: Thu, 09 Oct 2025 07:13:45 GMT  
		Size: 2.2 MB (2171978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c016add85054c3cb7f2c16c4beb8f8dcc5bffc8fb5f7477d3a53ac2a593a2b85`  
		Last Modified: Thu, 09 Oct 2025 07:13:46 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:d9454c3c75d02d24624d2d6741cbf61c1e896287265625736f0b7891039fafff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72285489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adec28a4a63fd7cc8cd54b34ddc6d53a178b2da922c574247c327397407ef119`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:9ffe3756686e8121120603c46e2bcc7c25a6a0c923bdc47741ddd8ac23f7505c`  
		Last Modified: Thu, 09 Oct 2025 12:23:13 GMT  
		Size: 13.7 MB (13667307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66a307993ff99b5b3658ed178834c47681fdc3296384c58149d6a03f07ef86`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f92261afff37de278981985cbf1b23f5b946658937d6f613c95988742502fc1`  
		Last Modified: Thu, 09 Oct 2025 12:23:11 GMT  
		Size: 19.4 MB (19373788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f739a05185d11834b1e53840782634f634ce0d1eca4746926c47033d6cf1ded8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be024fc29f2390a64fe4d73fb0873a93a6ccb37995d0b252dd9bb174cd1e4895`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8011cdcf4f7bc91f25ad15e332853b7a1c42a076454400c738594f3962209b8`  
		Last Modified: Thu, 09 Oct 2025 12:23:09 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49955161ff3f60e3060e3064936558be7775fe3ee8780e3b391f05a302a87979`  
		Last Modified: Mon, 13 Oct 2025 06:30:16 GMT  
		Size: 31.1 MB (31112421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f659ae5d89daae889e03a88d8619444d53a5725d6a2ce755f2cf115f095c55a7`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0947ceefd087c282c2cbd108a398739e126987182016113328633d16f6ef0e41`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 971.9 KB (971874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2a9e4844376d9dbbd6e414a8788a4d4985d6d092f498d319b5153812ef0450`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b667872090bb1420eafe05f6e33ce208d93749d7699c74ea351a9aa875a0049`  
		Last Modified: Mon, 13 Oct 2025 06:30:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:662e721ba6de44ed649520b09fe9f80302e5cd1802270931cb9eab71954ace21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6c7c6b16c8e6358c55869f649ef0545603f856581b0e13395e2da4d38c3bf2`

```dockerfile
```

-	Layers:
	-	`sha256:8aae531408035419e447caef87ce80412c07e31343314679ba4856567d8d78eb`  
		Last Modified: Mon, 13 Oct 2025 07:13:49 GMT  
		Size: 2.2 MB (2170245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c72ebd04f61bd95eefa1e9eed6a74683833f088e8007e539cc0c33298f8e582d`  
		Last Modified: Mon, 13 Oct 2025 07:13:50 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:05595a53f3002bbd2ba712d1885651be62400b12bd14119f40191f7ae3aef015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73841920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502f45c09a39566b91313513de05acd6f1490e3c336a2c7fd24cac084ddf44dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 19 Sep 2025 12:51:13 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["/bin/sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Sep 2025 12:51:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Sep 2025 12:51:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_VERSION=8.4.13
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Fri, 19 Sep 2025 12:51:13 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Sep 2025 12:51:13 GMT
CMD ["php" "-a"]
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 19 Sep 2025 12:51:13 GMT
ENV COMPOSER_VERSION=2.8.12
# Fri, 19 Sep 2025 12:51:13 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:51:13 GMT
WORKDIR /app
# Fri, 19 Sep 2025 12:51:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Sep 2025 12:51:13 GMT
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
	-	`sha256:b695282d592a178e4c36aa152fd59e9134e630400a7f212f7414d972457a8035`  
		Last Modified: Thu, 09 Oct 2025 01:06:21 GMT  
		Size: 13.7 MB (13667331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874309b732361867c2db5075f339f7d251d35a1999132dcbd51c4fe56c9f89b`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3e822974d38b51bcdf4e8d50473316964925d3354c2f94b653b31f9886cf6a`  
		Last Modified: Thu, 09 Oct 2025 01:06:20 GMT  
		Size: 20.0 MB (19969497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a883aae99b872ee9827b2eaacabac2e42e262e2db3ecbfa459de9906907f78`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4dd335651ea2da6132f7a2def407e03ec362587a03fe3560afdcc27f769573`  
		Last Modified: Thu, 09 Oct 2025 01:06:18 GMT  
		Size: 19.9 KB (19874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f5a27fa65467dec23807b65f8edbd31acd8a6a19f0fcfbeafd66e63326096`  
		Last Modified: Thu, 09 Oct 2025 01:06:19 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5219110d4f3e49ef43fca54c828f77476de52c08e27b490e23eb605777c4b8`  
		Last Modified: Thu, 09 Oct 2025 08:07:33 GMT  
		Size: 31.8 MB (31841368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b912ad325203381f087b9b20815b78a8a62274eb021560b83d0a130fdadc83`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b3763f27effcdcc686b244b630554f55656ad8f43c1abc3b8c8d516d707acd`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 977.2 KB (977171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e53287954018bc60f63bea842b06e6a30715c50a10e7021e3bad0e4ea802725`  
		Last Modified: Thu, 09 Oct 2025 08:07:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3888304b21042155b83dc5bbfb55b5a62ecaa2401bd061ba507b2c2bfd3fa7d`  
		Last Modified: Thu, 09 Oct 2025 08:07:32 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:a1dd369e5929c064afc2005875b7732ba60490562cbaf47c857940c7b8e6bc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3ea6c568cc3c0b5074248845f5f93c92bb29da444b2c7be0d1529405b9ec94`

```dockerfile
```

-	Layers:
	-	`sha256:a19650be819af7eb6ff88e79275de8056eac5a7f961dda45b1832e83ffd71794`  
		Last Modified: Thu, 09 Oct 2025 10:14:06 GMT  
		Size: 2.2 MB (2170027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136b3d48a9b0c3a1e679291b71cf94a1e413d4692a883077c8c2fd3fc32b15cc`  
		Last Modified: Thu, 09 Oct 2025 10:14:07 GMT  
		Size: 31.7 KB (31654 bytes)  
		MIME: application/vnd.in-toto+json
