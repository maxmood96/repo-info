<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.27`](#composer11027)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.25`](#composer2225)
-	[`composer:2.8`](#composer28)
-	[`composer:2.8.4`](#composer284)
-	[`composer:latest`](#composerlatest)
-	[`composer:lts`](#composerlts)

## `composer:1`

```console
$ docker pull composer@sha256:e99e61410cb87423abfc27501618836e8f7e2854c03edee9ef25f3ec3b139fbd
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
$ docker pull composer@sha256:f6f2f0df04f62f7dd02c747b1d0c9161df399c52c540f9a7852d086ecdfa6193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74622834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261b67752a8421c1bf84ddae7bc9562583567a7791b75d8d2c37b7dd608b2be5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926a903e79620f0a500e6c0b8920613cf3e77ee6fb031d64dfb3cb7d88442adc`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 3.3 MB (3336077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c946fba36f12b591be4b090159dd42766dc43c2a20caf28d504ef17c4491759`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac17bc9a4d3a9a1781e2999ce34426d9eec4eed120cb79c459b841169a923918`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8b186c29f3bb1fcde6dd416dd06bb7c990d07b2c9d4621ce4e8f93c94b835d`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 13.6 MB (13580495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e6cdee304691570c26af03b2fedb4dd8016faa742d307b7db946e6409f326`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27e6ddc32c5ab1579764b32caa4c52c636d33a510c4c3ef4495726c95381872`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.9 MB (20883408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7be51eeb9ec7eea5691039e5a979e9ae08b3c661c6e02bf44451ec261ec5b9`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c0be2943e6e61d571707b0255ead75b0198314874eefbdb3bfb8250db6c13e`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.1 KB (20064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8929cf6910012f550931620ff33afa2a5eeb28951deb94cf77e02da91edc9c`  
		Last Modified: Fri, 20 Dec 2024 22:34:02 GMT  
		Size: 31.9 MB (31896315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592305bd0b09f3f4bf2abb5855fd7df7d7f38228b07839e62d8e4c99b7aa2453`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de74cf125483e009cead30c88117a3784c581fdfe312f6dfef20d93a28be902`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 1.3 MB (1257179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1230cc481b09e600355d743ccf5f1ef1f6133229329f2864d85a1bb6b8e36f`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517e54ceb37a099c3ab292f6a687964a4b0f7deb256c639398b85b33a51d55cb`  
		Last Modified: Fri, 20 Dec 2024 22:34:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:8e2293cec65d5af2bce53e9d9c79a4e9b9c56ed918b26874183fedd670ee7b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f301b33fe54b95266bf217f0f4ece38deaaa6376f1c66ef65e59f211dac466`

```dockerfile
```

-	Layers:
	-	`sha256:8e60d3fd23d48da6b3c8aabe4d800e729d1b7e7372c58d4f11fa93a45f405f06`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 2.2 MB (2159053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c700f9717dba9c5e80b2338ffc409ed5df47fd980aa794754c9d0a6626ee297a`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:75475c855c43a508fb3aa5c1a12be942dbb4a753da6620df57d46e85bf7c241e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71747441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad773af411c2e3b099e57ce2dc103384f8f3cc17658dcf1d4462e2c988bf210b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b736a50b989ce147c8a50cd4eff3990052fbae41313316dd15bdd3ae41bb055`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 3.3 MB (3302897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520076a7063b8a800f7aeb276beb6363fa2c2192a17d803ee3f5fa20b0b0b211`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065854d8dae5a225e01a05809bd10528e215d02290cc6d9f51d4bc29dc1ac134`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7d8a646b13a1fce87a53e224ba759100c5661201fa77b07c2bb37e766e4399`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 13.6 MB (13580525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e81800135bc7fff5c18dd6a26d344cbcdc0f282ae7198e61803d1b9e97af13`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce8a346ef963d66430f1390abc1b68a4824385373ab05fa645c2aca57b6015`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.5 MB (19498804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eb2dc0afa0290d833b6477da2f88fe368ba4cefd3a8a5ef03f8561794efefa`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf11115b0d6d263d3685a04147a9d95c5179c52b651782cf9289977a6ac1ce`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a3ca09f084e2d996e8974d62fa6bd1b01b2867e5b1a057e00140bad318027d`  
		Last Modified: Fri, 20 Dec 2024 23:03:37 GMT  
		Size: 30.6 MB (30641288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c129606c926c4221d682770c2daaa54b304e77c6d10ac37d86224ded916fede3`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468aa2771d33870aa52d7276e0d644e3b2a0c1d49457facc8f98c48c443e9652`  
		Last Modified: Fri, 20 Dec 2024 23:04:19 GMT  
		Size: 1.3 MB (1331997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceec54fcb2477b469f9dca645219b218dc16b9abef7401105c9053f18e97c13`  
		Last Modified: Thu, 12 Dec 2024 01:10:16 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25de431533dc12c765715f77dcdd288f363c1175640be0767623fa5077aa01db`  
		Last Modified: Fri, 20 Dec 2024 23:04:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:e75d1f065e75f88eb05cd311df26fea5978e9ec42121e65f206cdb6329cf64c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5918d7d29d8b5f624f7408ea116ed719b2c6a9f2c2e39dbe8f4643fca3d7527e`

```dockerfile
```

-	Layers:
	-	`sha256:c448db397a898884cdc65f97cf9d700839beeb272c6b89b11c6d2129251f7296`  
		Last Modified: Fri, 20 Dec 2024 23:04:18 GMT  
		Size: 30.5 KB (30546 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:d6b500646669fefbb84c644e5542bff7e0aa8bed6d96389a33dd5f8fcdef5fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69677494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b34e72c61d28626b8c3d9005b712f42a2aa45b3bc99b2ad6a3109583e1279a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58a80555964d79b4c54d0bc69d1ac3c99d92bfa41dc077ad9039581c976fe1`  
		Last Modified: Wed, 11 Dec 2024 23:35:20 GMT  
		Size: 3.1 MB (3128235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30daf13605f2d1179f6005fb32926b33b8626b9ceb92de019df902d09cedf935`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365fc515397f6962469f3d1c8654b5801822a766158bca2e8a9fa961d78db8`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7b2510a73dde296829d64a7a766b9532e9e98238663d7544fcb11d828edf19`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 13.6 MB (13580531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05cf7b909bafdb9e34f1486d56a868891fed509111b921f6d72259313be2e5`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb18584dfdd2c5e1b16be910211bf58df75bebb8cc948d010bf7dacf1a81b`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 18.4 MB (18447692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af84d6773702a8389925020e1881a84b42b39eea9ebe082e379503372b4a2c6`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302c968087e93f72bd0a3e8da913da2a3b5cc3802ff0de5d389e6740323ef52`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 19.9 KB (19899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71edb0952ef713ac379d22d60a6a0e5e1ab8e1a7e0d6858994829d1584dfa20b`  
		Last Modified: Sat, 21 Dec 2024 00:54:42 GMT  
		Size: 30.2 MB (30150125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdfebf91571a2efa29d6268aafa0080828a4a9bc3ad5ecc7e2b43895774db5f`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3720e5b02237d0aad44cb437f18887d2226c222af60b025389ff8c14abfbf394`  
		Last Modified: Sat, 21 Dec 2024 00:55:21 GMT  
		Size: 1.2 MB (1246114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f638ec92f77aca1364999ec432ce9e6c5597380d8399a3303274811393423`  
		Last Modified: Sat, 21 Dec 2024 00:55:21 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1365514d3ef81faf9888a73d1b9e61f8bb44f75edec1d73e67757889bf4c91`  
		Last Modified: Sat, 21 Dec 2024 00:55:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:e03331179000157e2f3736a4c3a341575489b1c862eca61c26bfe23e192dd224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822fd38c403caac2afadec98a235d9acda9825146f33d156592318ad0982837`

```dockerfile
```

-	Layers:
	-	`sha256:e134f3eddf39bfdc15f41cb9a9a48cf3e0271a0a7f7d59c29d2b17d57f72eec2`  
		Last Modified: Sat, 21 Dec 2024 00:55:21 GMT  
		Size: 2.2 MB (2159369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a62cb3e6c95b15354610328bccb95a16d3c5e9fe205cb63997b5cdc04c1433`  
		Last Modified: Sat, 21 Dec 2024 00:55:20 GMT  
		Size: 30.8 KB (30761 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:6497d9402693041c40abf25999f202c68e0014b26055e0a4b5ca44fca32c4f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75126776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d0828f9a828f17b4ffd93f858f97011ddf1a36d5a80c1465b907e0fd9213b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02eb691f526c59a4feade4837dd3c26533d9fe4c9306da60dc23a30620af346`  
		Last Modified: Wed, 11 Dec 2024 23:34:10 GMT  
		Size: 3.3 MB (3331581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f32f7c87db3a6447e39cf371cb0c2bb2c95f7a814793eff967d2a9a3b95122`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7c12be75768edb813fc94e2e1d2c48d7cb1f4cea2c832026ca6ae796dff9ac`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2737967709483bb9e56014fca897a13fd112c3084028d6543b06a30985537c4e`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 13.6 MB (13580520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b64ce4fbef8321cb5b9a415b540a4baa87078a9d7ee17306f53198aa5c3d6b`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a01d64640e85e99659018a2a9d802c50d724bde24674cd1ace68a407f974cc8`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 20.9 MB (20912964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61930bd78024ed559eceaae6edaa2d5a5396db98ea69ec50e91c0ce227b97848`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e991f93dcb7aadac92e8529d0719e89be0fbb0cc3478b38e16914291fef40b`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8074648689cf1786e687dd5d23af39dfbe621da1270c66591b9671c41a9a8d35`  
		Last Modified: Sat, 21 Dec 2024 01:55:18 GMT  
		Size: 32.0 MB (32002924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafd0942fb02c25d23f08063ad2cbeab093d6cf618b8d1e3da7813080cf0a5d3`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e346e7494cdb07ad315dd65f8d5d2223a530acd24ca34b9fdec5780bef049610`  
		Last Modified: Sat, 21 Dec 2024 01:55:54 GMT  
		Size: 1.3 MB (1280839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327c51b2dbedc95dc22baad8ad83b2a05a8cd5d7cdbdd46b1f255d94dca24b1d`  
		Last Modified: Sat, 21 Dec 2024 01:55:53 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ac0f4203607a86081b60630045eb5fc7a752d91372d470b27e47ac05bc7866`  
		Last Modified: Sat, 21 Dec 2024 01:55:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:e56e9d0cbb9e8ecf718c3bd1e86d25e09b14c298be0b4cc4591336e90e8cc765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6448d96d0d8e03998848e626037099cca38beff91f0303ba11d4ffc87c6b0f56`

```dockerfile
```

-	Layers:
	-	`sha256:b2387690409d58feb678f2ac28ffbf2b75dbca1d3230188db44114230879a03c`  
		Last Modified: Sat, 21 Dec 2024 01:55:54 GMT  
		Size: 2.2 MB (2159193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a2675988e7c1a9db332796528523cd27bd60e7de8da36b10cdf7b63e51e3f9`  
		Last Modified: Sat, 21 Dec 2024 01:55:53 GMT  
		Size: 30.8 KB (30789 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:b2d7fd0b5df1db249af431ed539d3b4f0b5091f69519a624c55e140fbced11c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69599ad7c0d061be0c290927c1c0d1f3cf9f71abb21c3a45afc1165689eccb8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c898e29d83e9db370e8891b59d2b75d52becd1c60e7168a6068c60ab70d34d74`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 3.4 MB (3376600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaee1fb0dd467b0c78610a290f1dab2d06cab056e446bcd035ed5a5be5bad5f`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6589c5988c6fb89267a968f26279f8f922579aeafe69c3b3d5c70ff348de1faf`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f212ddee911fee0e94e486cf1d8c16d2e4609a0aca213ae03ef06b0ec953924`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 13.6 MB (13580481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc377b1762be65b8185324b4a83578d3e2bdb568e2370167b8ad00c5b3f2c5e`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dc25b1fb1a50563b2ccab2e97a663fcdf74d01b6d4f08ecdf423a7ec4178c9`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 21.4 MB (21397982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e557dee7812f54a16556ac580967a78aca6fb0c9444067feedb7c2fec0f1cf`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cacd67f7a12349f00be424d47f5a310859feb05ec769add44557c85dc4c045e`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 20.1 KB (20067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ea983c662a4c7aecfe50add16177147526623e4806159e5ca212d77090d131`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 11.4 MB (11421309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8dee48b1ed735d54e49355cc0e65a8faf12985a8251ee73f1c8c3442801155`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fbb9304d79110f6d7b0d97131342d7277dd225a13fd092dfe46d2755a8335`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 1.2 MB (1236578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a20b259e8d923b4c7a7ae1f115a9adc979621bb21e7459ec21816af795f3cfd`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0be2475ad4f5b74ecd46e819ab2a6a1d4fa3b97e4c15bcc496c5f28c017d28`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:9517ffcead6082b27ce8c525acba065d895c04dd270459d7c7ff06e3e66c9c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.3 KB (459347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fd9bc47a618474d1625dca96c8b0ac6a59186e22ea746ef815ac9db2de5b76`

```dockerfile
```

-	Layers:
	-	`sha256:3e101185d85c6a49576af10bd051b3a0b737ece4885c6c3dd7e7f4dc334333b0`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 428.7 KB (428711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f06839aed1b1ae33c05655f833803443e3cb075c52713c372314172cbc4325d`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 30.6 KB (30636 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:a152483bacfe60aec95718fc0c7d8a3c52832cd5a125487d9406874bb958219e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77195865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d0bc7be25d5a8af0b16f3ae331a06122522618def1458043f7311ca7ab6943`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dab8c9093e7207bf34d7e27bcaf8a12d512bc9a6228a188ccd032ab556c048`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 3.5 MB (3474267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887eff0819f1e81cf0537030ec0eefbed710884b4bdcb74a53300dafe99af22`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d10c33dd4ddf3d7039e24ae3ea2657811b8add42853a37557baa89339c584`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73154329c1c9a418799584abd71b5689505fae8a1fe0c1edf20b4c054fdfa404`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe8613e572e5a00abda95594733a8b015a569e70fcfb60f921b46b1d3b0b4ce`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bfbf1907d341a6d1c62419f97827940bb943dfd0067d8cce4a44af3d1da5c0`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 22.3 MB (22287679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa21b603882a7aa1280eb0a92a0814e2acb781ef4ea1490d6871b2cf300d5ed`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b46dc3369c678c5f6e91da763573d92319716e4238a641860950d083934a3b`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320193b91948f33c75121c293867d724d3bd3982783314901a94db790aab8942`  
		Last Modified: Sat, 21 Dec 2024 00:47:37 GMT  
		Size: 32.9 MB (32943931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87a05827ee97083cff81d981bb3bc249115eff0447c4e4a7b65127727301f1c`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1609958598829cbb95f942c795946be9e69aec96f8b4ecf911d7d9805c58dc9`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 1.3 MB (1307604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14939a9b7c36211dc15f90c4fa60b9b7167d2567826d8b79b6ccb97e59becf3d`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e662a9b885b617d41c5e59a01fc02bb6697ecc8dab3257c507d5e52f645bf9e4`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:6231a1f92fbab53bf8eca89fea472ffce39eca25a1afecc239146b7f1d350eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357fa3b6ad00541c405e4cf6a47938cd5c46eaf3b2babe60ea579a8b02d8790c`

```dockerfile
```

-	Layers:
	-	`sha256:9548a136be27d24de779000b4ba818228a62ffd301f27ca677af58f260afae5d`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 2.2 MB (2157610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ca6a526ae0512535d3d1547dd8a9183a0eb4d96ccf4808947c97a6beba7c0d1`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 30.7 KB (30709 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:8bc890682a436777508adbfe1428a5ebd4329b4024c25b84371c11bb596f19b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72928818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837d8435881ee9fd2c3bb91d5196af59945048fcc13deb02f0029921533fb3d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65b4aeb40f99d5493f73d9206995a90aa94768378fa8ed5e3d1bfa1a5650e5`  
		Last Modified: Thu, 12 Dec 2024 05:33:08 GMT  
		Size: 13.6 MB (13573066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3a97d778691306fc952ddd90fe8250103f76d9aeb4d0203ae146e8e521bae`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087168628cd777dcb9b702d528d92efb821d834b9f0dcd8c3797efb04ae1c3b9`  
		Last Modified: Thu, 12 Dec 2024 05:33:09 GMT  
		Size: 20.3 MB (20313768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df21e8373b5877a4b523291936f8960c514ba6fad4100e893b67db195cf644`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1688f016a09ac412aed8ac075c283501f128abef9696857d645a64c550c669`  
		Last Modified: Thu, 12 Dec 2024 05:33:07 GMT  
		Size: 19.9 KB (19881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabab48893d974e79a79888fc6df380c6dcf350a41715045f49febecefddffeb`  
		Last Modified: Fri, 13 Dec 2024 00:49:21 GMT  
		Size: 31.0 MB (31000601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede30cfb10bc21715eab17b816b53c120038851e557f760c598e7ce4e84e9148`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31f87b8020fbedb15dfb281c219e43c304b3143e7514d43ef00c5071b2db008`  
		Last Modified: Fri, 13 Dec 2024 00:54:26 GMT  
		Size: 1.2 MB (1216846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa73d9236be884be92d3577f58932ae343b2ba52298cf5d46931b99d53b58ce1`  
		Last Modified: Fri, 13 Dec 2024 00:54:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e72c857244708c8aa47c19384d557c44395c05110c348a78f75ab5c69d3dbd`  
		Last Modified: Fri, 13 Dec 2024 00:54:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:35694c527d101786faa78cd5c8f5c2e1d6ef2e28174b5342490a4e60cbb5eded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a412cc8edeb98c8f408100065e448b22b697ba88376520bc00625fb51494280c`

```dockerfile
```

-	Layers:
	-	`sha256:0ae29bd8c0761e4049dabcba5bd5ace3f8c276657017eb6c36b677871b5d99a3`  
		Last Modified: Fri, 13 Dec 2024 00:54:26 GMT  
		Size: 2.2 MB (2159620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f77f0951d08b4fb34050e4a3bf83d4127b06f892b32e434b0cf9b504397ed1b`  
		Last Modified: Fri, 13 Dec 2024 00:54:25 GMT  
		Size: 30.7 KB (30709 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:203c510a1b28317b19747a357222bb6482aacd40c1a44322e5518763c28f768d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75478982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee7ecfc49d6c78cadc734cdbadd544a60b2b53d349b2b0ec0983bc0f714c8b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b02d148e9caeb82d2cf6c286e6c9c576dbce389f6c2cb18910b789ebd4813`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 3.6 MB (3561751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d561dc5f913bf5ac5c30d9c4d42bdf7aa341b8fba0e0ded0354c6e1aca173438`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465f443f2fadb2b0191af2eb2aae7a8ff4e66fef38973f7b9f36688fc1ff5cc`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167bd40a3a9b1f0b21e6140078bd769d2d967f4713b5f34ccb482a4b419592fe`  
		Last Modified: Fri, 20 Dec 2024 22:04:11 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd8774ef9fa0dca490b5d556eec80cd22fa38fbd2ad90d593168cffab7f95de`  
		Last Modified: Fri, 20 Dec 2024 22:04:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0154e3b89ce7965e82ffec7aff04edec326644e952fe96eca0cbe395ccb151b8`  
		Last Modified: Sat, 21 Dec 2024 01:07:03 GMT  
		Size: 21.9 MB (21867735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1a08d85e9f5ffb6b386d5b9a9c2260779e2408eb44cf874b23d61902f877a`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946fabb80ac5e81a3ba1e80ef02c503fa9257fd27f28ce77c24815e131b7f5bf`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cae5d9bba6d84260838c31aac6e5cc01aadf2ab697ab41df33ab9508312e2e1`  
		Last Modified: Sat, 21 Dec 2024 02:09:57 GMT  
		Size: 31.7 MB (31675723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1671f7a4b9055dd3f4c65b5f95cca757e39df07b78b85cd25865c7838f093`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddecc87c862574fba1558e8e8d387ccc316566f1fd3a319b33adc44ef5f0633b`  
		Last Modified: Sat, 21 Dec 2024 02:11:07 GMT  
		Size: 1.3 MB (1298985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced976e9e84b3f9f81d527553fffcbf38ab11557dd8214d08a01101a2efc31aa`  
		Last Modified: Sat, 21 Dec 2024 02:11:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03d2fb37f9dcd370dbff1c415a899ca81d9ddcd5710cb0a64048f6db1889831`  
		Last Modified: Sat, 21 Dec 2024 02:11:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:0197c57da756af1cb04786935966c3952d4b5ae422058fe8228e8cd6620bf3a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76aee25416c6d2e0557c52851b5ef756eb17c81dde17010d6c40bdeecdaf11e1`

```dockerfile
```

-	Layers:
	-	`sha256:5902f8dd88c5dd12fc53080f9e72e26b7a7556c922cfd0024b26804ad6014ddb`  
		Last Modified: Sat, 21 Dec 2024 02:11:07 GMT  
		Size: 2.2 MB (2156338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8765fd135abaa8d0c08622dd7932ae1050aedcef136b69ed94ce978a82ad8e`  
		Last Modified: Sat, 21 Dec 2024 02:11:07 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:e99e61410cb87423abfc27501618836e8f7e2854c03edee9ef25f3ec3b139fbd
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
$ docker pull composer@sha256:f6f2f0df04f62f7dd02c747b1d0c9161df399c52c540f9a7852d086ecdfa6193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74622834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261b67752a8421c1bf84ddae7bc9562583567a7791b75d8d2c37b7dd608b2be5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926a903e79620f0a500e6c0b8920613cf3e77ee6fb031d64dfb3cb7d88442adc`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 3.3 MB (3336077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c946fba36f12b591be4b090159dd42766dc43c2a20caf28d504ef17c4491759`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac17bc9a4d3a9a1781e2999ce34426d9eec4eed120cb79c459b841169a923918`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8b186c29f3bb1fcde6dd416dd06bb7c990d07b2c9d4621ce4e8f93c94b835d`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 13.6 MB (13580495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e6cdee304691570c26af03b2fedb4dd8016faa742d307b7db946e6409f326`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27e6ddc32c5ab1579764b32caa4c52c636d33a510c4c3ef4495726c95381872`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.9 MB (20883408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7be51eeb9ec7eea5691039e5a979e9ae08b3c661c6e02bf44451ec261ec5b9`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c0be2943e6e61d571707b0255ead75b0198314874eefbdb3bfb8250db6c13e`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.1 KB (20064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8929cf6910012f550931620ff33afa2a5eeb28951deb94cf77e02da91edc9c`  
		Last Modified: Fri, 20 Dec 2024 22:34:02 GMT  
		Size: 31.9 MB (31896315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592305bd0b09f3f4bf2abb5855fd7df7d7f38228b07839e62d8e4c99b7aa2453`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de74cf125483e009cead30c88117a3784c581fdfe312f6dfef20d93a28be902`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 1.3 MB (1257179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1230cc481b09e600355d743ccf5f1ef1f6133229329f2864d85a1bb6b8e36f`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517e54ceb37a099c3ab292f6a687964a4b0f7deb256c639398b85b33a51d55cb`  
		Last Modified: Fri, 20 Dec 2024 22:34:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:8e2293cec65d5af2bce53e9d9c79a4e9b9c56ed918b26874183fedd670ee7b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f301b33fe54b95266bf217f0f4ece38deaaa6376f1c66ef65e59f211dac466`

```dockerfile
```

-	Layers:
	-	`sha256:8e60d3fd23d48da6b3c8aabe4d800e729d1b7e7372c58d4f11fa93a45f405f06`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 2.2 MB (2159053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c700f9717dba9c5e80b2338ffc409ed5df47fd980aa794754c9d0a6626ee297a`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:75475c855c43a508fb3aa5c1a12be942dbb4a753da6620df57d46e85bf7c241e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71747441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad773af411c2e3b099e57ce2dc103384f8f3cc17658dcf1d4462e2c988bf210b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b736a50b989ce147c8a50cd4eff3990052fbae41313316dd15bdd3ae41bb055`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 3.3 MB (3302897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520076a7063b8a800f7aeb276beb6363fa2c2192a17d803ee3f5fa20b0b0b211`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065854d8dae5a225e01a05809bd10528e215d02290cc6d9f51d4bc29dc1ac134`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7d8a646b13a1fce87a53e224ba759100c5661201fa77b07c2bb37e766e4399`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 13.6 MB (13580525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e81800135bc7fff5c18dd6a26d344cbcdc0f282ae7198e61803d1b9e97af13`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce8a346ef963d66430f1390abc1b68a4824385373ab05fa645c2aca57b6015`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.5 MB (19498804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eb2dc0afa0290d833b6477da2f88fe368ba4cefd3a8a5ef03f8561794efefa`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf11115b0d6d263d3685a04147a9d95c5179c52b651782cf9289977a6ac1ce`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a3ca09f084e2d996e8974d62fa6bd1b01b2867e5b1a057e00140bad318027d`  
		Last Modified: Fri, 20 Dec 2024 23:03:37 GMT  
		Size: 30.6 MB (30641288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c129606c926c4221d682770c2daaa54b304e77c6d10ac37d86224ded916fede3`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468aa2771d33870aa52d7276e0d644e3b2a0c1d49457facc8f98c48c443e9652`  
		Last Modified: Fri, 20 Dec 2024 23:04:19 GMT  
		Size: 1.3 MB (1331997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceec54fcb2477b469f9dca645219b218dc16b9abef7401105c9053f18e97c13`  
		Last Modified: Thu, 12 Dec 2024 01:10:16 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25de431533dc12c765715f77dcdd288f363c1175640be0767623fa5077aa01db`  
		Last Modified: Fri, 20 Dec 2024 23:04:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:e75d1f065e75f88eb05cd311df26fea5978e9ec42121e65f206cdb6329cf64c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5918d7d29d8b5f624f7408ea116ed719b2c6a9f2c2e39dbe8f4643fca3d7527e`

```dockerfile
```

-	Layers:
	-	`sha256:c448db397a898884cdc65f97cf9d700839beeb272c6b89b11c6d2129251f7296`  
		Last Modified: Fri, 20 Dec 2024 23:04:18 GMT  
		Size: 30.5 KB (30546 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:d6b500646669fefbb84c644e5542bff7e0aa8bed6d96389a33dd5f8fcdef5fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69677494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b34e72c61d28626b8c3d9005b712f42a2aa45b3bc99b2ad6a3109583e1279a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58a80555964d79b4c54d0bc69d1ac3c99d92bfa41dc077ad9039581c976fe1`  
		Last Modified: Wed, 11 Dec 2024 23:35:20 GMT  
		Size: 3.1 MB (3128235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30daf13605f2d1179f6005fb32926b33b8626b9ceb92de019df902d09cedf935`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365fc515397f6962469f3d1c8654b5801822a766158bca2e8a9fa961d78db8`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7b2510a73dde296829d64a7a766b9532e9e98238663d7544fcb11d828edf19`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 13.6 MB (13580531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05cf7b909bafdb9e34f1486d56a868891fed509111b921f6d72259313be2e5`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb18584dfdd2c5e1b16be910211bf58df75bebb8cc948d010bf7dacf1a81b`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 18.4 MB (18447692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af84d6773702a8389925020e1881a84b42b39eea9ebe082e379503372b4a2c6`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302c968087e93f72bd0a3e8da913da2a3b5cc3802ff0de5d389e6740323ef52`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 19.9 KB (19899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71edb0952ef713ac379d22d60a6a0e5e1ab8e1a7e0d6858994829d1584dfa20b`  
		Last Modified: Sat, 21 Dec 2024 00:54:42 GMT  
		Size: 30.2 MB (30150125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdfebf91571a2efa29d6268aafa0080828a4a9bc3ad5ecc7e2b43895774db5f`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3720e5b02237d0aad44cb437f18887d2226c222af60b025389ff8c14abfbf394`  
		Last Modified: Sat, 21 Dec 2024 00:55:21 GMT  
		Size: 1.2 MB (1246114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f638ec92f77aca1364999ec432ce9e6c5597380d8399a3303274811393423`  
		Last Modified: Sat, 21 Dec 2024 00:55:21 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1365514d3ef81faf9888a73d1b9e61f8bb44f75edec1d73e67757889bf4c91`  
		Last Modified: Sat, 21 Dec 2024 00:55:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:e03331179000157e2f3736a4c3a341575489b1c862eca61c26bfe23e192dd224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822fd38c403caac2afadec98a235d9acda9825146f33d156592318ad0982837`

```dockerfile
```

-	Layers:
	-	`sha256:e134f3eddf39bfdc15f41cb9a9a48cf3e0271a0a7f7d59c29d2b17d57f72eec2`  
		Last Modified: Sat, 21 Dec 2024 00:55:21 GMT  
		Size: 2.2 MB (2159369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a62cb3e6c95b15354610328bccb95a16d3c5e9fe205cb63997b5cdc04c1433`  
		Last Modified: Sat, 21 Dec 2024 00:55:20 GMT  
		Size: 30.8 KB (30761 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:6497d9402693041c40abf25999f202c68e0014b26055e0a4b5ca44fca32c4f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75126776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d0828f9a828f17b4ffd93f858f97011ddf1a36d5a80c1465b907e0fd9213b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02eb691f526c59a4feade4837dd3c26533d9fe4c9306da60dc23a30620af346`  
		Last Modified: Wed, 11 Dec 2024 23:34:10 GMT  
		Size: 3.3 MB (3331581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f32f7c87db3a6447e39cf371cb0c2bb2c95f7a814793eff967d2a9a3b95122`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7c12be75768edb813fc94e2e1d2c48d7cb1f4cea2c832026ca6ae796dff9ac`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2737967709483bb9e56014fca897a13fd112c3084028d6543b06a30985537c4e`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 13.6 MB (13580520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b64ce4fbef8321cb5b9a415b540a4baa87078a9d7ee17306f53198aa5c3d6b`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a01d64640e85e99659018a2a9d802c50d724bde24674cd1ace68a407f974cc8`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 20.9 MB (20912964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61930bd78024ed559eceaae6edaa2d5a5396db98ea69ec50e91c0ce227b97848`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e991f93dcb7aadac92e8529d0719e89be0fbb0cc3478b38e16914291fef40b`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8074648689cf1786e687dd5d23af39dfbe621da1270c66591b9671c41a9a8d35`  
		Last Modified: Sat, 21 Dec 2024 01:55:18 GMT  
		Size: 32.0 MB (32002924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafd0942fb02c25d23f08063ad2cbeab093d6cf618b8d1e3da7813080cf0a5d3`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e346e7494cdb07ad315dd65f8d5d2223a530acd24ca34b9fdec5780bef049610`  
		Last Modified: Sat, 21 Dec 2024 01:55:54 GMT  
		Size: 1.3 MB (1280839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327c51b2dbedc95dc22baad8ad83b2a05a8cd5d7cdbdd46b1f255d94dca24b1d`  
		Last Modified: Sat, 21 Dec 2024 01:55:53 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ac0f4203607a86081b60630045eb5fc7a752d91372d470b27e47ac05bc7866`  
		Last Modified: Sat, 21 Dec 2024 01:55:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:e56e9d0cbb9e8ecf718c3bd1e86d25e09b14c298be0b4cc4591336e90e8cc765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6448d96d0d8e03998848e626037099cca38beff91f0303ba11d4ffc87c6b0f56`

```dockerfile
```

-	Layers:
	-	`sha256:b2387690409d58feb678f2ac28ffbf2b75dbca1d3230188db44114230879a03c`  
		Last Modified: Sat, 21 Dec 2024 01:55:54 GMT  
		Size: 2.2 MB (2159193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a2675988e7c1a9db332796528523cd27bd60e7de8da36b10cdf7b63e51e3f9`  
		Last Modified: Sat, 21 Dec 2024 01:55:53 GMT  
		Size: 30.8 KB (30789 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:b2d7fd0b5df1db249af431ed539d3b4f0b5091f69519a624c55e140fbced11c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69599ad7c0d061be0c290927c1c0d1f3cf9f71abb21c3a45afc1165689eccb8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c898e29d83e9db370e8891b59d2b75d52becd1c60e7168a6068c60ab70d34d74`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 3.4 MB (3376600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaee1fb0dd467b0c78610a290f1dab2d06cab056e446bcd035ed5a5be5bad5f`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6589c5988c6fb89267a968f26279f8f922579aeafe69c3b3d5c70ff348de1faf`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f212ddee911fee0e94e486cf1d8c16d2e4609a0aca213ae03ef06b0ec953924`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 13.6 MB (13580481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc377b1762be65b8185324b4a83578d3e2bdb568e2370167b8ad00c5b3f2c5e`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dc25b1fb1a50563b2ccab2e97a663fcdf74d01b6d4f08ecdf423a7ec4178c9`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 21.4 MB (21397982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e557dee7812f54a16556ac580967a78aca6fb0c9444067feedb7c2fec0f1cf`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cacd67f7a12349f00be424d47f5a310859feb05ec769add44557c85dc4c045e`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 20.1 KB (20067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ea983c662a4c7aecfe50add16177147526623e4806159e5ca212d77090d131`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 11.4 MB (11421309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8dee48b1ed735d54e49355cc0e65a8faf12985a8251ee73f1c8c3442801155`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fbb9304d79110f6d7b0d97131342d7277dd225a13fd092dfe46d2755a8335`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 1.2 MB (1236578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a20b259e8d923b4c7a7ae1f115a9adc979621bb21e7459ec21816af795f3cfd`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0be2475ad4f5b74ecd46e819ab2a6a1d4fa3b97e4c15bcc496c5f28c017d28`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:9517ffcead6082b27ce8c525acba065d895c04dd270459d7c7ff06e3e66c9c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.3 KB (459347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fd9bc47a618474d1625dca96c8b0ac6a59186e22ea746ef815ac9db2de5b76`

```dockerfile
```

-	Layers:
	-	`sha256:3e101185d85c6a49576af10bd051b3a0b737ece4885c6c3dd7e7f4dc334333b0`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 428.7 KB (428711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f06839aed1b1ae33c05655f833803443e3cb075c52713c372314172cbc4325d`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 30.6 KB (30636 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:a152483bacfe60aec95718fc0c7d8a3c52832cd5a125487d9406874bb958219e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77195865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d0bc7be25d5a8af0b16f3ae331a06122522618def1458043f7311ca7ab6943`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dab8c9093e7207bf34d7e27bcaf8a12d512bc9a6228a188ccd032ab556c048`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 3.5 MB (3474267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887eff0819f1e81cf0537030ec0eefbed710884b4bdcb74a53300dafe99af22`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d10c33dd4ddf3d7039e24ae3ea2657811b8add42853a37557baa89339c584`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73154329c1c9a418799584abd71b5689505fae8a1fe0c1edf20b4c054fdfa404`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe8613e572e5a00abda95594733a8b015a569e70fcfb60f921b46b1d3b0b4ce`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bfbf1907d341a6d1c62419f97827940bb943dfd0067d8cce4a44af3d1da5c0`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 22.3 MB (22287679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa21b603882a7aa1280eb0a92a0814e2acb781ef4ea1490d6871b2cf300d5ed`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b46dc3369c678c5f6e91da763573d92319716e4238a641860950d083934a3b`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320193b91948f33c75121c293867d724d3bd3982783314901a94db790aab8942`  
		Last Modified: Sat, 21 Dec 2024 00:47:37 GMT  
		Size: 32.9 MB (32943931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87a05827ee97083cff81d981bb3bc249115eff0447c4e4a7b65127727301f1c`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1609958598829cbb95f942c795946be9e69aec96f8b4ecf911d7d9805c58dc9`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 1.3 MB (1307604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14939a9b7c36211dc15f90c4fa60b9b7167d2567826d8b79b6ccb97e59becf3d`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e662a9b885b617d41c5e59a01fc02bb6697ecc8dab3257c507d5e52f645bf9e4`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:6231a1f92fbab53bf8eca89fea472ffce39eca25a1afecc239146b7f1d350eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357fa3b6ad00541c405e4cf6a47938cd5c46eaf3b2babe60ea579a8b02d8790c`

```dockerfile
```

-	Layers:
	-	`sha256:9548a136be27d24de779000b4ba818228a62ffd301f27ca677af58f260afae5d`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 2.2 MB (2157610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ca6a526ae0512535d3d1547dd8a9183a0eb4d96ccf4808947c97a6beba7c0d1`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 30.7 KB (30709 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:8bc890682a436777508adbfe1428a5ebd4329b4024c25b84371c11bb596f19b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72928818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837d8435881ee9fd2c3bb91d5196af59945048fcc13deb02f0029921533fb3d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65b4aeb40f99d5493f73d9206995a90aa94768378fa8ed5e3d1bfa1a5650e5`  
		Last Modified: Thu, 12 Dec 2024 05:33:08 GMT  
		Size: 13.6 MB (13573066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3a97d778691306fc952ddd90fe8250103f76d9aeb4d0203ae146e8e521bae`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087168628cd777dcb9b702d528d92efb821d834b9f0dcd8c3797efb04ae1c3b9`  
		Last Modified: Thu, 12 Dec 2024 05:33:09 GMT  
		Size: 20.3 MB (20313768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df21e8373b5877a4b523291936f8960c514ba6fad4100e893b67db195cf644`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1688f016a09ac412aed8ac075c283501f128abef9696857d645a64c550c669`  
		Last Modified: Thu, 12 Dec 2024 05:33:07 GMT  
		Size: 19.9 KB (19881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabab48893d974e79a79888fc6df380c6dcf350a41715045f49febecefddffeb`  
		Last Modified: Fri, 13 Dec 2024 00:49:21 GMT  
		Size: 31.0 MB (31000601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede30cfb10bc21715eab17b816b53c120038851e557f760c598e7ce4e84e9148`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31f87b8020fbedb15dfb281c219e43c304b3143e7514d43ef00c5071b2db008`  
		Last Modified: Fri, 13 Dec 2024 00:54:26 GMT  
		Size: 1.2 MB (1216846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa73d9236be884be92d3577f58932ae343b2ba52298cf5d46931b99d53b58ce1`  
		Last Modified: Fri, 13 Dec 2024 00:54:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e72c857244708c8aa47c19384d557c44395c05110c348a78f75ab5c69d3dbd`  
		Last Modified: Fri, 13 Dec 2024 00:54:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:35694c527d101786faa78cd5c8f5c2e1d6ef2e28174b5342490a4e60cbb5eded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a412cc8edeb98c8f408100065e448b22b697ba88376520bc00625fb51494280c`

```dockerfile
```

-	Layers:
	-	`sha256:0ae29bd8c0761e4049dabcba5bd5ace3f8c276657017eb6c36b677871b5d99a3`  
		Last Modified: Fri, 13 Dec 2024 00:54:26 GMT  
		Size: 2.2 MB (2159620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f77f0951d08b4fb34050e4a3bf83d4127b06f892b32e434b0cf9b504397ed1b`  
		Last Modified: Fri, 13 Dec 2024 00:54:25 GMT  
		Size: 30.7 KB (30709 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:203c510a1b28317b19747a357222bb6482aacd40c1a44322e5518763c28f768d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75478982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee7ecfc49d6c78cadc734cdbadd544a60b2b53d349b2b0ec0983bc0f714c8b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b02d148e9caeb82d2cf6c286e6c9c576dbce389f6c2cb18910b789ebd4813`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 3.6 MB (3561751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d561dc5f913bf5ac5c30d9c4d42bdf7aa341b8fba0e0ded0354c6e1aca173438`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465f443f2fadb2b0191af2eb2aae7a8ff4e66fef38973f7b9f36688fc1ff5cc`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167bd40a3a9b1f0b21e6140078bd769d2d967f4713b5f34ccb482a4b419592fe`  
		Last Modified: Fri, 20 Dec 2024 22:04:11 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd8774ef9fa0dca490b5d556eec80cd22fa38fbd2ad90d593168cffab7f95de`  
		Last Modified: Fri, 20 Dec 2024 22:04:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0154e3b89ce7965e82ffec7aff04edec326644e952fe96eca0cbe395ccb151b8`  
		Last Modified: Sat, 21 Dec 2024 01:07:03 GMT  
		Size: 21.9 MB (21867735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1a08d85e9f5ffb6b386d5b9a9c2260779e2408eb44cf874b23d61902f877a`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946fabb80ac5e81a3ba1e80ef02c503fa9257fd27f28ce77c24815e131b7f5bf`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cae5d9bba6d84260838c31aac6e5cc01aadf2ab697ab41df33ab9508312e2e1`  
		Last Modified: Sat, 21 Dec 2024 02:09:57 GMT  
		Size: 31.7 MB (31675723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1671f7a4b9055dd3f4c65b5f95cca757e39df07b78b85cd25865c7838f093`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddecc87c862574fba1558e8e8d387ccc316566f1fd3a319b33adc44ef5f0633b`  
		Last Modified: Sat, 21 Dec 2024 02:11:07 GMT  
		Size: 1.3 MB (1298985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced976e9e84b3f9f81d527553fffcbf38ab11557dd8214d08a01101a2efc31aa`  
		Last Modified: Sat, 21 Dec 2024 02:11:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03d2fb37f9dcd370dbff1c415a899ca81d9ddcd5710cb0a64048f6db1889831`  
		Last Modified: Sat, 21 Dec 2024 02:11:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:0197c57da756af1cb04786935966c3952d4b5ae422058fe8228e8cd6620bf3a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76aee25416c6d2e0557c52851b5ef756eb17c81dde17010d6c40bdeecdaf11e1`

```dockerfile
```

-	Layers:
	-	`sha256:5902f8dd88c5dd12fc53080f9e72e26b7a7556c922cfd0024b26804ad6014ddb`  
		Last Modified: Sat, 21 Dec 2024 02:11:07 GMT  
		Size: 2.2 MB (2156338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8765fd135abaa8d0c08622dd7932ae1050aedcef136b69ed94ce978a82ad8e`  
		Last Modified: Sat, 21 Dec 2024 02:11:07 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:e99e61410cb87423abfc27501618836e8f7e2854c03edee9ef25f3ec3b139fbd
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
$ docker pull composer@sha256:f6f2f0df04f62f7dd02c747b1d0c9161df399c52c540f9a7852d086ecdfa6193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74622834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261b67752a8421c1bf84ddae7bc9562583567a7791b75d8d2c37b7dd608b2be5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926a903e79620f0a500e6c0b8920613cf3e77ee6fb031d64dfb3cb7d88442adc`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 3.3 MB (3336077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c946fba36f12b591be4b090159dd42766dc43c2a20caf28d504ef17c4491759`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac17bc9a4d3a9a1781e2999ce34426d9eec4eed120cb79c459b841169a923918`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8b186c29f3bb1fcde6dd416dd06bb7c990d07b2c9d4621ce4e8f93c94b835d`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 13.6 MB (13580495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e6cdee304691570c26af03b2fedb4dd8016faa742d307b7db946e6409f326`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27e6ddc32c5ab1579764b32caa4c52c636d33a510c4c3ef4495726c95381872`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.9 MB (20883408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7be51eeb9ec7eea5691039e5a979e9ae08b3c661c6e02bf44451ec261ec5b9`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c0be2943e6e61d571707b0255ead75b0198314874eefbdb3bfb8250db6c13e`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.1 KB (20064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8929cf6910012f550931620ff33afa2a5eeb28951deb94cf77e02da91edc9c`  
		Last Modified: Fri, 20 Dec 2024 22:34:02 GMT  
		Size: 31.9 MB (31896315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592305bd0b09f3f4bf2abb5855fd7df7d7f38228b07839e62d8e4c99b7aa2453`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de74cf125483e009cead30c88117a3784c581fdfe312f6dfef20d93a28be902`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 1.3 MB (1257179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1230cc481b09e600355d743ccf5f1ef1f6133229329f2864d85a1bb6b8e36f`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517e54ceb37a099c3ab292f6a687964a4b0f7deb256c639398b85b33a51d55cb`  
		Last Modified: Fri, 20 Dec 2024 22:34:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:8e2293cec65d5af2bce53e9d9c79a4e9b9c56ed918b26874183fedd670ee7b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f301b33fe54b95266bf217f0f4ece38deaaa6376f1c66ef65e59f211dac466`

```dockerfile
```

-	Layers:
	-	`sha256:8e60d3fd23d48da6b3c8aabe4d800e729d1b7e7372c58d4f11fa93a45f405f06`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 2.2 MB (2159053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c700f9717dba9c5e80b2338ffc409ed5df47fd980aa794754c9d0a6626ee297a`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v6

```console
$ docker pull composer@sha256:75475c855c43a508fb3aa5c1a12be942dbb4a753da6620df57d46e85bf7c241e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71747441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad773af411c2e3b099e57ce2dc103384f8f3cc17658dcf1d4462e2c988bf210b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b736a50b989ce147c8a50cd4eff3990052fbae41313316dd15bdd3ae41bb055`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 3.3 MB (3302897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520076a7063b8a800f7aeb276beb6363fa2c2192a17d803ee3f5fa20b0b0b211`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065854d8dae5a225e01a05809bd10528e215d02290cc6d9f51d4bc29dc1ac134`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7d8a646b13a1fce87a53e224ba759100c5661201fa77b07c2bb37e766e4399`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 13.6 MB (13580525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e81800135bc7fff5c18dd6a26d344cbcdc0f282ae7198e61803d1b9e97af13`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce8a346ef963d66430f1390abc1b68a4824385373ab05fa645c2aca57b6015`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.5 MB (19498804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eb2dc0afa0290d833b6477da2f88fe368ba4cefd3a8a5ef03f8561794efefa`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf11115b0d6d263d3685a04147a9d95c5179c52b651782cf9289977a6ac1ce`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a3ca09f084e2d996e8974d62fa6bd1b01b2867e5b1a057e00140bad318027d`  
		Last Modified: Fri, 20 Dec 2024 23:03:37 GMT  
		Size: 30.6 MB (30641288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c129606c926c4221d682770c2daaa54b304e77c6d10ac37d86224ded916fede3`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468aa2771d33870aa52d7276e0d644e3b2a0c1d49457facc8f98c48c443e9652`  
		Last Modified: Fri, 20 Dec 2024 23:04:19 GMT  
		Size: 1.3 MB (1331997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceec54fcb2477b469f9dca645219b218dc16b9abef7401105c9053f18e97c13`  
		Last Modified: Thu, 12 Dec 2024 01:10:16 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25de431533dc12c765715f77dcdd288f363c1175640be0767623fa5077aa01db`  
		Last Modified: Fri, 20 Dec 2024 23:04:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:e75d1f065e75f88eb05cd311df26fea5978e9ec42121e65f206cdb6329cf64c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5918d7d29d8b5f624f7408ea116ed719b2c6a9f2c2e39dbe8f4643fca3d7527e`

```dockerfile
```

-	Layers:
	-	`sha256:c448db397a898884cdc65f97cf9d700839beeb272c6b89b11c6d2129251f7296`  
		Last Modified: Fri, 20 Dec 2024 23:04:18 GMT  
		Size: 30.5 KB (30546 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v7

```console
$ docker pull composer@sha256:d6b500646669fefbb84c644e5542bff7e0aa8bed6d96389a33dd5f8fcdef5fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69677494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b34e72c61d28626b8c3d9005b712f42a2aa45b3bc99b2ad6a3109583e1279a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58a80555964d79b4c54d0bc69d1ac3c99d92bfa41dc077ad9039581c976fe1`  
		Last Modified: Wed, 11 Dec 2024 23:35:20 GMT  
		Size: 3.1 MB (3128235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30daf13605f2d1179f6005fb32926b33b8626b9ceb92de019df902d09cedf935`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365fc515397f6962469f3d1c8654b5801822a766158bca2e8a9fa961d78db8`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7b2510a73dde296829d64a7a766b9532e9e98238663d7544fcb11d828edf19`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 13.6 MB (13580531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05cf7b909bafdb9e34f1486d56a868891fed509111b921f6d72259313be2e5`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb18584dfdd2c5e1b16be910211bf58df75bebb8cc948d010bf7dacf1a81b`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 18.4 MB (18447692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af84d6773702a8389925020e1881a84b42b39eea9ebe082e379503372b4a2c6`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302c968087e93f72bd0a3e8da913da2a3b5cc3802ff0de5d389e6740323ef52`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 19.9 KB (19899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71edb0952ef713ac379d22d60a6a0e5e1ab8e1a7e0d6858994829d1584dfa20b`  
		Last Modified: Sat, 21 Dec 2024 00:54:42 GMT  
		Size: 30.2 MB (30150125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdfebf91571a2efa29d6268aafa0080828a4a9bc3ad5ecc7e2b43895774db5f`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3720e5b02237d0aad44cb437f18887d2226c222af60b025389ff8c14abfbf394`  
		Last Modified: Sat, 21 Dec 2024 00:55:21 GMT  
		Size: 1.2 MB (1246114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f638ec92f77aca1364999ec432ce9e6c5597380d8399a3303274811393423`  
		Last Modified: Sat, 21 Dec 2024 00:55:21 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1365514d3ef81faf9888a73d1b9e61f8bb44f75edec1d73e67757889bf4c91`  
		Last Modified: Sat, 21 Dec 2024 00:55:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:e03331179000157e2f3736a4c3a341575489b1c862eca61c26bfe23e192dd224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822fd38c403caac2afadec98a235d9acda9825146f33d156592318ad0982837`

```dockerfile
```

-	Layers:
	-	`sha256:e134f3eddf39bfdc15f41cb9a9a48cf3e0271a0a7f7d59c29d2b17d57f72eec2`  
		Last Modified: Sat, 21 Dec 2024 00:55:21 GMT  
		Size: 2.2 MB (2159369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a62cb3e6c95b15354610328bccb95a16d3c5e9fe205cb63997b5cdc04c1433`  
		Last Modified: Sat, 21 Dec 2024 00:55:20 GMT  
		Size: 30.8 KB (30761 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:6497d9402693041c40abf25999f202c68e0014b26055e0a4b5ca44fca32c4f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75126776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d0828f9a828f17b4ffd93f858f97011ddf1a36d5a80c1465b907e0fd9213b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02eb691f526c59a4feade4837dd3c26533d9fe4c9306da60dc23a30620af346`  
		Last Modified: Wed, 11 Dec 2024 23:34:10 GMT  
		Size: 3.3 MB (3331581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f32f7c87db3a6447e39cf371cb0c2bb2c95f7a814793eff967d2a9a3b95122`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7c12be75768edb813fc94e2e1d2c48d7cb1f4cea2c832026ca6ae796dff9ac`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2737967709483bb9e56014fca897a13fd112c3084028d6543b06a30985537c4e`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 13.6 MB (13580520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b64ce4fbef8321cb5b9a415b540a4baa87078a9d7ee17306f53198aa5c3d6b`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a01d64640e85e99659018a2a9d802c50d724bde24674cd1ace68a407f974cc8`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 20.9 MB (20912964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61930bd78024ed559eceaae6edaa2d5a5396db98ea69ec50e91c0ce227b97848`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e991f93dcb7aadac92e8529d0719e89be0fbb0cc3478b38e16914291fef40b`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8074648689cf1786e687dd5d23af39dfbe621da1270c66591b9671c41a9a8d35`  
		Last Modified: Sat, 21 Dec 2024 01:55:18 GMT  
		Size: 32.0 MB (32002924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafd0942fb02c25d23f08063ad2cbeab093d6cf618b8d1e3da7813080cf0a5d3`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e346e7494cdb07ad315dd65f8d5d2223a530acd24ca34b9fdec5780bef049610`  
		Last Modified: Sat, 21 Dec 2024 01:55:54 GMT  
		Size: 1.3 MB (1280839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327c51b2dbedc95dc22baad8ad83b2a05a8cd5d7cdbdd46b1f255d94dca24b1d`  
		Last Modified: Sat, 21 Dec 2024 01:55:53 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ac0f4203607a86081b60630045eb5fc7a752d91372d470b27e47ac05bc7866`  
		Last Modified: Sat, 21 Dec 2024 01:55:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:e56e9d0cbb9e8ecf718c3bd1e86d25e09b14c298be0b4cc4591336e90e8cc765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6448d96d0d8e03998848e626037099cca38beff91f0303ba11d4ffc87c6b0f56`

```dockerfile
```

-	Layers:
	-	`sha256:b2387690409d58feb678f2ac28ffbf2b75dbca1d3230188db44114230879a03c`  
		Last Modified: Sat, 21 Dec 2024 01:55:54 GMT  
		Size: 2.2 MB (2159193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a2675988e7c1a9db332796528523cd27bd60e7de8da36b10cdf7b63e51e3f9`  
		Last Modified: Sat, 21 Dec 2024 01:55:53 GMT  
		Size: 30.8 KB (30789 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; 386

```console
$ docker pull composer@sha256:b2d7fd0b5df1db249af431ed539d3b4f0b5091f69519a624c55e140fbced11c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54503951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69599ad7c0d061be0c290927c1c0d1f3cf9f71abb21c3a45afc1165689eccb8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c898e29d83e9db370e8891b59d2b75d52becd1c60e7168a6068c60ab70d34d74`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 3.4 MB (3376600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaee1fb0dd467b0c78610a290f1dab2d06cab056e446bcd035ed5a5be5bad5f`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6589c5988c6fb89267a968f26279f8f922579aeafe69c3b3d5c70ff348de1faf`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f212ddee911fee0e94e486cf1d8c16d2e4609a0aca213ae03ef06b0ec953924`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 13.6 MB (13580481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc377b1762be65b8185324b4a83578d3e2bdb568e2370167b8ad00c5b3f2c5e`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dc25b1fb1a50563b2ccab2e97a663fcdf74d01b6d4f08ecdf423a7ec4178c9`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 21.4 MB (21397982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e557dee7812f54a16556ac580967a78aca6fb0c9444067feedb7c2fec0f1cf`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cacd67f7a12349f00be424d47f5a310859feb05ec769add44557c85dc4c045e`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 20.1 KB (20067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ea983c662a4c7aecfe50add16177147526623e4806159e5ca212d77090d131`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 11.4 MB (11421309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8dee48b1ed735d54e49355cc0e65a8faf12985a8251ee73f1c8c3442801155`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fbb9304d79110f6d7b0d97131342d7277dd225a13fd092dfe46d2755a8335`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 1.2 MB (1236578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a20b259e8d923b4c7a7ae1f115a9adc979621bb21e7459ec21816af795f3cfd`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0be2475ad4f5b74ecd46e819ab2a6a1d4fa3b97e4c15bcc496c5f28c017d28`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:9517ffcead6082b27ce8c525acba065d895c04dd270459d7c7ff06e3e66c9c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.3 KB (459347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fd9bc47a618474d1625dca96c8b0ac6a59186e22ea746ef815ac9db2de5b76`

```dockerfile
```

-	Layers:
	-	`sha256:3e101185d85c6a49576af10bd051b3a0b737ece4885c6c3dd7e7f4dc334333b0`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 428.7 KB (428711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f06839aed1b1ae33c05655f833803443e3cb075c52713c372314172cbc4325d`  
		Last Modified: Fri, 20 Dec 2024 22:30:38 GMT  
		Size: 30.6 KB (30636 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; ppc64le

```console
$ docker pull composer@sha256:a152483bacfe60aec95718fc0c7d8a3c52832cd5a125487d9406874bb958219e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77195865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d0bc7be25d5a8af0b16f3ae331a06122522618def1458043f7311ca7ab6943`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dab8c9093e7207bf34d7e27bcaf8a12d512bc9a6228a188ccd032ab556c048`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 3.5 MB (3474267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887eff0819f1e81cf0537030ec0eefbed710884b4bdcb74a53300dafe99af22`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d10c33dd4ddf3d7039e24ae3ea2657811b8add42853a37557baa89339c584`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73154329c1c9a418799584abd71b5689505fae8a1fe0c1edf20b4c054fdfa404`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe8613e572e5a00abda95594733a8b015a569e70fcfb60f921b46b1d3b0b4ce`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bfbf1907d341a6d1c62419f97827940bb943dfd0067d8cce4a44af3d1da5c0`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 22.3 MB (22287679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa21b603882a7aa1280eb0a92a0814e2acb781ef4ea1490d6871b2cf300d5ed`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b46dc3369c678c5f6e91da763573d92319716e4238a641860950d083934a3b`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320193b91948f33c75121c293867d724d3bd3982783314901a94db790aab8942`  
		Last Modified: Sat, 21 Dec 2024 00:47:37 GMT  
		Size: 32.9 MB (32943931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87a05827ee97083cff81d981bb3bc249115eff0447c4e4a7b65127727301f1c`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1609958598829cbb95f942c795946be9e69aec96f8b4ecf911d7d9805c58dc9`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 1.3 MB (1307604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14939a9b7c36211dc15f90c4fa60b9b7167d2567826d8b79b6ccb97e59becf3d`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e662a9b885b617d41c5e59a01fc02bb6697ecc8dab3257c507d5e52f645bf9e4`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:6231a1f92fbab53bf8eca89fea472ffce39eca25a1afecc239146b7f1d350eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357fa3b6ad00541c405e4cf6a47938cd5c46eaf3b2babe60ea579a8b02d8790c`

```dockerfile
```

-	Layers:
	-	`sha256:9548a136be27d24de779000b4ba818228a62ffd301f27ca677af58f260afae5d`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 2.2 MB (2157610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ca6a526ae0512535d3d1547dd8a9183a0eb4d96ccf4808947c97a6beba7c0d1`  
		Last Modified: Sat, 21 Dec 2024 00:48:47 GMT  
		Size: 30.7 KB (30709 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; riscv64

```console
$ docker pull composer@sha256:8bc890682a436777508adbfe1428a5ebd4329b4024c25b84371c11bb596f19b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72928818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837d8435881ee9fd2c3bb91d5196af59945048fcc13deb02f0029921533fb3d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
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
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65b4aeb40f99d5493f73d9206995a90aa94768378fa8ed5e3d1bfa1a5650e5`  
		Last Modified: Thu, 12 Dec 2024 05:33:08 GMT  
		Size: 13.6 MB (13573066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3a97d778691306fc952ddd90fe8250103f76d9aeb4d0203ae146e8e521bae`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087168628cd777dcb9b702d528d92efb821d834b9f0dcd8c3797efb04ae1c3b9`  
		Last Modified: Thu, 12 Dec 2024 05:33:09 GMT  
		Size: 20.3 MB (20313768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df21e8373b5877a4b523291936f8960c514ba6fad4100e893b67db195cf644`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1688f016a09ac412aed8ac075c283501f128abef9696857d645a64c550c669`  
		Last Modified: Thu, 12 Dec 2024 05:33:07 GMT  
		Size: 19.9 KB (19881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabab48893d974e79a79888fc6df380c6dcf350a41715045f49febecefddffeb`  
		Last Modified: Fri, 13 Dec 2024 00:49:21 GMT  
		Size: 31.0 MB (31000601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede30cfb10bc21715eab17b816b53c120038851e557f760c598e7ce4e84e9148`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31f87b8020fbedb15dfb281c219e43c304b3143e7514d43ef00c5071b2db008`  
		Last Modified: Fri, 13 Dec 2024 00:54:26 GMT  
		Size: 1.2 MB (1216846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa73d9236be884be92d3577f58932ae343b2ba52298cf5d46931b99d53b58ce1`  
		Last Modified: Fri, 13 Dec 2024 00:54:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e72c857244708c8aa47c19384d557c44395c05110c348a78f75ab5c69d3dbd`  
		Last Modified: Fri, 13 Dec 2024 00:54:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:35694c527d101786faa78cd5c8f5c2e1d6ef2e28174b5342490a4e60cbb5eded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a412cc8edeb98c8f408100065e448b22b697ba88376520bc00625fb51494280c`

```dockerfile
```

-	Layers:
	-	`sha256:0ae29bd8c0761e4049dabcba5bd5ace3f8c276657017eb6c36b677871b5d99a3`  
		Last Modified: Fri, 13 Dec 2024 00:54:26 GMT  
		Size: 2.2 MB (2159620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f77f0951d08b4fb34050e4a3bf83d4127b06f892b32e434b0cf9b504397ed1b`  
		Last Modified: Fri, 13 Dec 2024 00:54:25 GMT  
		Size: 30.7 KB (30709 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; s390x

```console
$ docker pull composer@sha256:203c510a1b28317b19747a357222bb6482aacd40c1a44322e5518763c28f768d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75478982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee7ecfc49d6c78cadc734cdbadd544a60b2b53d349b2b0ec0983bc0f714c8b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
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
ENV PHP_VERSION=8.4.2
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b02d148e9caeb82d2cf6c286e6c9c576dbce389f6c2cb18910b789ebd4813`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 3.6 MB (3561751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d561dc5f913bf5ac5c30d9c4d42bdf7aa341b8fba0e0ded0354c6e1aca173438`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465f443f2fadb2b0191af2eb2aae7a8ff4e66fef38973f7b9f36688fc1ff5cc`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167bd40a3a9b1f0b21e6140078bd769d2d967f4713b5f34ccb482a4b419592fe`  
		Last Modified: Fri, 20 Dec 2024 22:04:11 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd8774ef9fa0dca490b5d556eec80cd22fa38fbd2ad90d593168cffab7f95de`  
		Last Modified: Fri, 20 Dec 2024 22:04:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0154e3b89ce7965e82ffec7aff04edec326644e952fe96eca0cbe395ccb151b8`  
		Last Modified: Sat, 21 Dec 2024 01:07:03 GMT  
		Size: 21.9 MB (21867735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1a08d85e9f5ffb6b386d5b9a9c2260779e2408eb44cf874b23d61902f877a`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946fabb80ac5e81a3ba1e80ef02c503fa9257fd27f28ce77c24815e131b7f5bf`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cae5d9bba6d84260838c31aac6e5cc01aadf2ab697ab41df33ab9508312e2e1`  
		Last Modified: Sat, 21 Dec 2024 02:09:57 GMT  
		Size: 31.7 MB (31675723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1671f7a4b9055dd3f4c65b5f95cca757e39df07b78b85cd25865c7838f093`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddecc87c862574fba1558e8e8d387ccc316566f1fd3a319b33adc44ef5f0633b`  
		Last Modified: Sat, 21 Dec 2024 02:11:07 GMT  
		Size: 1.3 MB (1298985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced976e9e84b3f9f81d527553fffcbf38ab11557dd8214d08a01101a2efc31aa`  
		Last Modified: Sat, 21 Dec 2024 02:11:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03d2fb37f9dcd370dbff1c415a899ca81d9ddcd5710cb0a64048f6db1889831`  
		Last Modified: Sat, 21 Dec 2024 02:11:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:0197c57da756af1cb04786935966c3952d4b5ae422058fe8228e8cd6620bf3a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76aee25416c6d2e0557c52851b5ef756eb17c81dde17010d6c40bdeecdaf11e1`

```dockerfile
```

-	Layers:
	-	`sha256:5902f8dd88c5dd12fc53080f9e72e26b7a7556c922cfd0024b26804ad6014ddb`  
		Last Modified: Sat, 21 Dec 2024 02:11:07 GMT  
		Size: 2.2 MB (2156338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8765fd135abaa8d0c08622dd7932ae1050aedcef136b69ed94ce978a82ad8e`  
		Last Modified: Sat, 21 Dec 2024 02:11:07 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:e49da3f473cf06fe694d7a578139f9ab3914f99fa406719109e7b171e059c08b
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
$ docker pull composer@sha256:e1b1c84478b74b1efb6c04d343cab7cdc69d8062b0538f6133ee96646e79104a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74853762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597f41083011e7bbca4e999c9fd285d81a3967eec31e4a4a1c482f0bcc8bcc68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926a903e79620f0a500e6c0b8920613cf3e77ee6fb031d64dfb3cb7d88442adc`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 3.3 MB (3336077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c946fba36f12b591be4b090159dd42766dc43c2a20caf28d504ef17c4491759`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac17bc9a4d3a9a1781e2999ce34426d9eec4eed120cb79c459b841169a923918`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8b186c29f3bb1fcde6dd416dd06bb7c990d07b2c9d4621ce4e8f93c94b835d`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 13.6 MB (13580495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e6cdee304691570c26af03b2fedb4dd8016faa742d307b7db946e6409f326`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27e6ddc32c5ab1579764b32caa4c52c636d33a510c4c3ef4495726c95381872`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.9 MB (20883408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7be51eeb9ec7eea5691039e5a979e9ae08b3c661c6e02bf44451ec261ec5b9`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c0be2943e6e61d571707b0255ead75b0198314874eefbdb3bfb8250db6c13e`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.1 KB (20064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566d18b93401424f6cbd928683adce9bf3ad82d0c304ecdb5761a031816caef6`  
		Last Modified: Fri, 20 Dec 2024 22:34:02 GMT  
		Size: 31.9 MB (31896290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592305bd0b09f3f4bf2abb5855fd7df7d7f38228b07839e62d8e4c99b7aa2453`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd129105385812e3d55bf1615ec40c334a459673a418d707df045a6139fdd96d`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 1.5 MB (1488122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91863bfb83d08b6151d9eaf8526a248b3af1ec3c748e87e93ae85a86dfdb53b`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517e54ceb37a099c3ab292f6a687964a4b0f7deb256c639398b85b33a51d55cb`  
		Last Modified: Fri, 20 Dec 2024 22:34:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:a923dedf7d089ffaddcad108756321cf5522ceece1700cf8fbd9625c918832c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c869ce6d6d541495dbae65bc4a0904de1854d78ca6f3d89cefd76eff7d59f212`

```dockerfile
```

-	Layers:
	-	`sha256:7b8df0015a446dc0086c8af311be236d57ebc2e27e15c8831e1a4e8b64591469`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 2.2 MB (2160547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db96c01aae65a4f474d876df088ecb013979b265d64fbb862820ca60a1d1507e`  
		Last Modified: Fri, 20 Dec 2024 22:34:00 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:5a901315d4c2bde5aa784104687bd50cfa9682b30b65a2ab66c2411f29470162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71975950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6f809430e63fc4ad150cc0cfa23da73d68f8d61240050a10a82e2d26d3a519`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b736a50b989ce147c8a50cd4eff3990052fbae41313316dd15bdd3ae41bb055`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 3.3 MB (3302897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520076a7063b8a800f7aeb276beb6363fa2c2192a17d803ee3f5fa20b0b0b211`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065854d8dae5a225e01a05809bd10528e215d02290cc6d9f51d4bc29dc1ac134`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7d8a646b13a1fce87a53e224ba759100c5661201fa77b07c2bb37e766e4399`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 13.6 MB (13580525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e81800135bc7fff5c18dd6a26d344cbcdc0f282ae7198e61803d1b9e97af13`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce8a346ef963d66430f1390abc1b68a4824385373ab05fa645c2aca57b6015`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.5 MB (19498804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eb2dc0afa0290d833b6477da2f88fe368ba4cefd3a8a5ef03f8561794efefa`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf11115b0d6d263d3685a04147a9d95c5179c52b651782cf9289977a6ac1ce`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a3ca09f084e2d996e8974d62fa6bd1b01b2867e5b1a057e00140bad318027d`  
		Last Modified: Fri, 20 Dec 2024 23:03:37 GMT  
		Size: 30.6 MB (30641288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c129606c926c4221d682770c2daaa54b304e77c6d10ac37d86224ded916fede3`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850dddccd57b27bdb3ca2dc30a6fb50f37cddf2591f3ba6c8f23d7de0e7a37c8`  
		Last Modified: Fri, 20 Dec 2024 23:04:54 GMT  
		Size: 1.6 MB (1560498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3826a6b574a6d595615f31b1ef9fae34a30dd1e418f79cee3bc7ab6a295e46ee`  
		Last Modified: Thu, 12 Dec 2024 19:28:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0626d3b0b278028796aa74a96ca4317a62592130844f13e3e2ac3acee08926aa`  
		Last Modified: Fri, 20 Dec 2024 23:04:53 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:6ad55a5cac64a1d8774c90709313e7e53126e21e45bbbcc671977e64bc8b1e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a3d9f20c6b83f35635d94080a217527ae9ed6e088b06ddc1f6fb6400865382`

```dockerfile
```

-	Layers:
	-	`sha256:a8b43523739b06da6ef40c60b9e3fa25c6202a24e2207b72b2a61b30b93ffa87`  
		Last Modified: Fri, 20 Dec 2024 23:04:53 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:db7e1d13f4f0f64df4e11318b1bfc27abf4689a3ffa2a4a6884941379e7e6cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69910112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d7406f32137829d576557610af675b4d6dc215cb6f02a9d945eeacc3781cd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58a80555964d79b4c54d0bc69d1ac3c99d92bfa41dc077ad9039581c976fe1`  
		Last Modified: Wed, 11 Dec 2024 23:35:20 GMT  
		Size: 3.1 MB (3128235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30daf13605f2d1179f6005fb32926b33b8626b9ceb92de019df902d09cedf935`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365fc515397f6962469f3d1c8654b5801822a766158bca2e8a9fa961d78db8`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7b2510a73dde296829d64a7a766b9532e9e98238663d7544fcb11d828edf19`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 13.6 MB (13580531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05cf7b909bafdb9e34f1486d56a868891fed509111b921f6d72259313be2e5`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb18584dfdd2c5e1b16be910211bf58df75bebb8cc948d010bf7dacf1a81b`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 18.4 MB (18447692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af84d6773702a8389925020e1881a84b42b39eea9ebe082e379503372b4a2c6`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302c968087e93f72bd0a3e8da913da2a3b5cc3802ff0de5d389e6740323ef52`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 19.9 KB (19899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71edb0952ef713ac379d22d60a6a0e5e1ab8e1a7e0d6858994829d1584dfa20b`  
		Last Modified: Sat, 21 Dec 2024 00:54:42 GMT  
		Size: 30.2 MB (30150125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdfebf91571a2efa29d6268aafa0080828a4a9bc3ad5ecc7e2b43895774db5f`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8aea252e0e53d95de52b8c5950ee056175c15143fbc121c31013209c5538a39`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 1.5 MB (1478722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3daab9b2754696fe222ee1f2893595fb1df9ac75c15609ad470c88caf501e8b`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6935c0a0e469ebc6c77c7f9a6b4f6e9e9e014039d2d057ae449266bf779ecfb0`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:a1616e46409e69c41cd4092ee361a3737ff11c8239f8c83144acaf68b187acb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074d3c493c898bdce2c01c34ec8fc7dbecdaf5b3e54323b863f669fc8667da5`

```dockerfile
```

-	Layers:
	-	`sha256:7e72894c6be4cfe667296ed4b53106cd8f218edbfa690f41518be4580405775d`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 2.2 MB (2160871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b62e2ff1b9aa44ff6550b505c92f55ce3b2f7cd0ea8c82649c5b1a4c9b41c9ca`  
		Last Modified: Sat, 21 Dec 2024 00:55:59 GMT  
		Size: 31.1 KB (31063 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:34f7cfafcc6768f84309dd8a37864fcf1a4e8939416c8931b3e4189294f3fc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75356775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636ee04b1d54bfa9b06d6c5b57f8de51413cf9c3b1672d6e6f9c431bed53fc23`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02eb691f526c59a4feade4837dd3c26533d9fe4c9306da60dc23a30620af346`  
		Last Modified: Wed, 11 Dec 2024 23:34:10 GMT  
		Size: 3.3 MB (3331581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f32f7c87db3a6447e39cf371cb0c2bb2c95f7a814793eff967d2a9a3b95122`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7c12be75768edb813fc94e2e1d2c48d7cb1f4cea2c832026ca6ae796dff9ac`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2737967709483bb9e56014fca897a13fd112c3084028d6543b06a30985537c4e`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 13.6 MB (13580520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b64ce4fbef8321cb5b9a415b540a4baa87078a9d7ee17306f53198aa5c3d6b`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a01d64640e85e99659018a2a9d802c50d724bde24674cd1ace68a407f974cc8`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 20.9 MB (20912964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61930bd78024ed559eceaae6edaa2d5a5396db98ea69ec50e91c0ce227b97848`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e991f93dcb7aadac92e8529d0719e89be0fbb0cc3478b38e16914291fef40b`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8074648689cf1786e687dd5d23af39dfbe621da1270c66591b9671c41a9a8d35`  
		Last Modified: Sat, 21 Dec 2024 01:55:18 GMT  
		Size: 32.0 MB (32002924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafd0942fb02c25d23f08063ad2cbeab093d6cf618b8d1e3da7813080cf0a5d3`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad88e37368d020d5a4f8a68e888a81393a07c69b0eefff65a090af38937a05c`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 1.5 MB (1510828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feacd1f5f2d7d620450018862bba088a1512fc3523832e860cb326e795f70605`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d2e662c0b87459a6d5034013826453a6b0afbd406209ce5fb7f5f9e0448460`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:b508f4c6c299c4a997fe4c9e1075a8cdc081617b6f5e94d79b9765f8e84c04e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a902e391fc2bce4bfb8212eafaefeb6a31b207b7e5e8dac5e021d386ddda2d`

```dockerfile
```

-	Layers:
	-	`sha256:bd6a6c91fca34ad1f1e3fd828fc199a78b4b81a76338f8ef7649a9efd37553a9`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 2.2 MB (2160699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23201e21b29c63fe764565ed4ae97d111c5cb614f494736f09cb5ec29c43411`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 31.1 KB (31094 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:13cd3c9d62766d3600c5ece8fc68f3b6c14e455c76cc87f55a92f697117b09a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54734604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef626d096c7b0e5d6ac570116527e30afdb8a372aa6a94ae10d9de7f416d4e65`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c898e29d83e9db370e8891b59d2b75d52becd1c60e7168a6068c60ab70d34d74`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 3.4 MB (3376600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaee1fb0dd467b0c78610a290f1dab2d06cab056e446bcd035ed5a5be5bad5f`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6589c5988c6fb89267a968f26279f8f922579aeafe69c3b3d5c70ff348de1faf`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f212ddee911fee0e94e486cf1d8c16d2e4609a0aca213ae03ef06b0ec953924`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 13.6 MB (13580481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc377b1762be65b8185324b4a83578d3e2bdb568e2370167b8ad00c5b3f2c5e`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dc25b1fb1a50563b2ccab2e97a663fcdf74d01b6d4f08ecdf423a7ec4178c9`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 21.4 MB (21397982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e557dee7812f54a16556ac580967a78aca6fb0c9444067feedb7c2fec0f1cf`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cacd67f7a12349f00be424d47f5a310859feb05ec769add44557c85dc4c045e`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 20.1 KB (20067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06287a9316358b0f72490833a72d6f7e508faa1f3e9b3108819c7e0b7a8030fc`  
		Last Modified: Fri, 20 Dec 2024 22:30:54 GMT  
		Size: 11.4 MB (11421356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3918f2868475d53e64393972d158b9cfa5d0ea9c2911105e6421859b924c19b2`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc78b2a127bd3e7ce50cb76ad940f21a9f0e134013e0297da350caa3ca9c073`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 1.5 MB (1467169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37da3c63d602ee971c9fc9ef89a41b6088e4f7e7eb8022ec5f593eaa0c3fa0aa`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a7c693a6c06c4d9ff1694fb9dfdb0bfe337f4a907a823f36e2cb6f465f7d3f`  
		Last Modified: Fri, 20 Dec 2024 22:30:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:07dc5dfc59e7558508b3f87d5215565024156fdf59cdab60361fb9d20ce0f6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.1 KB (461125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9173980e4148edc00eeb621831580e60c15d42a197e8ead0f3ff4c2d10d36b9c`

```dockerfile
```

-	Layers:
	-	`sha256:76657d0771423cfa4cbd38f6dfc24b8c2abe412fac80284be5ff2addd76a1f32`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 430.2 KB (430200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3397f97a793dc2b9ce6e3abdd4c5468a0a2c70afea3a9ff791553b666147d29a`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 30.9 KB (30925 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:f4f0f620051d42be48776181af565e7851f099b355d518b887d23b60c412804f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77427854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1474f7a9f0d1a42435f12cc71acb12436d8180efa5fec58aa72da53f62466f6e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dab8c9093e7207bf34d7e27bcaf8a12d512bc9a6228a188ccd032ab556c048`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 3.5 MB (3474267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887eff0819f1e81cf0537030ec0eefbed710884b4bdcb74a53300dafe99af22`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d10c33dd4ddf3d7039e24ae3ea2657811b8add42853a37557baa89339c584`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73154329c1c9a418799584abd71b5689505fae8a1fe0c1edf20b4c054fdfa404`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe8613e572e5a00abda95594733a8b015a569e70fcfb60f921b46b1d3b0b4ce`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bfbf1907d341a6d1c62419f97827940bb943dfd0067d8cce4a44af3d1da5c0`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 22.3 MB (22287679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa21b603882a7aa1280eb0a92a0814e2acb781ef4ea1490d6871b2cf300d5ed`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b46dc3369c678c5f6e91da763573d92319716e4238a641860950d083934a3b`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320193b91948f33c75121c293867d724d3bd3982783314901a94db790aab8942`  
		Last Modified: Sat, 21 Dec 2024 00:47:37 GMT  
		Size: 32.9 MB (32943931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87a05827ee97083cff81d981bb3bc249115eff0447c4e4a7b65127727301f1c`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362869a3172835ee4528ea6f2f44bc837ebb8f00e7a773ec2152c108b44cce5`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 1.5 MB (1539584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0469f95a3ee042bb6c8182cadae42ac0814e69524ac25f1f82fb60231d4ff9e`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a0182bc07154bed20d5a39868bb2fef6baa5627b3394984ca31848525ece57`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:59e8871447f1590862034a4aa3d632539f3ccd49edf6adf206a46616eb75a37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ebf547901c22f465b12649dc1cc8394f42b6a0f3fa10edda44e64adb2596a7`

```dockerfile
```

-	Layers:
	-	`sha256:d5823359ef511b41f5b0642517539477214cc9457852442e553b1dc19c7baa36`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 2.2 MB (2159110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a64225a958451c59f6b285afb2cf8db0039c43becec7a9df44fcc5e9287fda31`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:5ed834b87e8853267488e83580cf0efd0895c111918446017496ff1134309d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73159041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c5af21db82ae76f968ea7805d38106e25cfc280fa83e0a0552058c54de85cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
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
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65b4aeb40f99d5493f73d9206995a90aa94768378fa8ed5e3d1bfa1a5650e5`  
		Last Modified: Thu, 12 Dec 2024 05:33:08 GMT  
		Size: 13.6 MB (13573066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3a97d778691306fc952ddd90fe8250103f76d9aeb4d0203ae146e8e521bae`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087168628cd777dcb9b702d528d92efb821d834b9f0dcd8c3797efb04ae1c3b9`  
		Last Modified: Thu, 12 Dec 2024 05:33:09 GMT  
		Size: 20.3 MB (20313768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df21e8373b5877a4b523291936f8960c514ba6fad4100e893b67db195cf644`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1688f016a09ac412aed8ac075c283501f128abef9696857d645a64c550c669`  
		Last Modified: Thu, 12 Dec 2024 05:33:07 GMT  
		Size: 19.9 KB (19881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabab48893d974e79a79888fc6df380c6dcf350a41715045f49febecefddffeb`  
		Last Modified: Fri, 13 Dec 2024 00:49:21 GMT  
		Size: 31.0 MB (31000601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede30cfb10bc21715eab17b816b53c120038851e557f760c598e7ce4e84e9148`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946a7fcdbae57a989822e644601f1206974970f46880c2e4b93b740563d39880`  
		Last Modified: Fri, 13 Dec 2024 00:59:34 GMT  
		Size: 1.4 MB (1447059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e0b1c9377d6f40aa1bb8f77f7ad021c2cd3241936aa4c0070e1b1ddedca5db`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d621471430c14ecb515fd0a1755ef5f2b051d0729f8282b42214828554eccc30`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:1b77539025c2b4710b8f9c8abb0538f9fcd1d0f96079d528748cae96eefcfd2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2192120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4f29f2a4f548644ac52a500f1010b22e711fd4bc25d2179d348fe11c7b972e`

```dockerfile
```

-	Layers:
	-	`sha256:91caba4aa4b89b7471b15c276d6031e7253d025fb171f6a34066c214dd2068ae`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 2.2 MB (2161111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff1e0fa372986ca5902d81a83654c9d2e1e54a86b765e66b939114b561954fb`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:c08937ec02e7e3a8ba10b293a2d6bcafa3b7437f40a857fa7d1ab9ffeeb70680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75708713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185a38213023f1563ca995da494862924414e2c5244e2f344a8ec11bb37db3b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b02d148e9caeb82d2cf6c286e6c9c576dbce389f6c2cb18910b789ebd4813`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 3.6 MB (3561751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d561dc5f913bf5ac5c30d9c4d42bdf7aa341b8fba0e0ded0354c6e1aca173438`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465f443f2fadb2b0191af2eb2aae7a8ff4e66fef38973f7b9f36688fc1ff5cc`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167bd40a3a9b1f0b21e6140078bd769d2d967f4713b5f34ccb482a4b419592fe`  
		Last Modified: Fri, 20 Dec 2024 22:04:11 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd8774ef9fa0dca490b5d556eec80cd22fa38fbd2ad90d593168cffab7f95de`  
		Last Modified: Fri, 20 Dec 2024 22:04:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0154e3b89ce7965e82ffec7aff04edec326644e952fe96eca0cbe395ccb151b8`  
		Last Modified: Sat, 21 Dec 2024 01:07:03 GMT  
		Size: 21.9 MB (21867735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1a08d85e9f5ffb6b386d5b9a9c2260779e2408eb44cf874b23d61902f877a`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946fabb80ac5e81a3ba1e80ef02c503fa9257fd27f28ce77c24815e131b7f5bf`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cae5d9bba6d84260838c31aac6e5cc01aadf2ab697ab41df33ab9508312e2e1`  
		Last Modified: Sat, 21 Dec 2024 02:09:57 GMT  
		Size: 31.7 MB (31675723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1671f7a4b9055dd3f4c65b5f95cca757e39df07b78b85cd25865c7838f093`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6ea88506192fb2d0baa91e5c3ada4bd20b1007a7b0277404c092157519e1b4`  
		Last Modified: Sat, 21 Dec 2024 02:12:02 GMT  
		Size: 1.5 MB (1528705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c72de6015442cbef85c552a342409109175a5376f5e79acf9c56ee0dbbf495`  
		Last Modified: Sat, 21 Dec 2024 02:12:02 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dc08e4de24064ddc8c3fd37d73f66dce40dbe19b0ef56201d08671a7f2b901`  
		Last Modified: Sat, 21 Dec 2024 02:12:02 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:30a7adf0e400d70aa2347c9da2933cd55a90f800342b6f7109c86e4713c3e030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de56b26de8ffcb4f1353b74a2869b153a008d19e2db66e41cc749e7dba1f4481`

```dockerfile
```

-	Layers:
	-	`sha256:9b18a7df2365282d6bf26c5769e70e2c588af609e15f2fe2c9fa9b22b8759f73`  
		Last Modified: Sat, 21 Dec 2024 02:12:01 GMT  
		Size: 2.2 MB (2157832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881e3365eca7edb3a1b4748699a6523ca26215cf704dcd0d07de0b3edafc55b7`  
		Last Modified: Sat, 21 Dec 2024 02:12:01 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:83e7a817513a79b47ff105232417e3bd427cc91b4e04c0120af8d350c1f05b0a
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
$ docker pull composer@sha256:86715a9902c34da8b1a386da4f3620dc408719bc13c8e564a9ec59c980321809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74711677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc6137bd729ce1e7c590a7cbbc3971e242c2678b80e1019b1eaaa5990bed954`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926a903e79620f0a500e6c0b8920613cf3e77ee6fb031d64dfb3cb7d88442adc`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 3.3 MB (3336077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c946fba36f12b591be4b090159dd42766dc43c2a20caf28d504ef17c4491759`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac17bc9a4d3a9a1781e2999ce34426d9eec4eed120cb79c459b841169a923918`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8b186c29f3bb1fcde6dd416dd06bb7c990d07b2c9d4621ce4e8f93c94b835d`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 13.6 MB (13580495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e6cdee304691570c26af03b2fedb4dd8016faa742d307b7db946e6409f326`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27e6ddc32c5ab1579764b32caa4c52c636d33a510c4c3ef4495726c95381872`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.9 MB (20883408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7be51eeb9ec7eea5691039e5a979e9ae08b3c661c6e02bf44451ec261ec5b9`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c0be2943e6e61d571707b0255ead75b0198314874eefbdb3bfb8250db6c13e`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.1 KB (20064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297872bde09879fe8c40c33d24670744d6c17bec4a5ae5813e82e2e3e2226aa2`  
		Last Modified: Fri, 20 Dec 2024 22:33:43 GMT  
		Size: 31.9 MB (31896376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee2060556a2755bde3d1f9ef97928ca996a9803c47290d46626dbc8042d4c5f`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59909d02d551d27004dde96ad05907559b515402eaba5169a7123eacd852e30`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 1.3 MB (1345949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd6ca8b30cf3126e4e29b5036aa4540dadf93174a92aa26d50410b9b96dcbec`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8add366ccdb2fbd941033272751360debaf11d77812bd4e989b280f393ebe28`  
		Last Modified: Fri, 20 Dec 2024 22:33:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:05f8169281cd999bf35f6b343742200edf11de7d21febfe544190d88cd1c3c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b763c0169a3680d8c766871afc239d987faaadd62dc4c92e9dbe40f084289a2`

```dockerfile
```

-	Layers:
	-	`sha256:9159222466972256ebd9c846b95b63fcd4d6f60da3ad15da44e730cd3b8ce237`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 2.2 MB (2160253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827c4480a261b491158b29b2448e6c3cd5d73f3b2a1fdf3ba93d2acc080bd0c1`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:d339b6e27d102bc6a8a2c2d03140e17e4024ca9cdd9e155480a076da471e6235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71831909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b219a5abd047a63931a60c6374218612786c3cbf62cbc326a5e10e26d71d4e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b736a50b989ce147c8a50cd4eff3990052fbae41313316dd15bdd3ae41bb055`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 3.3 MB (3302897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520076a7063b8a800f7aeb276beb6363fa2c2192a17d803ee3f5fa20b0b0b211`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065854d8dae5a225e01a05809bd10528e215d02290cc6d9f51d4bc29dc1ac134`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7d8a646b13a1fce87a53e224ba759100c5661201fa77b07c2bb37e766e4399`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 13.6 MB (13580525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e81800135bc7fff5c18dd6a26d344cbcdc0f282ae7198e61803d1b9e97af13`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce8a346ef963d66430f1390abc1b68a4824385373ab05fa645c2aca57b6015`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.5 MB (19498804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eb2dc0afa0290d833b6477da2f88fe368ba4cefd3a8a5ef03f8561794efefa`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf11115b0d6d263d3685a04147a9d95c5179c52b651782cf9289977a6ac1ce`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a3ca09f084e2d996e8974d62fa6bd1b01b2867e5b1a057e00140bad318027d`  
		Last Modified: Fri, 20 Dec 2024 23:03:37 GMT  
		Size: 30.6 MB (30641288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c129606c926c4221d682770c2daaa54b304e77c6d10ac37d86224ded916fede3`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca357cec05180899d9e8d28334a0e6bc9298b37bca1b6c8c1c400e1a8ff18b0`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 1.4 MB (1416457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d76b9a3e1f7c21e5a182c9d58502bc43af53578e67a16921add85659a9209`  
		Last Modified: Thu, 12 Dec 2024 19:27:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9b049e98e5aa565b7511812e1351103b5e9f811e326eac0f30a2e3743b9c24`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:52cdc68e02a3ba68b8d2d2d8bec512376210abf3254d05aecb56736a8655063d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721d4101af98ce5b00dd62400ad02e9747f8cd2169aba4c3a50cb244f40eff06`

```dockerfile
```

-	Layers:
	-	`sha256:882e75b853bd9635aa0062827bef1e69172eb52c056816b244d9b01cfb964aaf`  
		Last Modified: Fri, 20 Dec 2024 23:03:35 GMT  
		Size: 30.5 KB (30536 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:44b63081db2d7161b0cdf1e553f37c64da6184c348efca14459551e73764049e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69768280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be287281ea2df9d53c487316b05754e7b654a2c80a9a449852731263a34fbc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58a80555964d79b4c54d0bc69d1ac3c99d92bfa41dc077ad9039581c976fe1`  
		Last Modified: Wed, 11 Dec 2024 23:35:20 GMT  
		Size: 3.1 MB (3128235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30daf13605f2d1179f6005fb32926b33b8626b9ceb92de019df902d09cedf935`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365fc515397f6962469f3d1c8654b5801822a766158bca2e8a9fa961d78db8`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7b2510a73dde296829d64a7a766b9532e9e98238663d7544fcb11d828edf19`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 13.6 MB (13580531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05cf7b909bafdb9e34f1486d56a868891fed509111b921f6d72259313be2e5`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb18584dfdd2c5e1b16be910211bf58df75bebb8cc948d010bf7dacf1a81b`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 18.4 MB (18447692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af84d6773702a8389925020e1881a84b42b39eea9ebe082e379503372b4a2c6`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302c968087e93f72bd0a3e8da913da2a3b5cc3802ff0de5d389e6740323ef52`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 19.9 KB (19899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71edb0952ef713ac379d22d60a6a0e5e1ab8e1a7e0d6858994829d1584dfa20b`  
		Last Modified: Sat, 21 Dec 2024 00:54:42 GMT  
		Size: 30.2 MB (30150125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdfebf91571a2efa29d6268aafa0080828a4a9bc3ad5ecc7e2b43895774db5f`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d312a625a9cea21c47b3651da95e34689bc2b048df02e891d27f92700227cbe`  
		Last Modified: Sat, 21 Dec 2024 00:54:41 GMT  
		Size: 1.3 MB (1336889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3b201948d6a81833fdccada5d4e3cf47b4952cee8e2d3e6974c5d9d5d20f66`  
		Last Modified: Sat, 21 Dec 2024 00:54:41 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f64f2a4c489fad4e0d0a64578400ebae97f48ff6414114e2193580823d120a7`  
		Last Modified: Sat, 21 Dec 2024 00:54:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:9ebde0546735c9af7af3e0795d5e659520a8296d53a8d1479d1523df17e4b03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656fc55c2768c519f56d85ad96da27ad71cad8a63f85a5fb611216d0ab47f0a8`

```dockerfile
```

-	Layers:
	-	`sha256:9cace02e0df1fe416cecf8d9e4cacd7b0e661eae776b0196c327aa4a8d9d5813`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 2.2 MB (2160569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cae917344f15fe6c2d3b209cecda6985293409e586c9eb483162cf377c2c8acb`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 30.8 KB (30750 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:dc0c7f531b624ee2477bd1cf49355293d04ddffe21bf6114a95607694ea7feb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75214437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80cdc1c07fb8562711a1ce803be054ec8470d65a5ee7357812f41a7e272d546`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02eb691f526c59a4feade4837dd3c26533d9fe4c9306da60dc23a30620af346`  
		Last Modified: Wed, 11 Dec 2024 23:34:10 GMT  
		Size: 3.3 MB (3331581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f32f7c87db3a6447e39cf371cb0c2bb2c95f7a814793eff967d2a9a3b95122`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7c12be75768edb813fc94e2e1d2c48d7cb1f4cea2c832026ca6ae796dff9ac`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2737967709483bb9e56014fca897a13fd112c3084028d6543b06a30985537c4e`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 13.6 MB (13580520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b64ce4fbef8321cb5b9a415b540a4baa87078a9d7ee17306f53198aa5c3d6b`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a01d64640e85e99659018a2a9d802c50d724bde24674cd1ace68a407f974cc8`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 20.9 MB (20912964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61930bd78024ed559eceaae6edaa2d5a5396db98ea69ec50e91c0ce227b97848`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e991f93dcb7aadac92e8529d0719e89be0fbb0cc3478b38e16914291fef40b`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8074648689cf1786e687dd5d23af39dfbe621da1270c66591b9671c41a9a8d35`  
		Last Modified: Sat, 21 Dec 2024 01:55:18 GMT  
		Size: 32.0 MB (32002924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafd0942fb02c25d23f08063ad2cbeab093d6cf618b8d1e3da7813080cf0a5d3`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbc1bdc44e9a45913e2c17420d5f0c504ad83620bb6aa1a544f6a6608694652`  
		Last Modified: Sat, 21 Dec 2024 01:55:17 GMT  
		Size: 1.4 MB (1368492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25613c051b7489fcf2c3b4ae8295ffdcd74e959353d1a2f93d7c8e645d2fdf8e`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29a8df97712a4eb0f354b2d611f7a2dad77ca4e5c2e01bb399a9a9fd735bc62`  
		Last Modified: Sat, 21 Dec 2024 01:55:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:bea8151175d39d5d94a2809339eb42d48eaa49c4d008cc0741bbd2ba97097379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190e8eab0e89ebd0cacb63889de9557f839863ab662253d51e4900933ca35c1b`

```dockerfile
```

-	Layers:
	-	`sha256:77b9b330d91ca7cb9e2fb6eea92938e4d38194a237b8bf6ec9fc78cbe304cd90`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 2.2 MB (2160393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edec463ea7ad2f12e75b14fa0f1f42f016e6597e5a6659e5cabfdd835ee8829f`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 30.8 KB (30779 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:45d1ecb99b2afaba6acc6b3650ec06cce0afe613523117a450d7ec301f328cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54591872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556f31a880ba642d0d47f607f2cf125f5a8cb888d8658e53912dd7cb425dd255`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c898e29d83e9db370e8891b59d2b75d52becd1c60e7168a6068c60ab70d34d74`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 3.4 MB (3376600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaee1fb0dd467b0c78610a290f1dab2d06cab056e446bcd035ed5a5be5bad5f`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6589c5988c6fb89267a968f26279f8f922579aeafe69c3b3d5c70ff348de1faf`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f212ddee911fee0e94e486cf1d8c16d2e4609a0aca213ae03ef06b0ec953924`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 13.6 MB (13580481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc377b1762be65b8185324b4a83578d3e2bdb568e2370167b8ad00c5b3f2c5e`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dc25b1fb1a50563b2ccab2e97a663fcdf74d01b6d4f08ecdf423a7ec4178c9`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 21.4 MB (21397982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e557dee7812f54a16556ac580967a78aca6fb0c9444067feedb7c2fec0f1cf`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cacd67f7a12349f00be424d47f5a310859feb05ec769add44557c85dc4c045e`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 20.1 KB (20067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23849d787e1a192bfd435c7fd7263c32435e87bd9d1fcbb9a4ae64a8f665d79f`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 11.4 MB (11421351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e11a704e653b95e9384311dd22ed4490a9a261e61d75660e76d9f67171b51f4`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af06b16830c267b956c54985affd5e7e43886fa2db245a39455ef078ad59e0`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 1.3 MB (1324445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f381b382e9ef1c58cffe5cbc61320a8e30721f2ede50059f17a2383f5befb7b`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d65102e5cbe1b6da82da528a5ad8d68921fd640fb933287d532f7ac4ef4878`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:ec9667f00c779b238bfaefd66a78952fcde3bd9e5a9d8b1f2a3434312fd45569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.5 KB (460537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2729d97b615f55eca06802c4c971107b63b89901a2175a96e049a48b01c94e56`

```dockerfile
```

-	Layers:
	-	`sha256:1788379821db1185f48672b130491ba6d2d4067eaa209d11071dd6e1591287ff`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 429.9 KB (429911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:793216d1cfe51d743a89fafc072b11087b8a3ea64df5a5c1d87b7c991424983b`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 30.6 KB (30626 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:39d47fddadebde46b5aa075b7b188488c77cd2fc5f78a482fbca5f8720e07784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9de5a09e6d5b3430ae020ddd9ad018e18cf2a612e13bf084f41785555ab912`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dab8c9093e7207bf34d7e27bcaf8a12d512bc9a6228a188ccd032ab556c048`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 3.5 MB (3474267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887eff0819f1e81cf0537030ec0eefbed710884b4bdcb74a53300dafe99af22`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d10c33dd4ddf3d7039e24ae3ea2657811b8add42853a37557baa89339c584`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73154329c1c9a418799584abd71b5689505fae8a1fe0c1edf20b4c054fdfa404`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe8613e572e5a00abda95594733a8b015a569e70fcfb60f921b46b1d3b0b4ce`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bfbf1907d341a6d1c62419f97827940bb943dfd0067d8cce4a44af3d1da5c0`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 22.3 MB (22287679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa21b603882a7aa1280eb0a92a0814e2acb781ef4ea1490d6871b2cf300d5ed`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b46dc3369c678c5f6e91da763573d92319716e4238a641860950d083934a3b`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320193b91948f33c75121c293867d724d3bd3982783314901a94db790aab8942`  
		Last Modified: Sat, 21 Dec 2024 00:47:37 GMT  
		Size: 32.9 MB (32943931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87a05827ee97083cff81d981bb3bc249115eff0447c4e4a7b65127727301f1c`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778809ac255a2d2ab7079bc8a84f7d2579eaa233a12aca89aa7bf87896b5853d`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 1.4 MB (1397690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d11e35988aedb4751dff69d03dda5e5372863af4a4f321bd35a2f249e2b9c3`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c494da996fb65daf0576665a803766cee732247601e416c96ecc6737c15d3242`  
		Last Modified: Sat, 21 Dec 2024 00:47:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:10851df2bb02f14a5d955ff5ee65aa6ccab36c724f71ce5e0f5bcffe198a592c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4228d46f61af59517ae32ece45efd921551f57cc01b81cea728b3989e3274692`

```dockerfile
```

-	Layers:
	-	`sha256:f6c18dc1eff360e59b3049c77febe8d09fadd373dc6c07021d937f971eda16ec`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 2.2 MB (2158810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c80bb77f9349195e9186f11e18f9830292abd319b18227f24b1f5a28246e4b3`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:47b8462c8ed5b32076b9992c2fca053d9e419ffb51d4f123ffedef94cce62e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73015557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccd019c062510ff8af4860bd81975195ec2de6183e87262123beca4fbc95d80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
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
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65b4aeb40f99d5493f73d9206995a90aa94768378fa8ed5e3d1bfa1a5650e5`  
		Last Modified: Thu, 12 Dec 2024 05:33:08 GMT  
		Size: 13.6 MB (13573066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3a97d778691306fc952ddd90fe8250103f76d9aeb4d0203ae146e8e521bae`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087168628cd777dcb9b702d528d92efb821d834b9f0dcd8c3797efb04ae1c3b9`  
		Last Modified: Thu, 12 Dec 2024 05:33:09 GMT  
		Size: 20.3 MB (20313768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df21e8373b5877a4b523291936f8960c514ba6fad4100e893b67db195cf644`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1688f016a09ac412aed8ac075c283501f128abef9696857d645a64c550c669`  
		Last Modified: Thu, 12 Dec 2024 05:33:07 GMT  
		Size: 19.9 KB (19881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabab48893d974e79a79888fc6df380c6dcf350a41715045f49febecefddffeb`  
		Last Modified: Fri, 13 Dec 2024 00:49:21 GMT  
		Size: 31.0 MB (31000601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede30cfb10bc21715eab17b816b53c120038851e557f760c598e7ce4e84e9148`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc06b5c0e3074b70e86182bbadb2eede36867ac1f673a3327193ccdc65412142`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 1.3 MB (1303577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ef1a692089e1b772a12c12bade7cfdc0ca04dbb8115b0ccb080b1166f58f65`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1fd3d6f31b8ed05d003559b7a561f07659b81dc8e1d9ffa5157b6ad068b351`  
		Last Modified: Fri, 13 Dec 2024 00:49:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:be33fe14c76b8ffb0df7d3b9ba205626a3aef71c9f13827819a643c1412ea57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f861530adf2f03c926a23437974a7e17a7755fdf0924ec5195013be2de3ae`

```dockerfile
```

-	Layers:
	-	`sha256:d20c559f6d17c094e1f4f0d0a431f3d1d96c89f862133f0c09bd60516e621b46`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 2.2 MB (2160811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb521b49d1ee3611c2f351b8614014b608f44c92cecb932c920a0e5f4252693`  
		Last Modified: Fri, 13 Dec 2024 00:49:16 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:4f81a8cc27005ca20ff31502d4a6c730ebdde93ab3c818e9a949744a2a4fe471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75563374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47b7f75693b368d37da5356369d307a6330ec3a41005305220a6f93e3dc3662`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b02d148e9caeb82d2cf6c286e6c9c576dbce389f6c2cb18910b789ebd4813`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 3.6 MB (3561751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d561dc5f913bf5ac5c30d9c4d42bdf7aa341b8fba0e0ded0354c6e1aca173438`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465f443f2fadb2b0191af2eb2aae7a8ff4e66fef38973f7b9f36688fc1ff5cc`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167bd40a3a9b1f0b21e6140078bd769d2d967f4713b5f34ccb482a4b419592fe`  
		Last Modified: Fri, 20 Dec 2024 22:04:11 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd8774ef9fa0dca490b5d556eec80cd22fa38fbd2ad90d593168cffab7f95de`  
		Last Modified: Fri, 20 Dec 2024 22:04:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0154e3b89ce7965e82ffec7aff04edec326644e952fe96eca0cbe395ccb151b8`  
		Last Modified: Sat, 21 Dec 2024 01:07:03 GMT  
		Size: 21.9 MB (21867735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1a08d85e9f5ffb6b386d5b9a9c2260779e2408eb44cf874b23d61902f877a`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946fabb80ac5e81a3ba1e80ef02c503fa9257fd27f28ce77c24815e131b7f5bf`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cae5d9bba6d84260838c31aac6e5cc01aadf2ab697ab41df33ab9508312e2e1`  
		Last Modified: Sat, 21 Dec 2024 02:09:57 GMT  
		Size: 31.7 MB (31675723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1671f7a4b9055dd3f4c65b5f95cca757e39df07b78b85cd25865c7838f093`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a786d406f9afd0e23cf22f180471c74e952824c2f48ebe920d51a5cca6b585`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 1.4 MB (1383367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcda2dd35badb4fcf5b29d84d87d4e2362e1c15e399dbe95174dbbdbbf864d`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bca8707ab38c51cacfdd23547715666185b870f73ac54d0e7369b2a8e2d2e22`  
		Last Modified: Sat, 21 Dec 2024 02:09:57 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:62fc7c8a86c521fc58dd3016471f30e0cdfbfdf55a419f5d33db6e451125c056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff60a4eb8bc2e74bb2a8493fcc3a8be67f97dd609905fac616010f440b1085df`

```dockerfile
```

-	Layers:
	-	`sha256:f4129b7ac05a7aa09cfe96e67a0cb62362c63d083940dbeb50969cd5cf1dc13f`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 2.2 MB (2157538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c905aa4f81f1297ba94ce9655d9a7185d706c0fa849ea968d820b627d7e159`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.25`

```console
$ docker pull composer@sha256:83e7a817513a79b47ff105232417e3bd427cc91b4e04c0120af8d350c1f05b0a
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
$ docker pull composer@sha256:86715a9902c34da8b1a386da4f3620dc408719bc13c8e564a9ec59c980321809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74711677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc6137bd729ce1e7c590a7cbbc3971e242c2678b80e1019b1eaaa5990bed954`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926a903e79620f0a500e6c0b8920613cf3e77ee6fb031d64dfb3cb7d88442adc`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 3.3 MB (3336077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c946fba36f12b591be4b090159dd42766dc43c2a20caf28d504ef17c4491759`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac17bc9a4d3a9a1781e2999ce34426d9eec4eed120cb79c459b841169a923918`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8b186c29f3bb1fcde6dd416dd06bb7c990d07b2c9d4621ce4e8f93c94b835d`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 13.6 MB (13580495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e6cdee304691570c26af03b2fedb4dd8016faa742d307b7db946e6409f326`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27e6ddc32c5ab1579764b32caa4c52c636d33a510c4c3ef4495726c95381872`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.9 MB (20883408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7be51eeb9ec7eea5691039e5a979e9ae08b3c661c6e02bf44451ec261ec5b9`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c0be2943e6e61d571707b0255ead75b0198314874eefbdb3bfb8250db6c13e`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.1 KB (20064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297872bde09879fe8c40c33d24670744d6c17bec4a5ae5813e82e2e3e2226aa2`  
		Last Modified: Fri, 20 Dec 2024 22:33:43 GMT  
		Size: 31.9 MB (31896376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee2060556a2755bde3d1f9ef97928ca996a9803c47290d46626dbc8042d4c5f`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59909d02d551d27004dde96ad05907559b515402eaba5169a7123eacd852e30`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 1.3 MB (1345949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd6ca8b30cf3126e4e29b5036aa4540dadf93174a92aa26d50410b9b96dcbec`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8add366ccdb2fbd941033272751360debaf11d77812bd4e989b280f393ebe28`  
		Last Modified: Fri, 20 Dec 2024 22:33:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:05f8169281cd999bf35f6b343742200edf11de7d21febfe544190d88cd1c3c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b763c0169a3680d8c766871afc239d987faaadd62dc4c92e9dbe40f084289a2`

```dockerfile
```

-	Layers:
	-	`sha256:9159222466972256ebd9c846b95b63fcd4d6f60da3ad15da44e730cd3b8ce237`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 2.2 MB (2160253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827c4480a261b491158b29b2448e6c3cd5d73f3b2a1fdf3ba93d2acc080bd0c1`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v6

```console
$ docker pull composer@sha256:d339b6e27d102bc6a8a2c2d03140e17e4024ca9cdd9e155480a076da471e6235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71831909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b219a5abd047a63931a60c6374218612786c3cbf62cbc326a5e10e26d71d4e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b736a50b989ce147c8a50cd4eff3990052fbae41313316dd15bdd3ae41bb055`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 3.3 MB (3302897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520076a7063b8a800f7aeb276beb6363fa2c2192a17d803ee3f5fa20b0b0b211`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065854d8dae5a225e01a05809bd10528e215d02290cc6d9f51d4bc29dc1ac134`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7d8a646b13a1fce87a53e224ba759100c5661201fa77b07c2bb37e766e4399`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 13.6 MB (13580525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e81800135bc7fff5c18dd6a26d344cbcdc0f282ae7198e61803d1b9e97af13`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce8a346ef963d66430f1390abc1b68a4824385373ab05fa645c2aca57b6015`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.5 MB (19498804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eb2dc0afa0290d833b6477da2f88fe368ba4cefd3a8a5ef03f8561794efefa`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf11115b0d6d263d3685a04147a9d95c5179c52b651782cf9289977a6ac1ce`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a3ca09f084e2d996e8974d62fa6bd1b01b2867e5b1a057e00140bad318027d`  
		Last Modified: Fri, 20 Dec 2024 23:03:37 GMT  
		Size: 30.6 MB (30641288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c129606c926c4221d682770c2daaa54b304e77c6d10ac37d86224ded916fede3`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca357cec05180899d9e8d28334a0e6bc9298b37bca1b6c8c1c400e1a8ff18b0`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 1.4 MB (1416457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d76b9a3e1f7c21e5a182c9d58502bc43af53578e67a16921add85659a9209`  
		Last Modified: Thu, 12 Dec 2024 19:27:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9b049e98e5aa565b7511812e1351103b5e9f811e326eac0f30a2e3743b9c24`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:52cdc68e02a3ba68b8d2d2d8bec512376210abf3254d05aecb56736a8655063d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721d4101af98ce5b00dd62400ad02e9747f8cd2169aba4c3a50cb244f40eff06`

```dockerfile
```

-	Layers:
	-	`sha256:882e75b853bd9635aa0062827bef1e69172eb52c056816b244d9b01cfb964aaf`  
		Last Modified: Fri, 20 Dec 2024 23:03:35 GMT  
		Size: 30.5 KB (30536 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v7

```console
$ docker pull composer@sha256:44b63081db2d7161b0cdf1e553f37c64da6184c348efca14459551e73764049e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69768280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be287281ea2df9d53c487316b05754e7b654a2c80a9a449852731263a34fbc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58a80555964d79b4c54d0bc69d1ac3c99d92bfa41dc077ad9039581c976fe1`  
		Last Modified: Wed, 11 Dec 2024 23:35:20 GMT  
		Size: 3.1 MB (3128235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30daf13605f2d1179f6005fb32926b33b8626b9ceb92de019df902d09cedf935`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365fc515397f6962469f3d1c8654b5801822a766158bca2e8a9fa961d78db8`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7b2510a73dde296829d64a7a766b9532e9e98238663d7544fcb11d828edf19`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 13.6 MB (13580531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05cf7b909bafdb9e34f1486d56a868891fed509111b921f6d72259313be2e5`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb18584dfdd2c5e1b16be910211bf58df75bebb8cc948d010bf7dacf1a81b`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 18.4 MB (18447692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af84d6773702a8389925020e1881a84b42b39eea9ebe082e379503372b4a2c6`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302c968087e93f72bd0a3e8da913da2a3b5cc3802ff0de5d389e6740323ef52`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 19.9 KB (19899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71edb0952ef713ac379d22d60a6a0e5e1ab8e1a7e0d6858994829d1584dfa20b`  
		Last Modified: Sat, 21 Dec 2024 00:54:42 GMT  
		Size: 30.2 MB (30150125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdfebf91571a2efa29d6268aafa0080828a4a9bc3ad5ecc7e2b43895774db5f`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d312a625a9cea21c47b3651da95e34689bc2b048df02e891d27f92700227cbe`  
		Last Modified: Sat, 21 Dec 2024 00:54:41 GMT  
		Size: 1.3 MB (1336889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3b201948d6a81833fdccada5d4e3cf47b4952cee8e2d3e6974c5d9d5d20f66`  
		Last Modified: Sat, 21 Dec 2024 00:54:41 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f64f2a4c489fad4e0d0a64578400ebae97f48ff6414114e2193580823d120a7`  
		Last Modified: Sat, 21 Dec 2024 00:54:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:9ebde0546735c9af7af3e0795d5e659520a8296d53a8d1479d1523df17e4b03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656fc55c2768c519f56d85ad96da27ad71cad8a63f85a5fb611216d0ab47f0a8`

```dockerfile
```

-	Layers:
	-	`sha256:9cace02e0df1fe416cecf8d9e4cacd7b0e661eae776b0196c327aa4a8d9d5813`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 2.2 MB (2160569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cae917344f15fe6c2d3b209cecda6985293409e586c9eb483162cf377c2c8acb`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 30.8 KB (30750 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:dc0c7f531b624ee2477bd1cf49355293d04ddffe21bf6114a95607694ea7feb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75214437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80cdc1c07fb8562711a1ce803be054ec8470d65a5ee7357812f41a7e272d546`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02eb691f526c59a4feade4837dd3c26533d9fe4c9306da60dc23a30620af346`  
		Last Modified: Wed, 11 Dec 2024 23:34:10 GMT  
		Size: 3.3 MB (3331581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f32f7c87db3a6447e39cf371cb0c2bb2c95f7a814793eff967d2a9a3b95122`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7c12be75768edb813fc94e2e1d2c48d7cb1f4cea2c832026ca6ae796dff9ac`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2737967709483bb9e56014fca897a13fd112c3084028d6543b06a30985537c4e`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 13.6 MB (13580520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b64ce4fbef8321cb5b9a415b540a4baa87078a9d7ee17306f53198aa5c3d6b`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a01d64640e85e99659018a2a9d802c50d724bde24674cd1ace68a407f974cc8`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 20.9 MB (20912964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61930bd78024ed559eceaae6edaa2d5a5396db98ea69ec50e91c0ce227b97848`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e991f93dcb7aadac92e8529d0719e89be0fbb0cc3478b38e16914291fef40b`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8074648689cf1786e687dd5d23af39dfbe621da1270c66591b9671c41a9a8d35`  
		Last Modified: Sat, 21 Dec 2024 01:55:18 GMT  
		Size: 32.0 MB (32002924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafd0942fb02c25d23f08063ad2cbeab093d6cf618b8d1e3da7813080cf0a5d3`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbc1bdc44e9a45913e2c17420d5f0c504ad83620bb6aa1a544f6a6608694652`  
		Last Modified: Sat, 21 Dec 2024 01:55:17 GMT  
		Size: 1.4 MB (1368492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25613c051b7489fcf2c3b4ae8295ffdcd74e959353d1a2f93d7c8e645d2fdf8e`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29a8df97712a4eb0f354b2d611f7a2dad77ca4e5c2e01bb399a9a9fd735bc62`  
		Last Modified: Sat, 21 Dec 2024 01:55:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:bea8151175d39d5d94a2809339eb42d48eaa49c4d008cc0741bbd2ba97097379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190e8eab0e89ebd0cacb63889de9557f839863ab662253d51e4900933ca35c1b`

```dockerfile
```

-	Layers:
	-	`sha256:77b9b330d91ca7cb9e2fb6eea92938e4d38194a237b8bf6ec9fc78cbe304cd90`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 2.2 MB (2160393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edec463ea7ad2f12e75b14fa0f1f42f016e6597e5a6659e5cabfdd835ee8829f`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 30.8 KB (30779 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; 386

```console
$ docker pull composer@sha256:45d1ecb99b2afaba6acc6b3650ec06cce0afe613523117a450d7ec301f328cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54591872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556f31a880ba642d0d47f607f2cf125f5a8cb888d8658e53912dd7cb425dd255`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c898e29d83e9db370e8891b59d2b75d52becd1c60e7168a6068c60ab70d34d74`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 3.4 MB (3376600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaee1fb0dd467b0c78610a290f1dab2d06cab056e446bcd035ed5a5be5bad5f`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6589c5988c6fb89267a968f26279f8f922579aeafe69c3b3d5c70ff348de1faf`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f212ddee911fee0e94e486cf1d8c16d2e4609a0aca213ae03ef06b0ec953924`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 13.6 MB (13580481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc377b1762be65b8185324b4a83578d3e2bdb568e2370167b8ad00c5b3f2c5e`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dc25b1fb1a50563b2ccab2e97a663fcdf74d01b6d4f08ecdf423a7ec4178c9`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 21.4 MB (21397982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e557dee7812f54a16556ac580967a78aca6fb0c9444067feedb7c2fec0f1cf`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cacd67f7a12349f00be424d47f5a310859feb05ec769add44557c85dc4c045e`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 20.1 KB (20067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23849d787e1a192bfd435c7fd7263c32435e87bd9d1fcbb9a4ae64a8f665d79f`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 11.4 MB (11421351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e11a704e653b95e9384311dd22ed4490a9a261e61d75660e76d9f67171b51f4`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af06b16830c267b956c54985affd5e7e43886fa2db245a39455ef078ad59e0`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 1.3 MB (1324445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f381b382e9ef1c58cffe5cbc61320a8e30721f2ede50059f17a2383f5befb7b`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d65102e5cbe1b6da82da528a5ad8d68921fd640fb933287d532f7ac4ef4878`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:ec9667f00c779b238bfaefd66a78952fcde3bd9e5a9d8b1f2a3434312fd45569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.5 KB (460537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2729d97b615f55eca06802c4c971107b63b89901a2175a96e049a48b01c94e56`

```dockerfile
```

-	Layers:
	-	`sha256:1788379821db1185f48672b130491ba6d2d4067eaa209d11071dd6e1591287ff`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 429.9 KB (429911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:793216d1cfe51d743a89fafc072b11087b8a3ea64df5a5c1d87b7c991424983b`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 30.6 KB (30626 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; ppc64le

```console
$ docker pull composer@sha256:39d47fddadebde46b5aa075b7b188488c77cd2fc5f78a482fbca5f8720e07784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9de5a09e6d5b3430ae020ddd9ad018e18cf2a612e13bf084f41785555ab912`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dab8c9093e7207bf34d7e27bcaf8a12d512bc9a6228a188ccd032ab556c048`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 3.5 MB (3474267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887eff0819f1e81cf0537030ec0eefbed710884b4bdcb74a53300dafe99af22`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d10c33dd4ddf3d7039e24ae3ea2657811b8add42853a37557baa89339c584`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73154329c1c9a418799584abd71b5689505fae8a1fe0c1edf20b4c054fdfa404`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe8613e572e5a00abda95594733a8b015a569e70fcfb60f921b46b1d3b0b4ce`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bfbf1907d341a6d1c62419f97827940bb943dfd0067d8cce4a44af3d1da5c0`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 22.3 MB (22287679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa21b603882a7aa1280eb0a92a0814e2acb781ef4ea1490d6871b2cf300d5ed`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b46dc3369c678c5f6e91da763573d92319716e4238a641860950d083934a3b`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320193b91948f33c75121c293867d724d3bd3982783314901a94db790aab8942`  
		Last Modified: Sat, 21 Dec 2024 00:47:37 GMT  
		Size: 32.9 MB (32943931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87a05827ee97083cff81d981bb3bc249115eff0447c4e4a7b65127727301f1c`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778809ac255a2d2ab7079bc8a84f7d2579eaa233a12aca89aa7bf87896b5853d`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 1.4 MB (1397690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d11e35988aedb4751dff69d03dda5e5372863af4a4f321bd35a2f249e2b9c3`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c494da996fb65daf0576665a803766cee732247601e416c96ecc6737c15d3242`  
		Last Modified: Sat, 21 Dec 2024 00:47:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:10851df2bb02f14a5d955ff5ee65aa6ccab36c724f71ce5e0f5bcffe198a592c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4228d46f61af59517ae32ece45efd921551f57cc01b81cea728b3989e3274692`

```dockerfile
```

-	Layers:
	-	`sha256:f6c18dc1eff360e59b3049c77febe8d09fadd373dc6c07021d937f971eda16ec`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 2.2 MB (2158810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c80bb77f9349195e9186f11e18f9830292abd319b18227f24b1f5a28246e4b3`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; riscv64

```console
$ docker pull composer@sha256:47b8462c8ed5b32076b9992c2fca053d9e419ffb51d4f123ffedef94cce62e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73015557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccd019c062510ff8af4860bd81975195ec2de6183e87262123beca4fbc95d80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
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
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65b4aeb40f99d5493f73d9206995a90aa94768378fa8ed5e3d1bfa1a5650e5`  
		Last Modified: Thu, 12 Dec 2024 05:33:08 GMT  
		Size: 13.6 MB (13573066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3a97d778691306fc952ddd90fe8250103f76d9aeb4d0203ae146e8e521bae`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087168628cd777dcb9b702d528d92efb821d834b9f0dcd8c3797efb04ae1c3b9`  
		Last Modified: Thu, 12 Dec 2024 05:33:09 GMT  
		Size: 20.3 MB (20313768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df21e8373b5877a4b523291936f8960c514ba6fad4100e893b67db195cf644`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1688f016a09ac412aed8ac075c283501f128abef9696857d645a64c550c669`  
		Last Modified: Thu, 12 Dec 2024 05:33:07 GMT  
		Size: 19.9 KB (19881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabab48893d974e79a79888fc6df380c6dcf350a41715045f49febecefddffeb`  
		Last Modified: Fri, 13 Dec 2024 00:49:21 GMT  
		Size: 31.0 MB (31000601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede30cfb10bc21715eab17b816b53c120038851e557f760c598e7ce4e84e9148`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc06b5c0e3074b70e86182bbadb2eede36867ac1f673a3327193ccdc65412142`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 1.3 MB (1303577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ef1a692089e1b772a12c12bade7cfdc0ca04dbb8115b0ccb080b1166f58f65`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1fd3d6f31b8ed05d003559b7a561f07659b81dc8e1d9ffa5157b6ad068b351`  
		Last Modified: Fri, 13 Dec 2024 00:49:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:be33fe14c76b8ffb0df7d3b9ba205626a3aef71c9f13827819a643c1412ea57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f861530adf2f03c926a23437974a7e17a7755fdf0924ec5195013be2de3ae`

```dockerfile
```

-	Layers:
	-	`sha256:d20c559f6d17c094e1f4f0d0a431f3d1d96c89f862133f0c09bd60516e621b46`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 2.2 MB (2160811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb521b49d1ee3611c2f351b8614014b608f44c92cecb932c920a0e5f4252693`  
		Last Modified: Fri, 13 Dec 2024 00:49:16 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; s390x

```console
$ docker pull composer@sha256:4f81a8cc27005ca20ff31502d4a6c730ebdde93ab3c818e9a949744a2a4fe471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75563374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47b7f75693b368d37da5356369d307a6330ec3a41005305220a6f93e3dc3662`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b02d148e9caeb82d2cf6c286e6c9c576dbce389f6c2cb18910b789ebd4813`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 3.6 MB (3561751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d561dc5f913bf5ac5c30d9c4d42bdf7aa341b8fba0e0ded0354c6e1aca173438`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465f443f2fadb2b0191af2eb2aae7a8ff4e66fef38973f7b9f36688fc1ff5cc`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167bd40a3a9b1f0b21e6140078bd769d2d967f4713b5f34ccb482a4b419592fe`  
		Last Modified: Fri, 20 Dec 2024 22:04:11 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd8774ef9fa0dca490b5d556eec80cd22fa38fbd2ad90d593168cffab7f95de`  
		Last Modified: Fri, 20 Dec 2024 22:04:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0154e3b89ce7965e82ffec7aff04edec326644e952fe96eca0cbe395ccb151b8`  
		Last Modified: Sat, 21 Dec 2024 01:07:03 GMT  
		Size: 21.9 MB (21867735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1a08d85e9f5ffb6b386d5b9a9c2260779e2408eb44cf874b23d61902f877a`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946fabb80ac5e81a3ba1e80ef02c503fa9257fd27f28ce77c24815e131b7f5bf`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cae5d9bba6d84260838c31aac6e5cc01aadf2ab697ab41df33ab9508312e2e1`  
		Last Modified: Sat, 21 Dec 2024 02:09:57 GMT  
		Size: 31.7 MB (31675723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1671f7a4b9055dd3f4c65b5f95cca757e39df07b78b85cd25865c7838f093`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a786d406f9afd0e23cf22f180471c74e952824c2f48ebe920d51a5cca6b585`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 1.4 MB (1383367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcda2dd35badb4fcf5b29d84d87d4e2362e1c15e399dbe95174dbbdbbf864d`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bca8707ab38c51cacfdd23547715666185b870f73ac54d0e7369b2a8e2d2e22`  
		Last Modified: Sat, 21 Dec 2024 02:09:57 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:62fc7c8a86c521fc58dd3016471f30e0cdfbfdf55a419f5d33db6e451125c056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff60a4eb8bc2e74bb2a8493fcc3a8be67f97dd609905fac616010f440b1085df`

```dockerfile
```

-	Layers:
	-	`sha256:f4129b7ac05a7aa09cfe96e67a0cb62362c63d083940dbeb50969cd5cf1dc13f`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 2.2 MB (2157538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c905aa4f81f1297ba94ce9655d9a7185d706c0fa849ea968d820b627d7e159`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8`

```console
$ docker pull composer@sha256:e49da3f473cf06fe694d7a578139f9ab3914f99fa406719109e7b171e059c08b
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
$ docker pull composer@sha256:e1b1c84478b74b1efb6c04d343cab7cdc69d8062b0538f6133ee96646e79104a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74853762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597f41083011e7bbca4e999c9fd285d81a3967eec31e4a4a1c482f0bcc8bcc68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926a903e79620f0a500e6c0b8920613cf3e77ee6fb031d64dfb3cb7d88442adc`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 3.3 MB (3336077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c946fba36f12b591be4b090159dd42766dc43c2a20caf28d504ef17c4491759`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac17bc9a4d3a9a1781e2999ce34426d9eec4eed120cb79c459b841169a923918`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8b186c29f3bb1fcde6dd416dd06bb7c990d07b2c9d4621ce4e8f93c94b835d`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 13.6 MB (13580495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e6cdee304691570c26af03b2fedb4dd8016faa742d307b7db946e6409f326`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27e6ddc32c5ab1579764b32caa4c52c636d33a510c4c3ef4495726c95381872`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.9 MB (20883408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7be51eeb9ec7eea5691039e5a979e9ae08b3c661c6e02bf44451ec261ec5b9`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c0be2943e6e61d571707b0255ead75b0198314874eefbdb3bfb8250db6c13e`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.1 KB (20064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566d18b93401424f6cbd928683adce9bf3ad82d0c304ecdb5761a031816caef6`  
		Last Modified: Fri, 20 Dec 2024 22:34:02 GMT  
		Size: 31.9 MB (31896290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592305bd0b09f3f4bf2abb5855fd7df7d7f38228b07839e62d8e4c99b7aa2453`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd129105385812e3d55bf1615ec40c334a459673a418d707df045a6139fdd96d`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 1.5 MB (1488122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91863bfb83d08b6151d9eaf8526a248b3af1ec3c748e87e93ae85a86dfdb53b`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517e54ceb37a099c3ab292f6a687964a4b0f7deb256c639398b85b33a51d55cb`  
		Last Modified: Fri, 20 Dec 2024 22:34:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:a923dedf7d089ffaddcad108756321cf5522ceece1700cf8fbd9625c918832c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c869ce6d6d541495dbae65bc4a0904de1854d78ca6f3d89cefd76eff7d59f212`

```dockerfile
```

-	Layers:
	-	`sha256:7b8df0015a446dc0086c8af311be236d57ebc2e27e15c8831e1a4e8b64591469`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 2.2 MB (2160547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db96c01aae65a4f474d876df088ecb013979b265d64fbb862820ca60a1d1507e`  
		Last Modified: Fri, 20 Dec 2024 22:34:00 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:5a901315d4c2bde5aa784104687bd50cfa9682b30b65a2ab66c2411f29470162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71975950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6f809430e63fc4ad150cc0cfa23da73d68f8d61240050a10a82e2d26d3a519`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b736a50b989ce147c8a50cd4eff3990052fbae41313316dd15bdd3ae41bb055`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 3.3 MB (3302897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520076a7063b8a800f7aeb276beb6363fa2c2192a17d803ee3f5fa20b0b0b211`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065854d8dae5a225e01a05809bd10528e215d02290cc6d9f51d4bc29dc1ac134`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7d8a646b13a1fce87a53e224ba759100c5661201fa77b07c2bb37e766e4399`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 13.6 MB (13580525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e81800135bc7fff5c18dd6a26d344cbcdc0f282ae7198e61803d1b9e97af13`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce8a346ef963d66430f1390abc1b68a4824385373ab05fa645c2aca57b6015`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.5 MB (19498804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eb2dc0afa0290d833b6477da2f88fe368ba4cefd3a8a5ef03f8561794efefa`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf11115b0d6d263d3685a04147a9d95c5179c52b651782cf9289977a6ac1ce`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a3ca09f084e2d996e8974d62fa6bd1b01b2867e5b1a057e00140bad318027d`  
		Last Modified: Fri, 20 Dec 2024 23:03:37 GMT  
		Size: 30.6 MB (30641288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c129606c926c4221d682770c2daaa54b304e77c6d10ac37d86224ded916fede3`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850dddccd57b27bdb3ca2dc30a6fb50f37cddf2591f3ba6c8f23d7de0e7a37c8`  
		Last Modified: Fri, 20 Dec 2024 23:04:54 GMT  
		Size: 1.6 MB (1560498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3826a6b574a6d595615f31b1ef9fae34a30dd1e418f79cee3bc7ab6a295e46ee`  
		Last Modified: Thu, 12 Dec 2024 19:28:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0626d3b0b278028796aa74a96ca4317a62592130844f13e3e2ac3acee08926aa`  
		Last Modified: Fri, 20 Dec 2024 23:04:53 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:6ad55a5cac64a1d8774c90709313e7e53126e21e45bbbcc671977e64bc8b1e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a3d9f20c6b83f35635d94080a217527ae9ed6e088b06ddc1f6fb6400865382`

```dockerfile
```

-	Layers:
	-	`sha256:a8b43523739b06da6ef40c60b9e3fa25c6202a24e2207b72b2a61b30b93ffa87`  
		Last Modified: Fri, 20 Dec 2024 23:04:53 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:db7e1d13f4f0f64df4e11318b1bfc27abf4689a3ffa2a4a6884941379e7e6cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69910112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d7406f32137829d576557610af675b4d6dc215cb6f02a9d945eeacc3781cd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58a80555964d79b4c54d0bc69d1ac3c99d92bfa41dc077ad9039581c976fe1`  
		Last Modified: Wed, 11 Dec 2024 23:35:20 GMT  
		Size: 3.1 MB (3128235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30daf13605f2d1179f6005fb32926b33b8626b9ceb92de019df902d09cedf935`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365fc515397f6962469f3d1c8654b5801822a766158bca2e8a9fa961d78db8`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7b2510a73dde296829d64a7a766b9532e9e98238663d7544fcb11d828edf19`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 13.6 MB (13580531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05cf7b909bafdb9e34f1486d56a868891fed509111b921f6d72259313be2e5`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb18584dfdd2c5e1b16be910211bf58df75bebb8cc948d010bf7dacf1a81b`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 18.4 MB (18447692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af84d6773702a8389925020e1881a84b42b39eea9ebe082e379503372b4a2c6`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302c968087e93f72bd0a3e8da913da2a3b5cc3802ff0de5d389e6740323ef52`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 19.9 KB (19899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71edb0952ef713ac379d22d60a6a0e5e1ab8e1a7e0d6858994829d1584dfa20b`  
		Last Modified: Sat, 21 Dec 2024 00:54:42 GMT  
		Size: 30.2 MB (30150125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdfebf91571a2efa29d6268aafa0080828a4a9bc3ad5ecc7e2b43895774db5f`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8aea252e0e53d95de52b8c5950ee056175c15143fbc121c31013209c5538a39`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 1.5 MB (1478722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3daab9b2754696fe222ee1f2893595fb1df9ac75c15609ad470c88caf501e8b`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6935c0a0e469ebc6c77c7f9a6b4f6e9e9e014039d2d057ae449266bf779ecfb0`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:a1616e46409e69c41cd4092ee361a3737ff11c8239f8c83144acaf68b187acb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074d3c493c898bdce2c01c34ec8fc7dbecdaf5b3e54323b863f669fc8667da5`

```dockerfile
```

-	Layers:
	-	`sha256:7e72894c6be4cfe667296ed4b53106cd8f218edbfa690f41518be4580405775d`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 2.2 MB (2160871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b62e2ff1b9aa44ff6550b505c92f55ce3b2f7cd0ea8c82649c5b1a4c9b41c9ca`  
		Last Modified: Sat, 21 Dec 2024 00:55:59 GMT  
		Size: 31.1 KB (31063 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:34f7cfafcc6768f84309dd8a37864fcf1a4e8939416c8931b3e4189294f3fc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75356775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636ee04b1d54bfa9b06d6c5b57f8de51413cf9c3b1672d6e6f9c431bed53fc23`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02eb691f526c59a4feade4837dd3c26533d9fe4c9306da60dc23a30620af346`  
		Last Modified: Wed, 11 Dec 2024 23:34:10 GMT  
		Size: 3.3 MB (3331581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f32f7c87db3a6447e39cf371cb0c2bb2c95f7a814793eff967d2a9a3b95122`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7c12be75768edb813fc94e2e1d2c48d7cb1f4cea2c832026ca6ae796dff9ac`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2737967709483bb9e56014fca897a13fd112c3084028d6543b06a30985537c4e`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 13.6 MB (13580520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b64ce4fbef8321cb5b9a415b540a4baa87078a9d7ee17306f53198aa5c3d6b`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a01d64640e85e99659018a2a9d802c50d724bde24674cd1ace68a407f974cc8`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 20.9 MB (20912964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61930bd78024ed559eceaae6edaa2d5a5396db98ea69ec50e91c0ce227b97848`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e991f93dcb7aadac92e8529d0719e89be0fbb0cc3478b38e16914291fef40b`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8074648689cf1786e687dd5d23af39dfbe621da1270c66591b9671c41a9a8d35`  
		Last Modified: Sat, 21 Dec 2024 01:55:18 GMT  
		Size: 32.0 MB (32002924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafd0942fb02c25d23f08063ad2cbeab093d6cf618b8d1e3da7813080cf0a5d3`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad88e37368d020d5a4f8a68e888a81393a07c69b0eefff65a090af38937a05c`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 1.5 MB (1510828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feacd1f5f2d7d620450018862bba088a1512fc3523832e860cb326e795f70605`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d2e662c0b87459a6d5034013826453a6b0afbd406209ce5fb7f5f9e0448460`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:b508f4c6c299c4a997fe4c9e1075a8cdc081617b6f5e94d79b9765f8e84c04e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a902e391fc2bce4bfb8212eafaefeb6a31b207b7e5e8dac5e021d386ddda2d`

```dockerfile
```

-	Layers:
	-	`sha256:bd6a6c91fca34ad1f1e3fd828fc199a78b4b81a76338f8ef7649a9efd37553a9`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 2.2 MB (2160699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23201e21b29c63fe764565ed4ae97d111c5cb614f494736f09cb5ec29c43411`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 31.1 KB (31094 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; 386

```console
$ docker pull composer@sha256:13cd3c9d62766d3600c5ece8fc68f3b6c14e455c76cc87f55a92f697117b09a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54734604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef626d096c7b0e5d6ac570116527e30afdb8a372aa6a94ae10d9de7f416d4e65`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c898e29d83e9db370e8891b59d2b75d52becd1c60e7168a6068c60ab70d34d74`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 3.4 MB (3376600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaee1fb0dd467b0c78610a290f1dab2d06cab056e446bcd035ed5a5be5bad5f`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6589c5988c6fb89267a968f26279f8f922579aeafe69c3b3d5c70ff348de1faf`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f212ddee911fee0e94e486cf1d8c16d2e4609a0aca213ae03ef06b0ec953924`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 13.6 MB (13580481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc377b1762be65b8185324b4a83578d3e2bdb568e2370167b8ad00c5b3f2c5e`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dc25b1fb1a50563b2ccab2e97a663fcdf74d01b6d4f08ecdf423a7ec4178c9`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 21.4 MB (21397982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e557dee7812f54a16556ac580967a78aca6fb0c9444067feedb7c2fec0f1cf`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cacd67f7a12349f00be424d47f5a310859feb05ec769add44557c85dc4c045e`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 20.1 KB (20067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06287a9316358b0f72490833a72d6f7e508faa1f3e9b3108819c7e0b7a8030fc`  
		Last Modified: Fri, 20 Dec 2024 22:30:54 GMT  
		Size: 11.4 MB (11421356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3918f2868475d53e64393972d158b9cfa5d0ea9c2911105e6421859b924c19b2`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc78b2a127bd3e7ce50cb76ad940f21a9f0e134013e0297da350caa3ca9c073`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 1.5 MB (1467169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37da3c63d602ee971c9fc9ef89a41b6088e4f7e7eb8022ec5f593eaa0c3fa0aa`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a7c693a6c06c4d9ff1694fb9dfdb0bfe337f4a907a823f36e2cb6f465f7d3f`  
		Last Modified: Fri, 20 Dec 2024 22:30:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:07dc5dfc59e7558508b3f87d5215565024156fdf59cdab60361fb9d20ce0f6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.1 KB (461125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9173980e4148edc00eeb621831580e60c15d42a197e8ead0f3ff4c2d10d36b9c`

```dockerfile
```

-	Layers:
	-	`sha256:76657d0771423cfa4cbd38f6dfc24b8c2abe412fac80284be5ff2addd76a1f32`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 430.2 KB (430200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3397f97a793dc2b9ce6e3abdd4c5468a0a2c70afea3a9ff791553b666147d29a`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 30.9 KB (30925 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; ppc64le

```console
$ docker pull composer@sha256:f4f0f620051d42be48776181af565e7851f099b355d518b887d23b60c412804f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77427854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1474f7a9f0d1a42435f12cc71acb12436d8180efa5fec58aa72da53f62466f6e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dab8c9093e7207bf34d7e27bcaf8a12d512bc9a6228a188ccd032ab556c048`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 3.5 MB (3474267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887eff0819f1e81cf0537030ec0eefbed710884b4bdcb74a53300dafe99af22`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d10c33dd4ddf3d7039e24ae3ea2657811b8add42853a37557baa89339c584`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73154329c1c9a418799584abd71b5689505fae8a1fe0c1edf20b4c054fdfa404`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe8613e572e5a00abda95594733a8b015a569e70fcfb60f921b46b1d3b0b4ce`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bfbf1907d341a6d1c62419f97827940bb943dfd0067d8cce4a44af3d1da5c0`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 22.3 MB (22287679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa21b603882a7aa1280eb0a92a0814e2acb781ef4ea1490d6871b2cf300d5ed`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b46dc3369c678c5f6e91da763573d92319716e4238a641860950d083934a3b`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320193b91948f33c75121c293867d724d3bd3982783314901a94db790aab8942`  
		Last Modified: Sat, 21 Dec 2024 00:47:37 GMT  
		Size: 32.9 MB (32943931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87a05827ee97083cff81d981bb3bc249115eff0447c4e4a7b65127727301f1c`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362869a3172835ee4528ea6f2f44bc837ebb8f00e7a773ec2152c108b44cce5`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 1.5 MB (1539584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0469f95a3ee042bb6c8182cadae42ac0814e69524ac25f1f82fb60231d4ff9e`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a0182bc07154bed20d5a39868bb2fef6baa5627b3394984ca31848525ece57`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:59e8871447f1590862034a4aa3d632539f3ccd49edf6adf206a46616eb75a37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ebf547901c22f465b12649dc1cc8394f42b6a0f3fa10edda44e64adb2596a7`

```dockerfile
```

-	Layers:
	-	`sha256:d5823359ef511b41f5b0642517539477214cc9457852442e553b1dc19c7baa36`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 2.2 MB (2159110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a64225a958451c59f6b285afb2cf8db0039c43becec7a9df44fcc5e9287fda31`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; riscv64

```console
$ docker pull composer@sha256:5ed834b87e8853267488e83580cf0efd0895c111918446017496ff1134309d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73159041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c5af21db82ae76f968ea7805d38106e25cfc280fa83e0a0552058c54de85cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
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
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65b4aeb40f99d5493f73d9206995a90aa94768378fa8ed5e3d1bfa1a5650e5`  
		Last Modified: Thu, 12 Dec 2024 05:33:08 GMT  
		Size: 13.6 MB (13573066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3a97d778691306fc952ddd90fe8250103f76d9aeb4d0203ae146e8e521bae`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087168628cd777dcb9b702d528d92efb821d834b9f0dcd8c3797efb04ae1c3b9`  
		Last Modified: Thu, 12 Dec 2024 05:33:09 GMT  
		Size: 20.3 MB (20313768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df21e8373b5877a4b523291936f8960c514ba6fad4100e893b67db195cf644`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1688f016a09ac412aed8ac075c283501f128abef9696857d645a64c550c669`  
		Last Modified: Thu, 12 Dec 2024 05:33:07 GMT  
		Size: 19.9 KB (19881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabab48893d974e79a79888fc6df380c6dcf350a41715045f49febecefddffeb`  
		Last Modified: Fri, 13 Dec 2024 00:49:21 GMT  
		Size: 31.0 MB (31000601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede30cfb10bc21715eab17b816b53c120038851e557f760c598e7ce4e84e9148`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946a7fcdbae57a989822e644601f1206974970f46880c2e4b93b740563d39880`  
		Last Modified: Fri, 13 Dec 2024 00:59:34 GMT  
		Size: 1.4 MB (1447059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e0b1c9377d6f40aa1bb8f77f7ad021c2cd3241936aa4c0070e1b1ddedca5db`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d621471430c14ecb515fd0a1755ef5f2b051d0729f8282b42214828554eccc30`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:1b77539025c2b4710b8f9c8abb0538f9fcd1d0f96079d528748cae96eefcfd2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2192120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4f29f2a4f548644ac52a500f1010b22e711fd4bc25d2179d348fe11c7b972e`

```dockerfile
```

-	Layers:
	-	`sha256:91caba4aa4b89b7471b15c276d6031e7253d025fb171f6a34066c214dd2068ae`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 2.2 MB (2161111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff1e0fa372986ca5902d81a83654c9d2e1e54a86b765e66b939114b561954fb`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; s390x

```console
$ docker pull composer@sha256:c08937ec02e7e3a8ba10b293a2d6bcafa3b7437f40a857fa7d1ab9ffeeb70680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75708713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185a38213023f1563ca995da494862924414e2c5244e2f344a8ec11bb37db3b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b02d148e9caeb82d2cf6c286e6c9c576dbce389f6c2cb18910b789ebd4813`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 3.6 MB (3561751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d561dc5f913bf5ac5c30d9c4d42bdf7aa341b8fba0e0ded0354c6e1aca173438`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465f443f2fadb2b0191af2eb2aae7a8ff4e66fef38973f7b9f36688fc1ff5cc`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167bd40a3a9b1f0b21e6140078bd769d2d967f4713b5f34ccb482a4b419592fe`  
		Last Modified: Fri, 20 Dec 2024 22:04:11 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd8774ef9fa0dca490b5d556eec80cd22fa38fbd2ad90d593168cffab7f95de`  
		Last Modified: Fri, 20 Dec 2024 22:04:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0154e3b89ce7965e82ffec7aff04edec326644e952fe96eca0cbe395ccb151b8`  
		Last Modified: Sat, 21 Dec 2024 01:07:03 GMT  
		Size: 21.9 MB (21867735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1a08d85e9f5ffb6b386d5b9a9c2260779e2408eb44cf874b23d61902f877a`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946fabb80ac5e81a3ba1e80ef02c503fa9257fd27f28ce77c24815e131b7f5bf`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cae5d9bba6d84260838c31aac6e5cc01aadf2ab697ab41df33ab9508312e2e1`  
		Last Modified: Sat, 21 Dec 2024 02:09:57 GMT  
		Size: 31.7 MB (31675723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1671f7a4b9055dd3f4c65b5f95cca757e39df07b78b85cd25865c7838f093`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6ea88506192fb2d0baa91e5c3ada4bd20b1007a7b0277404c092157519e1b4`  
		Last Modified: Sat, 21 Dec 2024 02:12:02 GMT  
		Size: 1.5 MB (1528705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c72de6015442cbef85c552a342409109175a5376f5e79acf9c56ee0dbbf495`  
		Last Modified: Sat, 21 Dec 2024 02:12:02 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dc08e4de24064ddc8c3fd37d73f66dce40dbe19b0ef56201d08671a7f2b901`  
		Last Modified: Sat, 21 Dec 2024 02:12:02 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:30a7adf0e400d70aa2347c9da2933cd55a90f800342b6f7109c86e4713c3e030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de56b26de8ffcb4f1353b74a2869b153a008d19e2db66e41cc749e7dba1f4481`

```dockerfile
```

-	Layers:
	-	`sha256:9b18a7df2365282d6bf26c5769e70e2c588af609e15f2fe2c9fa9b22b8759f73`  
		Last Modified: Sat, 21 Dec 2024 02:12:01 GMT  
		Size: 2.2 MB (2157832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881e3365eca7edb3a1b4748699a6523ca26215cf704dcd0d07de0b3edafc55b7`  
		Last Modified: Sat, 21 Dec 2024 02:12:01 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8.4`

```console
$ docker pull composer@sha256:e49da3f473cf06fe694d7a578139f9ab3914f99fa406719109e7b171e059c08b
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

### `composer:2.8.4` - linux; amd64

```console
$ docker pull composer@sha256:e1b1c84478b74b1efb6c04d343cab7cdc69d8062b0538f6133ee96646e79104a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74853762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597f41083011e7bbca4e999c9fd285d81a3967eec31e4a4a1c482f0bcc8bcc68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926a903e79620f0a500e6c0b8920613cf3e77ee6fb031d64dfb3cb7d88442adc`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 3.3 MB (3336077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c946fba36f12b591be4b090159dd42766dc43c2a20caf28d504ef17c4491759`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac17bc9a4d3a9a1781e2999ce34426d9eec4eed120cb79c459b841169a923918`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8b186c29f3bb1fcde6dd416dd06bb7c990d07b2c9d4621ce4e8f93c94b835d`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 13.6 MB (13580495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e6cdee304691570c26af03b2fedb4dd8016faa742d307b7db946e6409f326`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27e6ddc32c5ab1579764b32caa4c52c636d33a510c4c3ef4495726c95381872`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.9 MB (20883408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7be51eeb9ec7eea5691039e5a979e9ae08b3c661c6e02bf44451ec261ec5b9`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c0be2943e6e61d571707b0255ead75b0198314874eefbdb3bfb8250db6c13e`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.1 KB (20064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566d18b93401424f6cbd928683adce9bf3ad82d0c304ecdb5761a031816caef6`  
		Last Modified: Fri, 20 Dec 2024 22:34:02 GMT  
		Size: 31.9 MB (31896290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592305bd0b09f3f4bf2abb5855fd7df7d7f38228b07839e62d8e4c99b7aa2453`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd129105385812e3d55bf1615ec40c334a459673a418d707df045a6139fdd96d`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 1.5 MB (1488122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91863bfb83d08b6151d9eaf8526a248b3af1ec3c748e87e93ae85a86dfdb53b`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517e54ceb37a099c3ab292f6a687964a4b0f7deb256c639398b85b33a51d55cb`  
		Last Modified: Fri, 20 Dec 2024 22:34:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:a923dedf7d089ffaddcad108756321cf5522ceece1700cf8fbd9625c918832c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c869ce6d6d541495dbae65bc4a0904de1854d78ca6f3d89cefd76eff7d59f212`

```dockerfile
```

-	Layers:
	-	`sha256:7b8df0015a446dc0086c8af311be236d57ebc2e27e15c8831e1a4e8b64591469`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 2.2 MB (2160547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db96c01aae65a4f474d876df088ecb013979b265d64fbb862820ca60a1d1507e`  
		Last Modified: Fri, 20 Dec 2024 22:34:00 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.4` - linux; arm variant v6

```console
$ docker pull composer@sha256:5a901315d4c2bde5aa784104687bd50cfa9682b30b65a2ab66c2411f29470162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71975950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6f809430e63fc4ad150cc0cfa23da73d68f8d61240050a10a82e2d26d3a519`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b736a50b989ce147c8a50cd4eff3990052fbae41313316dd15bdd3ae41bb055`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 3.3 MB (3302897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520076a7063b8a800f7aeb276beb6363fa2c2192a17d803ee3f5fa20b0b0b211`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065854d8dae5a225e01a05809bd10528e215d02290cc6d9f51d4bc29dc1ac134`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7d8a646b13a1fce87a53e224ba759100c5661201fa77b07c2bb37e766e4399`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 13.6 MB (13580525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e81800135bc7fff5c18dd6a26d344cbcdc0f282ae7198e61803d1b9e97af13`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce8a346ef963d66430f1390abc1b68a4824385373ab05fa645c2aca57b6015`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.5 MB (19498804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eb2dc0afa0290d833b6477da2f88fe368ba4cefd3a8a5ef03f8561794efefa`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf11115b0d6d263d3685a04147a9d95c5179c52b651782cf9289977a6ac1ce`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a3ca09f084e2d996e8974d62fa6bd1b01b2867e5b1a057e00140bad318027d`  
		Last Modified: Fri, 20 Dec 2024 23:03:37 GMT  
		Size: 30.6 MB (30641288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c129606c926c4221d682770c2daaa54b304e77c6d10ac37d86224ded916fede3`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850dddccd57b27bdb3ca2dc30a6fb50f37cddf2591f3ba6c8f23d7de0e7a37c8`  
		Last Modified: Fri, 20 Dec 2024 23:04:54 GMT  
		Size: 1.6 MB (1560498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3826a6b574a6d595615f31b1ef9fae34a30dd1e418f79cee3bc7ab6a295e46ee`  
		Last Modified: Thu, 12 Dec 2024 19:28:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0626d3b0b278028796aa74a96ca4317a62592130844f13e3e2ac3acee08926aa`  
		Last Modified: Fri, 20 Dec 2024 23:04:53 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:6ad55a5cac64a1d8774c90709313e7e53126e21e45bbbcc671977e64bc8b1e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a3d9f20c6b83f35635d94080a217527ae9ed6e088b06ddc1f6fb6400865382`

```dockerfile
```

-	Layers:
	-	`sha256:a8b43523739b06da6ef40c60b9e3fa25c6202a24e2207b72b2a61b30b93ffa87`  
		Last Modified: Fri, 20 Dec 2024 23:04:53 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.4` - linux; arm variant v7

```console
$ docker pull composer@sha256:db7e1d13f4f0f64df4e11318b1bfc27abf4689a3ffa2a4a6884941379e7e6cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69910112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d7406f32137829d576557610af675b4d6dc215cb6f02a9d945eeacc3781cd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58a80555964d79b4c54d0bc69d1ac3c99d92bfa41dc077ad9039581c976fe1`  
		Last Modified: Wed, 11 Dec 2024 23:35:20 GMT  
		Size: 3.1 MB (3128235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30daf13605f2d1179f6005fb32926b33b8626b9ceb92de019df902d09cedf935`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365fc515397f6962469f3d1c8654b5801822a766158bca2e8a9fa961d78db8`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7b2510a73dde296829d64a7a766b9532e9e98238663d7544fcb11d828edf19`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 13.6 MB (13580531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05cf7b909bafdb9e34f1486d56a868891fed509111b921f6d72259313be2e5`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb18584dfdd2c5e1b16be910211bf58df75bebb8cc948d010bf7dacf1a81b`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 18.4 MB (18447692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af84d6773702a8389925020e1881a84b42b39eea9ebe082e379503372b4a2c6`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302c968087e93f72bd0a3e8da913da2a3b5cc3802ff0de5d389e6740323ef52`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 19.9 KB (19899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71edb0952ef713ac379d22d60a6a0e5e1ab8e1a7e0d6858994829d1584dfa20b`  
		Last Modified: Sat, 21 Dec 2024 00:54:42 GMT  
		Size: 30.2 MB (30150125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdfebf91571a2efa29d6268aafa0080828a4a9bc3ad5ecc7e2b43895774db5f`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8aea252e0e53d95de52b8c5950ee056175c15143fbc121c31013209c5538a39`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 1.5 MB (1478722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3daab9b2754696fe222ee1f2893595fb1df9ac75c15609ad470c88caf501e8b`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6935c0a0e469ebc6c77c7f9a6b4f6e9e9e014039d2d057ae449266bf779ecfb0`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:a1616e46409e69c41cd4092ee361a3737ff11c8239f8c83144acaf68b187acb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074d3c493c898bdce2c01c34ec8fc7dbecdaf5b3e54323b863f669fc8667da5`

```dockerfile
```

-	Layers:
	-	`sha256:7e72894c6be4cfe667296ed4b53106cd8f218edbfa690f41518be4580405775d`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 2.2 MB (2160871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b62e2ff1b9aa44ff6550b505c92f55ce3b2f7cd0ea8c82649c5b1a4c9b41c9ca`  
		Last Modified: Sat, 21 Dec 2024 00:55:59 GMT  
		Size: 31.1 KB (31063 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.4` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:34f7cfafcc6768f84309dd8a37864fcf1a4e8939416c8931b3e4189294f3fc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75356775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636ee04b1d54bfa9b06d6c5b57f8de51413cf9c3b1672d6e6f9c431bed53fc23`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02eb691f526c59a4feade4837dd3c26533d9fe4c9306da60dc23a30620af346`  
		Last Modified: Wed, 11 Dec 2024 23:34:10 GMT  
		Size: 3.3 MB (3331581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f32f7c87db3a6447e39cf371cb0c2bb2c95f7a814793eff967d2a9a3b95122`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7c12be75768edb813fc94e2e1d2c48d7cb1f4cea2c832026ca6ae796dff9ac`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2737967709483bb9e56014fca897a13fd112c3084028d6543b06a30985537c4e`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 13.6 MB (13580520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b64ce4fbef8321cb5b9a415b540a4baa87078a9d7ee17306f53198aa5c3d6b`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a01d64640e85e99659018a2a9d802c50d724bde24674cd1ace68a407f974cc8`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 20.9 MB (20912964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61930bd78024ed559eceaae6edaa2d5a5396db98ea69ec50e91c0ce227b97848`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e991f93dcb7aadac92e8529d0719e89be0fbb0cc3478b38e16914291fef40b`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8074648689cf1786e687dd5d23af39dfbe621da1270c66591b9671c41a9a8d35`  
		Last Modified: Sat, 21 Dec 2024 01:55:18 GMT  
		Size: 32.0 MB (32002924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafd0942fb02c25d23f08063ad2cbeab093d6cf618b8d1e3da7813080cf0a5d3`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad88e37368d020d5a4f8a68e888a81393a07c69b0eefff65a090af38937a05c`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 1.5 MB (1510828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feacd1f5f2d7d620450018862bba088a1512fc3523832e860cb326e795f70605`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d2e662c0b87459a6d5034013826453a6b0afbd406209ce5fb7f5f9e0448460`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:b508f4c6c299c4a997fe4c9e1075a8cdc081617b6f5e94d79b9765f8e84c04e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a902e391fc2bce4bfb8212eafaefeb6a31b207b7e5e8dac5e021d386ddda2d`

```dockerfile
```

-	Layers:
	-	`sha256:bd6a6c91fca34ad1f1e3fd828fc199a78b4b81a76338f8ef7649a9efd37553a9`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 2.2 MB (2160699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23201e21b29c63fe764565ed4ae97d111c5cb614f494736f09cb5ec29c43411`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 31.1 KB (31094 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.4` - linux; 386

```console
$ docker pull composer@sha256:13cd3c9d62766d3600c5ece8fc68f3b6c14e455c76cc87f55a92f697117b09a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54734604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef626d096c7b0e5d6ac570116527e30afdb8a372aa6a94ae10d9de7f416d4e65`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c898e29d83e9db370e8891b59d2b75d52becd1c60e7168a6068c60ab70d34d74`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 3.4 MB (3376600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaee1fb0dd467b0c78610a290f1dab2d06cab056e446bcd035ed5a5be5bad5f`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6589c5988c6fb89267a968f26279f8f922579aeafe69c3b3d5c70ff348de1faf`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f212ddee911fee0e94e486cf1d8c16d2e4609a0aca213ae03ef06b0ec953924`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 13.6 MB (13580481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc377b1762be65b8185324b4a83578d3e2bdb568e2370167b8ad00c5b3f2c5e`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dc25b1fb1a50563b2ccab2e97a663fcdf74d01b6d4f08ecdf423a7ec4178c9`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 21.4 MB (21397982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e557dee7812f54a16556ac580967a78aca6fb0c9444067feedb7c2fec0f1cf`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cacd67f7a12349f00be424d47f5a310859feb05ec769add44557c85dc4c045e`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 20.1 KB (20067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06287a9316358b0f72490833a72d6f7e508faa1f3e9b3108819c7e0b7a8030fc`  
		Last Modified: Fri, 20 Dec 2024 22:30:54 GMT  
		Size: 11.4 MB (11421356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3918f2868475d53e64393972d158b9cfa5d0ea9c2911105e6421859b924c19b2`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc78b2a127bd3e7ce50cb76ad940f21a9f0e134013e0297da350caa3ca9c073`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 1.5 MB (1467169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37da3c63d602ee971c9fc9ef89a41b6088e4f7e7eb8022ec5f593eaa0c3fa0aa`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a7c693a6c06c4d9ff1694fb9dfdb0bfe337f4a907a823f36e2cb6f465f7d3f`  
		Last Modified: Fri, 20 Dec 2024 22:30:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:07dc5dfc59e7558508b3f87d5215565024156fdf59cdab60361fb9d20ce0f6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.1 KB (461125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9173980e4148edc00eeb621831580e60c15d42a197e8ead0f3ff4c2d10d36b9c`

```dockerfile
```

-	Layers:
	-	`sha256:76657d0771423cfa4cbd38f6dfc24b8c2abe412fac80284be5ff2addd76a1f32`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 430.2 KB (430200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3397f97a793dc2b9ce6e3abdd4c5468a0a2c70afea3a9ff791553b666147d29a`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 30.9 KB (30925 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.4` - linux; ppc64le

```console
$ docker pull composer@sha256:f4f0f620051d42be48776181af565e7851f099b355d518b887d23b60c412804f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77427854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1474f7a9f0d1a42435f12cc71acb12436d8180efa5fec58aa72da53f62466f6e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dab8c9093e7207bf34d7e27bcaf8a12d512bc9a6228a188ccd032ab556c048`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 3.5 MB (3474267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887eff0819f1e81cf0537030ec0eefbed710884b4bdcb74a53300dafe99af22`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d10c33dd4ddf3d7039e24ae3ea2657811b8add42853a37557baa89339c584`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73154329c1c9a418799584abd71b5689505fae8a1fe0c1edf20b4c054fdfa404`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe8613e572e5a00abda95594733a8b015a569e70fcfb60f921b46b1d3b0b4ce`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bfbf1907d341a6d1c62419f97827940bb943dfd0067d8cce4a44af3d1da5c0`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 22.3 MB (22287679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa21b603882a7aa1280eb0a92a0814e2acb781ef4ea1490d6871b2cf300d5ed`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b46dc3369c678c5f6e91da763573d92319716e4238a641860950d083934a3b`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320193b91948f33c75121c293867d724d3bd3982783314901a94db790aab8942`  
		Last Modified: Sat, 21 Dec 2024 00:47:37 GMT  
		Size: 32.9 MB (32943931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87a05827ee97083cff81d981bb3bc249115eff0447c4e4a7b65127727301f1c`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362869a3172835ee4528ea6f2f44bc837ebb8f00e7a773ec2152c108b44cce5`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 1.5 MB (1539584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0469f95a3ee042bb6c8182cadae42ac0814e69524ac25f1f82fb60231d4ff9e`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a0182bc07154bed20d5a39868bb2fef6baa5627b3394984ca31848525ece57`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:59e8871447f1590862034a4aa3d632539f3ccd49edf6adf206a46616eb75a37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ebf547901c22f465b12649dc1cc8394f42b6a0f3fa10edda44e64adb2596a7`

```dockerfile
```

-	Layers:
	-	`sha256:d5823359ef511b41f5b0642517539477214cc9457852442e553b1dc19c7baa36`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 2.2 MB (2159110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a64225a958451c59f6b285afb2cf8db0039c43becec7a9df44fcc5e9287fda31`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.4` - linux; riscv64

```console
$ docker pull composer@sha256:5ed834b87e8853267488e83580cf0efd0895c111918446017496ff1134309d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73159041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c5af21db82ae76f968ea7805d38106e25cfc280fa83e0a0552058c54de85cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
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
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65b4aeb40f99d5493f73d9206995a90aa94768378fa8ed5e3d1bfa1a5650e5`  
		Last Modified: Thu, 12 Dec 2024 05:33:08 GMT  
		Size: 13.6 MB (13573066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3a97d778691306fc952ddd90fe8250103f76d9aeb4d0203ae146e8e521bae`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087168628cd777dcb9b702d528d92efb821d834b9f0dcd8c3797efb04ae1c3b9`  
		Last Modified: Thu, 12 Dec 2024 05:33:09 GMT  
		Size: 20.3 MB (20313768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df21e8373b5877a4b523291936f8960c514ba6fad4100e893b67db195cf644`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1688f016a09ac412aed8ac075c283501f128abef9696857d645a64c550c669`  
		Last Modified: Thu, 12 Dec 2024 05:33:07 GMT  
		Size: 19.9 KB (19881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabab48893d974e79a79888fc6df380c6dcf350a41715045f49febecefddffeb`  
		Last Modified: Fri, 13 Dec 2024 00:49:21 GMT  
		Size: 31.0 MB (31000601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede30cfb10bc21715eab17b816b53c120038851e557f760c598e7ce4e84e9148`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946a7fcdbae57a989822e644601f1206974970f46880c2e4b93b740563d39880`  
		Last Modified: Fri, 13 Dec 2024 00:59:34 GMT  
		Size: 1.4 MB (1447059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e0b1c9377d6f40aa1bb8f77f7ad021c2cd3241936aa4c0070e1b1ddedca5db`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d621471430c14ecb515fd0a1755ef5f2b051d0729f8282b42214828554eccc30`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:1b77539025c2b4710b8f9c8abb0538f9fcd1d0f96079d528748cae96eefcfd2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2192120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4f29f2a4f548644ac52a500f1010b22e711fd4bc25d2179d348fe11c7b972e`

```dockerfile
```

-	Layers:
	-	`sha256:91caba4aa4b89b7471b15c276d6031e7253d025fb171f6a34066c214dd2068ae`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 2.2 MB (2161111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff1e0fa372986ca5902d81a83654c9d2e1e54a86b765e66b939114b561954fb`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.4` - linux; s390x

```console
$ docker pull composer@sha256:c08937ec02e7e3a8ba10b293a2d6bcafa3b7437f40a857fa7d1ab9ffeeb70680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75708713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185a38213023f1563ca995da494862924414e2c5244e2f344a8ec11bb37db3b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b02d148e9caeb82d2cf6c286e6c9c576dbce389f6c2cb18910b789ebd4813`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 3.6 MB (3561751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d561dc5f913bf5ac5c30d9c4d42bdf7aa341b8fba0e0ded0354c6e1aca173438`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465f443f2fadb2b0191af2eb2aae7a8ff4e66fef38973f7b9f36688fc1ff5cc`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167bd40a3a9b1f0b21e6140078bd769d2d967f4713b5f34ccb482a4b419592fe`  
		Last Modified: Fri, 20 Dec 2024 22:04:11 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd8774ef9fa0dca490b5d556eec80cd22fa38fbd2ad90d593168cffab7f95de`  
		Last Modified: Fri, 20 Dec 2024 22:04:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0154e3b89ce7965e82ffec7aff04edec326644e952fe96eca0cbe395ccb151b8`  
		Last Modified: Sat, 21 Dec 2024 01:07:03 GMT  
		Size: 21.9 MB (21867735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1a08d85e9f5ffb6b386d5b9a9c2260779e2408eb44cf874b23d61902f877a`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946fabb80ac5e81a3ba1e80ef02c503fa9257fd27f28ce77c24815e131b7f5bf`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cae5d9bba6d84260838c31aac6e5cc01aadf2ab697ab41df33ab9508312e2e1`  
		Last Modified: Sat, 21 Dec 2024 02:09:57 GMT  
		Size: 31.7 MB (31675723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1671f7a4b9055dd3f4c65b5f95cca757e39df07b78b85cd25865c7838f093`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6ea88506192fb2d0baa91e5c3ada4bd20b1007a7b0277404c092157519e1b4`  
		Last Modified: Sat, 21 Dec 2024 02:12:02 GMT  
		Size: 1.5 MB (1528705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c72de6015442cbef85c552a342409109175a5376f5e79acf9c56ee0dbbf495`  
		Last Modified: Sat, 21 Dec 2024 02:12:02 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dc08e4de24064ddc8c3fd37d73f66dce40dbe19b0ef56201d08671a7f2b901`  
		Last Modified: Sat, 21 Dec 2024 02:12:02 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:30a7adf0e400d70aa2347c9da2933cd55a90f800342b6f7109c86e4713c3e030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de56b26de8ffcb4f1353b74a2869b153a008d19e2db66e41cc749e7dba1f4481`

```dockerfile
```

-	Layers:
	-	`sha256:9b18a7df2365282d6bf26c5769e70e2c588af609e15f2fe2c9fa9b22b8759f73`  
		Last Modified: Sat, 21 Dec 2024 02:12:01 GMT  
		Size: 2.2 MB (2157832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881e3365eca7edb3a1b4748699a6523ca26215cf704dcd0d07de0b3edafc55b7`  
		Last Modified: Sat, 21 Dec 2024 02:12:01 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:e49da3f473cf06fe694d7a578139f9ab3914f99fa406719109e7b171e059c08b
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
$ docker pull composer@sha256:e1b1c84478b74b1efb6c04d343cab7cdc69d8062b0538f6133ee96646e79104a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74853762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597f41083011e7bbca4e999c9fd285d81a3967eec31e4a4a1c482f0bcc8bcc68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926a903e79620f0a500e6c0b8920613cf3e77ee6fb031d64dfb3cb7d88442adc`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 3.3 MB (3336077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c946fba36f12b591be4b090159dd42766dc43c2a20caf28d504ef17c4491759`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac17bc9a4d3a9a1781e2999ce34426d9eec4eed120cb79c459b841169a923918`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8b186c29f3bb1fcde6dd416dd06bb7c990d07b2c9d4621ce4e8f93c94b835d`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 13.6 MB (13580495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e6cdee304691570c26af03b2fedb4dd8016faa742d307b7db946e6409f326`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27e6ddc32c5ab1579764b32caa4c52c636d33a510c4c3ef4495726c95381872`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.9 MB (20883408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7be51eeb9ec7eea5691039e5a979e9ae08b3c661c6e02bf44451ec261ec5b9`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c0be2943e6e61d571707b0255ead75b0198314874eefbdb3bfb8250db6c13e`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.1 KB (20064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566d18b93401424f6cbd928683adce9bf3ad82d0c304ecdb5761a031816caef6`  
		Last Modified: Fri, 20 Dec 2024 22:34:02 GMT  
		Size: 31.9 MB (31896290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592305bd0b09f3f4bf2abb5855fd7df7d7f38228b07839e62d8e4c99b7aa2453`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd129105385812e3d55bf1615ec40c334a459673a418d707df045a6139fdd96d`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 1.5 MB (1488122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91863bfb83d08b6151d9eaf8526a248b3af1ec3c748e87e93ae85a86dfdb53b`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517e54ceb37a099c3ab292f6a687964a4b0f7deb256c639398b85b33a51d55cb`  
		Last Modified: Fri, 20 Dec 2024 22:34:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:a923dedf7d089ffaddcad108756321cf5522ceece1700cf8fbd9625c918832c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c869ce6d6d541495dbae65bc4a0904de1854d78ca6f3d89cefd76eff7d59f212`

```dockerfile
```

-	Layers:
	-	`sha256:7b8df0015a446dc0086c8af311be236d57ebc2e27e15c8831e1a4e8b64591469`  
		Last Modified: Fri, 20 Dec 2024 22:34:01 GMT  
		Size: 2.2 MB (2160547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db96c01aae65a4f474d876df088ecb013979b265d64fbb862820ca60a1d1507e`  
		Last Modified: Fri, 20 Dec 2024 22:34:00 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:5a901315d4c2bde5aa784104687bd50cfa9682b30b65a2ab66c2411f29470162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71975950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6f809430e63fc4ad150cc0cfa23da73d68f8d61240050a10a82e2d26d3a519`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b736a50b989ce147c8a50cd4eff3990052fbae41313316dd15bdd3ae41bb055`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 3.3 MB (3302897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520076a7063b8a800f7aeb276beb6363fa2c2192a17d803ee3f5fa20b0b0b211`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065854d8dae5a225e01a05809bd10528e215d02290cc6d9f51d4bc29dc1ac134`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7d8a646b13a1fce87a53e224ba759100c5661201fa77b07c2bb37e766e4399`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 13.6 MB (13580525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e81800135bc7fff5c18dd6a26d344cbcdc0f282ae7198e61803d1b9e97af13`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce8a346ef963d66430f1390abc1b68a4824385373ab05fa645c2aca57b6015`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.5 MB (19498804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eb2dc0afa0290d833b6477da2f88fe368ba4cefd3a8a5ef03f8561794efefa`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf11115b0d6d263d3685a04147a9d95c5179c52b651782cf9289977a6ac1ce`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a3ca09f084e2d996e8974d62fa6bd1b01b2867e5b1a057e00140bad318027d`  
		Last Modified: Fri, 20 Dec 2024 23:03:37 GMT  
		Size: 30.6 MB (30641288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c129606c926c4221d682770c2daaa54b304e77c6d10ac37d86224ded916fede3`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850dddccd57b27bdb3ca2dc30a6fb50f37cddf2591f3ba6c8f23d7de0e7a37c8`  
		Last Modified: Fri, 20 Dec 2024 23:04:54 GMT  
		Size: 1.6 MB (1560498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3826a6b574a6d595615f31b1ef9fae34a30dd1e418f79cee3bc7ab6a295e46ee`  
		Last Modified: Thu, 12 Dec 2024 19:28:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0626d3b0b278028796aa74a96ca4317a62592130844f13e3e2ac3acee08926aa`  
		Last Modified: Fri, 20 Dec 2024 23:04:53 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:6ad55a5cac64a1d8774c90709313e7e53126e21e45bbbcc671977e64bc8b1e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a3d9f20c6b83f35635d94080a217527ae9ed6e088b06ddc1f6fb6400865382`

```dockerfile
```

-	Layers:
	-	`sha256:a8b43523739b06da6ef40c60b9e3fa25c6202a24e2207b72b2a61b30b93ffa87`  
		Last Modified: Fri, 20 Dec 2024 23:04:53 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:db7e1d13f4f0f64df4e11318b1bfc27abf4689a3ffa2a4a6884941379e7e6cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69910112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d7406f32137829d576557610af675b4d6dc215cb6f02a9d945eeacc3781cd5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58a80555964d79b4c54d0bc69d1ac3c99d92bfa41dc077ad9039581c976fe1`  
		Last Modified: Wed, 11 Dec 2024 23:35:20 GMT  
		Size: 3.1 MB (3128235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30daf13605f2d1179f6005fb32926b33b8626b9ceb92de019df902d09cedf935`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365fc515397f6962469f3d1c8654b5801822a766158bca2e8a9fa961d78db8`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7b2510a73dde296829d64a7a766b9532e9e98238663d7544fcb11d828edf19`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 13.6 MB (13580531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05cf7b909bafdb9e34f1486d56a868891fed509111b921f6d72259313be2e5`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb18584dfdd2c5e1b16be910211bf58df75bebb8cc948d010bf7dacf1a81b`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 18.4 MB (18447692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af84d6773702a8389925020e1881a84b42b39eea9ebe082e379503372b4a2c6`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302c968087e93f72bd0a3e8da913da2a3b5cc3802ff0de5d389e6740323ef52`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 19.9 KB (19899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71edb0952ef713ac379d22d60a6a0e5e1ab8e1a7e0d6858994829d1584dfa20b`  
		Last Modified: Sat, 21 Dec 2024 00:54:42 GMT  
		Size: 30.2 MB (30150125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdfebf91571a2efa29d6268aafa0080828a4a9bc3ad5ecc7e2b43895774db5f`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8aea252e0e53d95de52b8c5950ee056175c15143fbc121c31013209c5538a39`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 1.5 MB (1478722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3daab9b2754696fe222ee1f2893595fb1df9ac75c15609ad470c88caf501e8b`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6935c0a0e469ebc6c77c7f9a6b4f6e9e9e014039d2d057ae449266bf779ecfb0`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:a1616e46409e69c41cd4092ee361a3737ff11c8239f8c83144acaf68b187acb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074d3c493c898bdce2c01c34ec8fc7dbecdaf5b3e54323b863f669fc8667da5`

```dockerfile
```

-	Layers:
	-	`sha256:7e72894c6be4cfe667296ed4b53106cd8f218edbfa690f41518be4580405775d`  
		Last Modified: Sat, 21 Dec 2024 00:56:00 GMT  
		Size: 2.2 MB (2160871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b62e2ff1b9aa44ff6550b505c92f55ce3b2f7cd0ea8c82649c5b1a4c9b41c9ca`  
		Last Modified: Sat, 21 Dec 2024 00:55:59 GMT  
		Size: 31.1 KB (31063 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:34f7cfafcc6768f84309dd8a37864fcf1a4e8939416c8931b3e4189294f3fc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75356775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636ee04b1d54bfa9b06d6c5b57f8de51413cf9c3b1672d6e6f9c431bed53fc23`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02eb691f526c59a4feade4837dd3c26533d9fe4c9306da60dc23a30620af346`  
		Last Modified: Wed, 11 Dec 2024 23:34:10 GMT  
		Size: 3.3 MB (3331581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f32f7c87db3a6447e39cf371cb0c2bb2c95f7a814793eff967d2a9a3b95122`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7c12be75768edb813fc94e2e1d2c48d7cb1f4cea2c832026ca6ae796dff9ac`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2737967709483bb9e56014fca897a13fd112c3084028d6543b06a30985537c4e`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 13.6 MB (13580520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b64ce4fbef8321cb5b9a415b540a4baa87078a9d7ee17306f53198aa5c3d6b`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a01d64640e85e99659018a2a9d802c50d724bde24674cd1ace68a407f974cc8`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 20.9 MB (20912964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61930bd78024ed559eceaae6edaa2d5a5396db98ea69ec50e91c0ce227b97848`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e991f93dcb7aadac92e8529d0719e89be0fbb0cc3478b38e16914291fef40b`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8074648689cf1786e687dd5d23af39dfbe621da1270c66591b9671c41a9a8d35`  
		Last Modified: Sat, 21 Dec 2024 01:55:18 GMT  
		Size: 32.0 MB (32002924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafd0942fb02c25d23f08063ad2cbeab093d6cf618b8d1e3da7813080cf0a5d3`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad88e37368d020d5a4f8a68e888a81393a07c69b0eefff65a090af38937a05c`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 1.5 MB (1510828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feacd1f5f2d7d620450018862bba088a1512fc3523832e860cb326e795f70605`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d2e662c0b87459a6d5034013826453a6b0afbd406209ce5fb7f5f9e0448460`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:b508f4c6c299c4a997fe4c9e1075a8cdc081617b6f5e94d79b9765f8e84c04e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a902e391fc2bce4bfb8212eafaefeb6a31b207b7e5e8dac5e021d386ddda2d`

```dockerfile
```

-	Layers:
	-	`sha256:bd6a6c91fca34ad1f1e3fd828fc199a78b4b81a76338f8ef7649a9efd37553a9`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 2.2 MB (2160699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23201e21b29c63fe764565ed4ae97d111c5cb614f494736f09cb5ec29c43411`  
		Last Modified: Sat, 21 Dec 2024 04:29:08 GMT  
		Size: 31.1 KB (31094 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:13cd3c9d62766d3600c5ece8fc68f3b6c14e455c76cc87f55a92f697117b09a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54734604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef626d096c7b0e5d6ac570116527e30afdb8a372aa6a94ae10d9de7f416d4e65`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c898e29d83e9db370e8891b59d2b75d52becd1c60e7168a6068c60ab70d34d74`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 3.4 MB (3376600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaee1fb0dd467b0c78610a290f1dab2d06cab056e446bcd035ed5a5be5bad5f`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6589c5988c6fb89267a968f26279f8f922579aeafe69c3b3d5c70ff348de1faf`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f212ddee911fee0e94e486cf1d8c16d2e4609a0aca213ae03ef06b0ec953924`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 13.6 MB (13580481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc377b1762be65b8185324b4a83578d3e2bdb568e2370167b8ad00c5b3f2c5e`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dc25b1fb1a50563b2ccab2e97a663fcdf74d01b6d4f08ecdf423a7ec4178c9`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 21.4 MB (21397982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e557dee7812f54a16556ac580967a78aca6fb0c9444067feedb7c2fec0f1cf`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cacd67f7a12349f00be424d47f5a310859feb05ec769add44557c85dc4c045e`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 20.1 KB (20067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06287a9316358b0f72490833a72d6f7e508faa1f3e9b3108819c7e0b7a8030fc`  
		Last Modified: Fri, 20 Dec 2024 22:30:54 GMT  
		Size: 11.4 MB (11421356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3918f2868475d53e64393972d158b9cfa5d0ea9c2911105e6421859b924c19b2`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc78b2a127bd3e7ce50cb76ad940f21a9f0e134013e0297da350caa3ca9c073`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 1.5 MB (1467169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37da3c63d602ee971c9fc9ef89a41b6088e4f7e7eb8022ec5f593eaa0c3fa0aa`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a7c693a6c06c4d9ff1694fb9dfdb0bfe337f4a907a823f36e2cb6f465f7d3f`  
		Last Modified: Fri, 20 Dec 2024 22:30:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:07dc5dfc59e7558508b3f87d5215565024156fdf59cdab60361fb9d20ce0f6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.1 KB (461125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9173980e4148edc00eeb621831580e60c15d42a197e8ead0f3ff4c2d10d36b9c`

```dockerfile
```

-	Layers:
	-	`sha256:76657d0771423cfa4cbd38f6dfc24b8c2abe412fac80284be5ff2addd76a1f32`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 430.2 KB (430200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3397f97a793dc2b9ce6e3abdd4c5468a0a2c70afea3a9ff791553b666147d29a`  
		Last Modified: Fri, 20 Dec 2024 22:30:53 GMT  
		Size: 30.9 KB (30925 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:f4f0f620051d42be48776181af565e7851f099b355d518b887d23b60c412804f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77427854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1474f7a9f0d1a42435f12cc71acb12436d8180efa5fec58aa72da53f62466f6e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dab8c9093e7207bf34d7e27bcaf8a12d512bc9a6228a188ccd032ab556c048`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 3.5 MB (3474267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887eff0819f1e81cf0537030ec0eefbed710884b4bdcb74a53300dafe99af22`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d10c33dd4ddf3d7039e24ae3ea2657811b8add42853a37557baa89339c584`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73154329c1c9a418799584abd71b5689505fae8a1fe0c1edf20b4c054fdfa404`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe8613e572e5a00abda95594733a8b015a569e70fcfb60f921b46b1d3b0b4ce`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bfbf1907d341a6d1c62419f97827940bb943dfd0067d8cce4a44af3d1da5c0`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 22.3 MB (22287679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa21b603882a7aa1280eb0a92a0814e2acb781ef4ea1490d6871b2cf300d5ed`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b46dc3369c678c5f6e91da763573d92319716e4238a641860950d083934a3b`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320193b91948f33c75121c293867d724d3bd3982783314901a94db790aab8942`  
		Last Modified: Sat, 21 Dec 2024 00:47:37 GMT  
		Size: 32.9 MB (32943931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87a05827ee97083cff81d981bb3bc249115eff0447c4e4a7b65127727301f1c`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362869a3172835ee4528ea6f2f44bc837ebb8f00e7a773ec2152c108b44cce5`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 1.5 MB (1539584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0469f95a3ee042bb6c8182cadae42ac0814e69524ac25f1f82fb60231d4ff9e`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a0182bc07154bed20d5a39868bb2fef6baa5627b3394984ca31848525ece57`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:59e8871447f1590862034a4aa3d632539f3ccd49edf6adf206a46616eb75a37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ebf547901c22f465b12649dc1cc8394f42b6a0f3fa10edda44e64adb2596a7`

```dockerfile
```

-	Layers:
	-	`sha256:d5823359ef511b41f5b0642517539477214cc9457852442e553b1dc19c7baa36`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 2.2 MB (2159110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a64225a958451c59f6b285afb2cf8db0039c43becec7a9df44fcc5e9287fda31`  
		Last Modified: Sat, 21 Dec 2024 00:49:58 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:5ed834b87e8853267488e83580cf0efd0895c111918446017496ff1134309d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73159041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c5af21db82ae76f968ea7805d38106e25cfc280fa83e0a0552058c54de85cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
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
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65b4aeb40f99d5493f73d9206995a90aa94768378fa8ed5e3d1bfa1a5650e5`  
		Last Modified: Thu, 12 Dec 2024 05:33:08 GMT  
		Size: 13.6 MB (13573066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3a97d778691306fc952ddd90fe8250103f76d9aeb4d0203ae146e8e521bae`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087168628cd777dcb9b702d528d92efb821d834b9f0dcd8c3797efb04ae1c3b9`  
		Last Modified: Thu, 12 Dec 2024 05:33:09 GMT  
		Size: 20.3 MB (20313768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df21e8373b5877a4b523291936f8960c514ba6fad4100e893b67db195cf644`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1688f016a09ac412aed8ac075c283501f128abef9696857d645a64c550c669`  
		Last Modified: Thu, 12 Dec 2024 05:33:07 GMT  
		Size: 19.9 KB (19881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabab48893d974e79a79888fc6df380c6dcf350a41715045f49febecefddffeb`  
		Last Modified: Fri, 13 Dec 2024 00:49:21 GMT  
		Size: 31.0 MB (31000601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede30cfb10bc21715eab17b816b53c120038851e557f760c598e7ce4e84e9148`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946a7fcdbae57a989822e644601f1206974970f46880c2e4b93b740563d39880`  
		Last Modified: Fri, 13 Dec 2024 00:59:34 GMT  
		Size: 1.4 MB (1447059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e0b1c9377d6f40aa1bb8f77f7ad021c2cd3241936aa4c0070e1b1ddedca5db`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d621471430c14ecb515fd0a1755ef5f2b051d0729f8282b42214828554eccc30`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:1b77539025c2b4710b8f9c8abb0538f9fcd1d0f96079d528748cae96eefcfd2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2192120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4f29f2a4f548644ac52a500f1010b22e711fd4bc25d2179d348fe11c7b972e`

```dockerfile
```

-	Layers:
	-	`sha256:91caba4aa4b89b7471b15c276d6031e7253d025fb171f6a34066c214dd2068ae`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 2.2 MB (2161111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff1e0fa372986ca5902d81a83654c9d2e1e54a86b765e66b939114b561954fb`  
		Last Modified: Fri, 13 Dec 2024 00:59:33 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:c08937ec02e7e3a8ba10b293a2d6bcafa3b7437f40a857fa7d1ab9ffeeb70680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75708713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185a38213023f1563ca995da494862924414e2c5244e2f344a8ec11bb37db3b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b02d148e9caeb82d2cf6c286e6c9c576dbce389f6c2cb18910b789ebd4813`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 3.6 MB (3561751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d561dc5f913bf5ac5c30d9c4d42bdf7aa341b8fba0e0ded0354c6e1aca173438`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465f443f2fadb2b0191af2eb2aae7a8ff4e66fef38973f7b9f36688fc1ff5cc`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167bd40a3a9b1f0b21e6140078bd769d2d967f4713b5f34ccb482a4b419592fe`  
		Last Modified: Fri, 20 Dec 2024 22:04:11 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd8774ef9fa0dca490b5d556eec80cd22fa38fbd2ad90d593168cffab7f95de`  
		Last Modified: Fri, 20 Dec 2024 22:04:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0154e3b89ce7965e82ffec7aff04edec326644e952fe96eca0cbe395ccb151b8`  
		Last Modified: Sat, 21 Dec 2024 01:07:03 GMT  
		Size: 21.9 MB (21867735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1a08d85e9f5ffb6b386d5b9a9c2260779e2408eb44cf874b23d61902f877a`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946fabb80ac5e81a3ba1e80ef02c503fa9257fd27f28ce77c24815e131b7f5bf`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cae5d9bba6d84260838c31aac6e5cc01aadf2ab697ab41df33ab9508312e2e1`  
		Last Modified: Sat, 21 Dec 2024 02:09:57 GMT  
		Size: 31.7 MB (31675723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1671f7a4b9055dd3f4c65b5f95cca757e39df07b78b85cd25865c7838f093`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6ea88506192fb2d0baa91e5c3ada4bd20b1007a7b0277404c092157519e1b4`  
		Last Modified: Sat, 21 Dec 2024 02:12:02 GMT  
		Size: 1.5 MB (1528705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c72de6015442cbef85c552a342409109175a5376f5e79acf9c56ee0dbbf495`  
		Last Modified: Sat, 21 Dec 2024 02:12:02 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dc08e4de24064ddc8c3fd37d73f66dce40dbe19b0ef56201d08671a7f2b901`  
		Last Modified: Sat, 21 Dec 2024 02:12:02 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:30a7adf0e400d70aa2347c9da2933cd55a90f800342b6f7109c86e4713c3e030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de56b26de8ffcb4f1353b74a2869b153a008d19e2db66e41cc749e7dba1f4481`

```dockerfile
```

-	Layers:
	-	`sha256:9b18a7df2365282d6bf26c5769e70e2c588af609e15f2fe2c9fa9b22b8759f73`  
		Last Modified: Sat, 21 Dec 2024 02:12:01 GMT  
		Size: 2.2 MB (2157832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881e3365eca7edb3a1b4748699a6523ca26215cf704dcd0d07de0b3edafc55b7`  
		Last Modified: Sat, 21 Dec 2024 02:12:01 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:lts`

```console
$ docker pull composer@sha256:83e7a817513a79b47ff105232417e3bd427cc91b4e04c0120af8d350c1f05b0a
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
$ docker pull composer@sha256:86715a9902c34da8b1a386da4f3620dc408719bc13c8e564a9ec59c980321809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74711677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc6137bd729ce1e7c590a7cbbc3971e242c2678b80e1019b1eaaa5990bed954`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926a903e79620f0a500e6c0b8920613cf3e77ee6fb031d64dfb3cb7d88442adc`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 3.3 MB (3336077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c946fba36f12b591be4b090159dd42766dc43c2a20caf28d504ef17c4491759`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac17bc9a4d3a9a1781e2999ce34426d9eec4eed120cb79c459b841169a923918`  
		Last Modified: Fri, 20 Dec 2024 21:35:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8b186c29f3bb1fcde6dd416dd06bb7c990d07b2c9d4621ce4e8f93c94b835d`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 13.6 MB (13580495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e6cdee304691570c26af03b2fedb4dd8016faa742d307b7db946e6409f326`  
		Last Modified: Fri, 20 Dec 2024 21:35:34 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27e6ddc32c5ab1579764b32caa4c52c636d33a510c4c3ef4495726c95381872`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.9 MB (20883408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7be51eeb9ec7eea5691039e5a979e9ae08b3c661c6e02bf44451ec261ec5b9`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c0be2943e6e61d571707b0255ead75b0198314874eefbdb3bfb8250db6c13e`  
		Last Modified: Fri, 20 Dec 2024 21:35:35 GMT  
		Size: 20.1 KB (20064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297872bde09879fe8c40c33d24670744d6c17bec4a5ae5813e82e2e3e2226aa2`  
		Last Modified: Fri, 20 Dec 2024 22:33:43 GMT  
		Size: 31.9 MB (31896376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee2060556a2755bde3d1f9ef97928ca996a9803c47290d46626dbc8042d4c5f`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59909d02d551d27004dde96ad05907559b515402eaba5169a7123eacd852e30`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 1.3 MB (1345949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd6ca8b30cf3126e4e29b5036aa4540dadf93174a92aa26d50410b9b96dcbec`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8add366ccdb2fbd941033272751360debaf11d77812bd4e989b280f393ebe28`  
		Last Modified: Fri, 20 Dec 2024 22:33:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:05f8169281cd999bf35f6b343742200edf11de7d21febfe544190d88cd1c3c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b763c0169a3680d8c766871afc239d987faaadd62dc4c92e9dbe40f084289a2`

```dockerfile
```

-	Layers:
	-	`sha256:9159222466972256ebd9c846b95b63fcd4d6f60da3ad15da44e730cd3b8ce237`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 2.2 MB (2160253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827c4480a261b491158b29b2448e6c3cd5d73f3b2a1fdf3ba93d2acc080bd0c1`  
		Last Modified: Fri, 20 Dec 2024 22:33:42 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v6

```console
$ docker pull composer@sha256:d339b6e27d102bc6a8a2c2d03140e17e4024ca9cdd9e155480a076da471e6235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71831909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b219a5abd047a63931a60c6374218612786c3cbf62cbc326a5e10e26d71d4e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b736a50b989ce147c8a50cd4eff3990052fbae41313316dd15bdd3ae41bb055`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 3.3 MB (3302897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520076a7063b8a800f7aeb276beb6363fa2c2192a17d803ee3f5fa20b0b0b211`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065854d8dae5a225e01a05809bd10528e215d02290cc6d9f51d4bc29dc1ac134`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7d8a646b13a1fce87a53e224ba759100c5661201fa77b07c2bb37e766e4399`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 13.6 MB (13580525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e81800135bc7fff5c18dd6a26d344cbcdc0f282ae7198e61803d1b9e97af13`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce8a346ef963d66430f1390abc1b68a4824385373ab05fa645c2aca57b6015`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.5 MB (19498804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eb2dc0afa0290d833b6477da2f88fe368ba4cefd3a8a5ef03f8561794efefa`  
		Last Modified: Fri, 20 Dec 2024 21:35:42 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf11115b0d6d263d3685a04147a9d95c5179c52b651782cf9289977a6ac1ce`  
		Last Modified: Fri, 20 Dec 2024 21:35:43 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a3ca09f084e2d996e8974d62fa6bd1b01b2867e5b1a057e00140bad318027d`  
		Last Modified: Fri, 20 Dec 2024 23:03:37 GMT  
		Size: 30.6 MB (30641288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c129606c926c4221d682770c2daaa54b304e77c6d10ac37d86224ded916fede3`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca357cec05180899d9e8d28334a0e6bc9298b37bca1b6c8c1c400e1a8ff18b0`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 1.4 MB (1416457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d76b9a3e1f7c21e5a182c9d58502bc43af53578e67a16921add85659a9209`  
		Last Modified: Thu, 12 Dec 2024 19:27:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9b049e98e5aa565b7511812e1351103b5e9f811e326eac0f30a2e3743b9c24`  
		Last Modified: Fri, 20 Dec 2024 23:03:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:52cdc68e02a3ba68b8d2d2d8bec512376210abf3254d05aecb56736a8655063d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721d4101af98ce5b00dd62400ad02e9747f8cd2169aba4c3a50cb244f40eff06`

```dockerfile
```

-	Layers:
	-	`sha256:882e75b853bd9635aa0062827bef1e69172eb52c056816b244d9b01cfb964aaf`  
		Last Modified: Fri, 20 Dec 2024 23:03:35 GMT  
		Size: 30.5 KB (30536 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v7

```console
$ docker pull composer@sha256:44b63081db2d7161b0cdf1e553f37c64da6184c348efca14459551e73764049e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69768280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be287281ea2df9d53c487316b05754e7b654a2c80a9a449852731263a34fbc7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58a80555964d79b4c54d0bc69d1ac3c99d92bfa41dc077ad9039581c976fe1`  
		Last Modified: Wed, 11 Dec 2024 23:35:20 GMT  
		Size: 3.1 MB (3128235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30daf13605f2d1179f6005fb32926b33b8626b9ceb92de019df902d09cedf935`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365fc515397f6962469f3d1c8654b5801822a766158bca2e8a9fa961d78db8`  
		Last Modified: Wed, 11 Dec 2024 23:35:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7b2510a73dde296829d64a7a766b9532e9e98238663d7544fcb11d828edf19`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 13.6 MB (13580531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05cf7b909bafdb9e34f1486d56a868891fed509111b921f6d72259313be2e5`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcb18584dfdd2c5e1b16be910211bf58df75bebb8cc948d010bf7dacf1a81b`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 18.4 MB (18447692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af84d6773702a8389925020e1881a84b42b39eea9ebe082e379503372b4a2c6`  
		Last Modified: Fri, 20 Dec 2024 22:12:44 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302c968087e93f72bd0a3e8da913da2a3b5cc3802ff0de5d389e6740323ef52`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 19.9 KB (19899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71edb0952ef713ac379d22d60a6a0e5e1ab8e1a7e0d6858994829d1584dfa20b`  
		Last Modified: Sat, 21 Dec 2024 00:54:42 GMT  
		Size: 30.2 MB (30150125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdfebf91571a2efa29d6268aafa0080828a4a9bc3ad5ecc7e2b43895774db5f`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d312a625a9cea21c47b3651da95e34689bc2b048df02e891d27f92700227cbe`  
		Last Modified: Sat, 21 Dec 2024 00:54:41 GMT  
		Size: 1.3 MB (1336889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3b201948d6a81833fdccada5d4e3cf47b4952cee8e2d3e6974c5d9d5d20f66`  
		Last Modified: Sat, 21 Dec 2024 00:54:41 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f64f2a4c489fad4e0d0a64578400ebae97f48ff6414114e2193580823d120a7`  
		Last Modified: Sat, 21 Dec 2024 00:54:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:9ebde0546735c9af7af3e0795d5e659520a8296d53a8d1479d1523df17e4b03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656fc55c2768c519f56d85ad96da27ad71cad8a63f85a5fb611216d0ab47f0a8`

```dockerfile
```

-	Layers:
	-	`sha256:9cace02e0df1fe416cecf8d9e4cacd7b0e661eae776b0196c327aa4a8d9d5813`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 2.2 MB (2160569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cae917344f15fe6c2d3b209cecda6985293409e586c9eb483162cf377c2c8acb`  
		Last Modified: Sat, 21 Dec 2024 00:54:40 GMT  
		Size: 30.8 KB (30750 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:dc0c7f531b624ee2477bd1cf49355293d04ddffe21bf6114a95607694ea7feb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75214437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80cdc1c07fb8562711a1ce803be054ec8470d65a5ee7357812f41a7e272d546`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02eb691f526c59a4feade4837dd3c26533d9fe4c9306da60dc23a30620af346`  
		Last Modified: Wed, 11 Dec 2024 23:34:10 GMT  
		Size: 3.3 MB (3331581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f32f7c87db3a6447e39cf371cb0c2bb2c95f7a814793eff967d2a9a3b95122`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7c12be75768edb813fc94e2e1d2c48d7cb1f4cea2c832026ca6ae796dff9ac`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2737967709483bb9e56014fca897a13fd112c3084028d6543b06a30985537c4e`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 13.6 MB (13580520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b64ce4fbef8321cb5b9a415b540a4baa87078a9d7ee17306f53198aa5c3d6b`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a01d64640e85e99659018a2a9d802c50d724bde24674cd1ace68a407f974cc8`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 20.9 MB (20912964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61930bd78024ed559eceaae6edaa2d5a5396db98ea69ec50e91c0ce227b97848`  
		Last Modified: Fri, 20 Dec 2024 22:01:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e991f93dcb7aadac92e8529d0719e89be0fbb0cc3478b38e16914291fef40b`  
		Last Modified: Fri, 20 Dec 2024 22:01:15 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8074648689cf1786e687dd5d23af39dfbe621da1270c66591b9671c41a9a8d35`  
		Last Modified: Sat, 21 Dec 2024 01:55:18 GMT  
		Size: 32.0 MB (32002924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafd0942fb02c25d23f08063ad2cbeab093d6cf618b8d1e3da7813080cf0a5d3`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbc1bdc44e9a45913e2c17420d5f0c504ad83620bb6aa1a544f6a6608694652`  
		Last Modified: Sat, 21 Dec 2024 01:55:17 GMT  
		Size: 1.4 MB (1368492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25613c051b7489fcf2c3b4ae8295ffdcd74e959353d1a2f93d7c8e645d2fdf8e`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29a8df97712a4eb0f354b2d611f7a2dad77ca4e5c2e01bb399a9a9fd735bc62`  
		Last Modified: Sat, 21 Dec 2024 01:55:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:bea8151175d39d5d94a2809339eb42d48eaa49c4d008cc0741bbd2ba97097379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190e8eab0e89ebd0cacb63889de9557f839863ab662253d51e4900933ca35c1b`

```dockerfile
```

-	Layers:
	-	`sha256:77b9b330d91ca7cb9e2fb6eea92938e4d38194a237b8bf6ec9fc78cbe304cd90`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 2.2 MB (2160393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edec463ea7ad2f12e75b14fa0f1f42f016e6597e5a6659e5cabfdd835ee8829f`  
		Last Modified: Sat, 21 Dec 2024 01:55:16 GMT  
		Size: 30.8 KB (30779 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; 386

```console
$ docker pull composer@sha256:45d1ecb99b2afaba6acc6b3650ec06cce0afe613523117a450d7ec301f328cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54591872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556f31a880ba642d0d47f607f2cf125f5a8cb888d8658e53912dd7cb425dd255`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c898e29d83e9db370e8891b59d2b75d52becd1c60e7168a6068c60ab70d34d74`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 3.4 MB (3376600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaee1fb0dd467b0c78610a290f1dab2d06cab056e446bcd035ed5a5be5bad5f`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6589c5988c6fb89267a968f26279f8f922579aeafe69c3b3d5c70ff348de1faf`  
		Last Modified: Fri, 20 Dec 2024 21:35:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f212ddee911fee0e94e486cf1d8c16d2e4609a0aca213ae03ef06b0ec953924`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 13.6 MB (13580481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc377b1762be65b8185324b4a83578d3e2bdb568e2370167b8ad00c5b3f2c5e`  
		Last Modified: Fri, 20 Dec 2024 21:35:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dc25b1fb1a50563b2ccab2e97a663fcdf74d01b6d4f08ecdf423a7ec4178c9`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 21.4 MB (21397982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e557dee7812f54a16556ac580967a78aca6fb0c9444067feedb7c2fec0f1cf`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cacd67f7a12349f00be424d47f5a310859feb05ec769add44557c85dc4c045e`  
		Last Modified: Fri, 20 Dec 2024 21:35:46 GMT  
		Size: 20.1 KB (20067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23849d787e1a192bfd435c7fd7263c32435e87bd9d1fcbb9a4ae64a8f665d79f`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 11.4 MB (11421351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e11a704e653b95e9384311dd22ed4490a9a261e61d75660e76d9f67171b51f4`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af06b16830c267b956c54985affd5e7e43886fa2db245a39455ef078ad59e0`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 1.3 MB (1324445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f381b382e9ef1c58cffe5cbc61320a8e30721f2ede50059f17a2383f5befb7b`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d65102e5cbe1b6da82da528a5ad8d68921fd640fb933287d532f7ac4ef4878`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:ec9667f00c779b238bfaefd66a78952fcde3bd9e5a9d8b1f2a3434312fd45569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.5 KB (460537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2729d97b615f55eca06802c4c971107b63b89901a2175a96e049a48b01c94e56`

```dockerfile
```

-	Layers:
	-	`sha256:1788379821db1185f48672b130491ba6d2d4067eaa209d11071dd6e1591287ff`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 429.9 KB (429911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:793216d1cfe51d743a89fafc072b11087b8a3ea64df5a5c1d87b7c991424983b`  
		Last Modified: Fri, 20 Dec 2024 22:30:33 GMT  
		Size: 30.6 KB (30626 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; ppc64le

```console
$ docker pull composer@sha256:39d47fddadebde46b5aa075b7b188488c77cd2fc5f78a482fbca5f8720e07784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9de5a09e6d5b3430ae020ddd9ad018e18cf2a612e13bf084f41785555ab912`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dab8c9093e7207bf34d7e27bcaf8a12d512bc9a6228a188ccd032ab556c048`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 3.5 MB (3474267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887eff0819f1e81cf0537030ec0eefbed710884b4bdcb74a53300dafe99af22`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d10c33dd4ddf3d7039e24ae3ea2657811b8add42853a37557baa89339c584`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73154329c1c9a418799584abd71b5689505fae8a1fe0c1edf20b4c054fdfa404`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe8613e572e5a00abda95594733a8b015a569e70fcfb60f921b46b1d3b0b4ce`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bfbf1907d341a6d1c62419f97827940bb943dfd0067d8cce4a44af3d1da5c0`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 22.3 MB (22287679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa21b603882a7aa1280eb0a92a0814e2acb781ef4ea1490d6871b2cf300d5ed`  
		Last Modified: Fri, 20 Dec 2024 21:50:45 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b46dc3369c678c5f6e91da763573d92319716e4238a641860950d083934a3b`  
		Last Modified: Fri, 20 Dec 2024 21:50:46 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320193b91948f33c75121c293867d724d3bd3982783314901a94db790aab8942`  
		Last Modified: Sat, 21 Dec 2024 00:47:37 GMT  
		Size: 32.9 MB (32943931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87a05827ee97083cff81d981bb3bc249115eff0447c4e4a7b65127727301f1c`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778809ac255a2d2ab7079bc8a84f7d2579eaa233a12aca89aa7bf87896b5853d`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 1.4 MB (1397690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d11e35988aedb4751dff69d03dda5e5372863af4a4f321bd35a2f249e2b9c3`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c494da996fb65daf0576665a803766cee732247601e416c96ecc6737c15d3242`  
		Last Modified: Sat, 21 Dec 2024 00:47:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:10851df2bb02f14a5d955ff5ee65aa6ccab36c724f71ce5e0f5bcffe198a592c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4228d46f61af59517ae32ece45efd921551f57cc01b81cea728b3989e3274692`

```dockerfile
```

-	Layers:
	-	`sha256:f6c18dc1eff360e59b3049c77febe8d09fadd373dc6c07021d937f971eda16ec`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 2.2 MB (2158810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c80bb77f9349195e9186f11e18f9830292abd319b18227f24b1f5a28246e4b3`  
		Last Modified: Sat, 21 Dec 2024 00:47:36 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; riscv64

```console
$ docker pull composer@sha256:47b8462c8ed5b32076b9992c2fca053d9e419ffb51d4f123ffedef94cce62e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73015557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccd019c062510ff8af4860bd81975195ec2de6183e87262123beca4fbc95d80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Dec 2024 09:57:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Dec 2024 09:57:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_VERSION=8.4.1
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.1.tar.xz.asc
# Sat, 07 Dec 2024 09:57:27 GMT
ENV PHP_SHA256=94c8a4fd419d45748951fa6d73bd55f6bdf0adaefb8814880a67baa66027311f
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 07 Dec 2024 09:57:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 07 Dec 2024 09:57:27 GMT
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
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65b4aeb40f99d5493f73d9206995a90aa94768378fa8ed5e3d1bfa1a5650e5`  
		Last Modified: Thu, 12 Dec 2024 05:33:08 GMT  
		Size: 13.6 MB (13573066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3a97d778691306fc952ddd90fe8250103f76d9aeb4d0203ae146e8e521bae`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087168628cd777dcb9b702d528d92efb821d834b9f0dcd8c3797efb04ae1c3b9`  
		Last Modified: Thu, 12 Dec 2024 05:33:09 GMT  
		Size: 20.3 MB (20313768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df21e8373b5877a4b523291936f8960c514ba6fad4100e893b67db195cf644`  
		Last Modified: Thu, 12 Dec 2024 05:33:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1688f016a09ac412aed8ac075c283501f128abef9696857d645a64c550c669`  
		Last Modified: Thu, 12 Dec 2024 05:33:07 GMT  
		Size: 19.9 KB (19881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabab48893d974e79a79888fc6df380c6dcf350a41715045f49febecefddffeb`  
		Last Modified: Fri, 13 Dec 2024 00:49:21 GMT  
		Size: 31.0 MB (31000601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede30cfb10bc21715eab17b816b53c120038851e557f760c598e7ce4e84e9148`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc06b5c0e3074b70e86182bbadb2eede36867ac1f673a3327193ccdc65412142`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 1.3 MB (1303577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ef1a692089e1b772a12c12bade7cfdc0ca04dbb8115b0ccb080b1166f58f65`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1fd3d6f31b8ed05d003559b7a561f07659b81dc8e1d9ffa5157b6ad068b351`  
		Last Modified: Fri, 13 Dec 2024 00:49:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:be33fe14c76b8ffb0df7d3b9ba205626a3aef71c9f13827819a643c1412ea57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f861530adf2f03c926a23437974a7e17a7755fdf0924ec5195013be2de3ae`

```dockerfile
```

-	Layers:
	-	`sha256:d20c559f6d17c094e1f4f0d0a431f3d1d96c89f862133f0c09bd60516e621b46`  
		Last Modified: Fri, 13 Dec 2024 00:49:17 GMT  
		Size: 2.2 MB (2160811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb521b49d1ee3611c2f351b8614014b608f44c92cecb932c920a0e5f4252693`  
		Last Modified: Fri, 13 Dec 2024 00:49:16 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; s390x

```console
$ docker pull composer@sha256:4f81a8cc27005ca20ff31502d4a6c730ebdde93ab3c818e9a949744a2a4fe471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75563374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47b7f75693b368d37da5356369d307a6330ec3a41005305220a6f93e3dc3662`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
ENV PHP_VERSION=8.4.2
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b02d148e9caeb82d2cf6c286e6c9c576dbce389f6c2cb18910b789ebd4813`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 3.6 MB (3561751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d561dc5f913bf5ac5c30d9c4d42bdf7aa341b8fba0e0ded0354c6e1aca173438`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465f443f2fadb2b0191af2eb2aae7a8ff4e66fef38973f7b9f36688fc1ff5cc`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167bd40a3a9b1f0b21e6140078bd769d2d967f4713b5f34ccb482a4b419592fe`  
		Last Modified: Fri, 20 Dec 2024 22:04:11 GMT  
		Size: 13.6 MB (13580519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd8774ef9fa0dca490b5d556eec80cd22fa38fbd2ad90d593168cffab7f95de`  
		Last Modified: Fri, 20 Dec 2024 22:04:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0154e3b89ce7965e82ffec7aff04edec326644e952fe96eca0cbe395ccb151b8`  
		Last Modified: Sat, 21 Dec 2024 01:07:03 GMT  
		Size: 21.9 MB (21867735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1a08d85e9f5ffb6b386d5b9a9c2260779e2408eb44cf874b23d61902f877a`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946fabb80ac5e81a3ba1e80ef02c503fa9257fd27f28ce77c24815e131b7f5bf`  
		Last Modified: Sat, 21 Dec 2024 01:06:59 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cae5d9bba6d84260838c31aac6e5cc01aadf2ab697ab41df33ab9508312e2e1`  
		Last Modified: Sat, 21 Dec 2024 02:09:57 GMT  
		Size: 31.7 MB (31675723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1671f7a4b9055dd3f4c65b5f95cca757e39df07b78b85cd25865c7838f093`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a786d406f9afd0e23cf22f180471c74e952824c2f48ebe920d51a5cca6b585`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 1.4 MB (1383367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcda2dd35badb4fcf5b29d84d87d4e2362e1c15e399dbe95174dbbdbbf864d`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bca8707ab38c51cacfdd23547715666185b870f73ac54d0e7369b2a8e2d2e22`  
		Last Modified: Sat, 21 Dec 2024 02:09:57 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:62fc7c8a86c521fc58dd3016471f30e0cdfbfdf55a419f5d33db6e451125c056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff60a4eb8bc2e74bb2a8493fcc3a8be67f97dd609905fac616010f440b1085df`

```dockerfile
```

-	Layers:
	-	`sha256:f4129b7ac05a7aa09cfe96e67a0cb62362c63d083940dbeb50969cd5cf1dc13f`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 2.2 MB (2157538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c905aa4f81f1297ba94ce9655d9a7185d706c0fa849ea968d820b627d7e159`  
		Last Modified: Sat, 21 Dec 2024 02:09:56 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json
