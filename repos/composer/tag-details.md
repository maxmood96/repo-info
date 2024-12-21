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
$ docker pull composer@sha256:05405855883dd01626b72eb307c78d95bba8cd7a5fa2828780200bd3a35af19c
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
$ docker pull composer@sha256:1e2d7273ccd17acb7c3492abb432220db1d3013bcf55c550555c71cfc37bc9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74091940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee07706e551cc6a6b3ad6ef4cfa1fa5af87339a7006a37ce31d66a4c52f6eb5`
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
	-	`sha256:bbcf41220f696f1ec3f3f3b53534f127b841636f0ca74e73210df73c7afefd94`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 13.6 MB (13573084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809689fb0b0450d700790c2f857ee46f0365fcb59cd3a227a736a8490de3c543`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ce08adea5bc33bdbdd66d6a505b2121998cfa91dd21b795b357eddd2e39b35`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 20.4 MB (20431405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ae36b542eb59f1f97688d2b4eff8d5e2772fe2c54c924a04d4b5c624307eea`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27d88523f19c0d0489fc13f34a3ce1166db9f0768337a9f3eccddfe7b511fbf`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 19.9 KB (19891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfa30f31250098695573d0af31f5d6241bcc6e651d4869a41bbb7dd377e83ba`  
		Last Modified: Thu, 12 Dec 2024 01:32:35 GMT  
		Size: 32.0 MB (32002990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad774222e92c8e35a5b78acc18db3f756bd2ab88623b5b116d1141660bc7e57`  
		Last Modified: Thu, 12 Dec 2024 01:32:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ac0e4ac113caea7eadd428f87ec7fdee449d348377f6f51919ef57267eb20`  
		Last Modified: Thu, 12 Dec 2024 01:33:11 GMT  
		Size: 734.9 KB (734945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337d5a2b89002f8d71e07df8e468d35f43bbb9adf04785a4384c20d479317d3d`  
		Last Modified: Thu, 12 Dec 2024 01:33:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ededd848983dff2aecf20fa9653ee5d7a7fc0f97e7b62129af777a5e8044d5ca`  
		Last Modified: Thu, 12 Dec 2024 01:33:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:0fa90e3cf424f9ac31146b878e2222466d9fb1f6b1bded5c697a684d8d0a9d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2193051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ba1993b74968107b5331cf5f2ecf6584cc97b8cb60d4a2cc436c912447b1ed`

```dockerfile
```

-	Layers:
	-	`sha256:18fbbfa34563d8030c88b1aa90af403d2778f2a37d5b8987ec0f8902ca8c54c2`  
		Last Modified: Thu, 12 Dec 2024 01:33:11 GMT  
		Size: 2.2 MB (2162265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6690f6046aaae684cb7236cdf58caae0bfcb2fcbce81177a978fb427851601`  
		Last Modified: Thu, 12 Dec 2024 01:33:10 GMT  
		Size: 30.8 KB (30786 bytes)  
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
$ docker pull composer@sha256:8cb3575258a34ce35f457eb65215c60278ea1aebd0bbbf9a37e2d14bfe1a8d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74404914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b478c43d543db5a53fe39603e1c4496194d9cba0cfd2f6b9ab6020fc9405a5bb`
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
	-	`sha256:7fedb1f25ba3b80074435858fc7794f83dc60e8736ca21254eab5159475f8ce4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 13.6 MB (13573088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c1315e733813b79535cafe40777595657596cda0a210db51f85480bfef1d4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee25f5bf4dbcae92e377529e99cb4c6fa1cddf3d1f43f8a63f4c01fffbc168f`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 21.4 MB (21362101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefb014c07c692f915ec490b55896346a687632ed71b8639d478c6573b16d88`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c7a618991f31a5ebdf26fbe9b53afeeaf94c829681cf294eb65ff6100da285`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 19.9 KB (19883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70251eda3f8e3a22e23ade26da5ea0d2b6dd1124907cb91a168a968d99172a4`  
		Last Modified: Thu, 12 Dec 2024 01:07:56 GMT  
		Size: 31.7 MB (31675572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071b32b1e7922ec5606ce28fd8866edd970297da1052a382440e3f930929be0`  
		Last Modified: Thu, 12 Dec 2024 01:07:55 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f85764e069052ebde3b88528c7a5ba363eddb4afdb279a0e3c3f88f086047a`  
		Last Modified: Thu, 12 Dec 2024 01:08:52 GMT  
		Size: 738.1 KB (738146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e226fd56bf3b0fea17f1d6097d0d76d569344e028ed8002371adb730f450f1`  
		Last Modified: Thu, 12 Dec 2024 01:08:52 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675157972e7dfc7d294dc71464fdfa631b9cd964d0ade85a7a0bb098f1739e7e`  
		Last Modified: Thu, 12 Dec 2024 01:08:52 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:d3cdabc2997fbb9eb5c3e57027869d526a2b518c2aeb49208ba6bacbe9210841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5fdd5cf7d6707bed1b309859925236066bc95efa6389dcd8d988660cf5f431`

```dockerfile
```

-	Layers:
	-	`sha256:111d60ec9b823588d8a578f29773b962f20cf088b208edda151ac35df389e550`  
		Last Modified: Thu, 12 Dec 2024 01:08:51 GMT  
		Size: 2.2 MB (2159406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b1c2c3afaa2c2d883884a06800fc18c3859999a936b023cce0428ea2e562ed`  
		Last Modified: Thu, 12 Dec 2024 01:08:51 GMT  
		Size: 30.7 KB (30664 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:05405855883dd01626b72eb307c78d95bba8cd7a5fa2828780200bd3a35af19c
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
$ docker pull composer@sha256:1e2d7273ccd17acb7c3492abb432220db1d3013bcf55c550555c71cfc37bc9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74091940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee07706e551cc6a6b3ad6ef4cfa1fa5af87339a7006a37ce31d66a4c52f6eb5`
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
	-	`sha256:bbcf41220f696f1ec3f3f3b53534f127b841636f0ca74e73210df73c7afefd94`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 13.6 MB (13573084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809689fb0b0450d700790c2f857ee46f0365fcb59cd3a227a736a8490de3c543`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ce08adea5bc33bdbdd66d6a505b2121998cfa91dd21b795b357eddd2e39b35`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 20.4 MB (20431405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ae36b542eb59f1f97688d2b4eff8d5e2772fe2c54c924a04d4b5c624307eea`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27d88523f19c0d0489fc13f34a3ce1166db9f0768337a9f3eccddfe7b511fbf`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 19.9 KB (19891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfa30f31250098695573d0af31f5d6241bcc6e651d4869a41bbb7dd377e83ba`  
		Last Modified: Thu, 12 Dec 2024 01:32:35 GMT  
		Size: 32.0 MB (32002990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad774222e92c8e35a5b78acc18db3f756bd2ab88623b5b116d1141660bc7e57`  
		Last Modified: Thu, 12 Dec 2024 01:32:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ac0e4ac113caea7eadd428f87ec7fdee449d348377f6f51919ef57267eb20`  
		Last Modified: Thu, 12 Dec 2024 01:33:11 GMT  
		Size: 734.9 KB (734945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337d5a2b89002f8d71e07df8e468d35f43bbb9adf04785a4384c20d479317d3d`  
		Last Modified: Thu, 12 Dec 2024 01:33:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ededd848983dff2aecf20fa9653ee5d7a7fc0f97e7b62129af777a5e8044d5ca`  
		Last Modified: Thu, 12 Dec 2024 01:33:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:0fa90e3cf424f9ac31146b878e2222466d9fb1f6b1bded5c697a684d8d0a9d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2193051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ba1993b74968107b5331cf5f2ecf6584cc97b8cb60d4a2cc436c912447b1ed`

```dockerfile
```

-	Layers:
	-	`sha256:18fbbfa34563d8030c88b1aa90af403d2778f2a37d5b8987ec0f8902ca8c54c2`  
		Last Modified: Thu, 12 Dec 2024 01:33:11 GMT  
		Size: 2.2 MB (2162265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6690f6046aaae684cb7236cdf58caae0bfcb2fcbce81177a978fb427851601`  
		Last Modified: Thu, 12 Dec 2024 01:33:10 GMT  
		Size: 30.8 KB (30786 bytes)  
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
$ docker pull composer@sha256:8cb3575258a34ce35f457eb65215c60278ea1aebd0bbbf9a37e2d14bfe1a8d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74404914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b478c43d543db5a53fe39603e1c4496194d9cba0cfd2f6b9ab6020fc9405a5bb`
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
	-	`sha256:7fedb1f25ba3b80074435858fc7794f83dc60e8736ca21254eab5159475f8ce4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 13.6 MB (13573088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c1315e733813b79535cafe40777595657596cda0a210db51f85480bfef1d4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee25f5bf4dbcae92e377529e99cb4c6fa1cddf3d1f43f8a63f4c01fffbc168f`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 21.4 MB (21362101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefb014c07c692f915ec490b55896346a687632ed71b8639d478c6573b16d88`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c7a618991f31a5ebdf26fbe9b53afeeaf94c829681cf294eb65ff6100da285`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 19.9 KB (19883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70251eda3f8e3a22e23ade26da5ea0d2b6dd1124907cb91a168a968d99172a4`  
		Last Modified: Thu, 12 Dec 2024 01:07:56 GMT  
		Size: 31.7 MB (31675572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071b32b1e7922ec5606ce28fd8866edd970297da1052a382440e3f930929be0`  
		Last Modified: Thu, 12 Dec 2024 01:07:55 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f85764e069052ebde3b88528c7a5ba363eddb4afdb279a0e3c3f88f086047a`  
		Last Modified: Thu, 12 Dec 2024 01:08:52 GMT  
		Size: 738.1 KB (738146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e226fd56bf3b0fea17f1d6097d0d76d569344e028ed8002371adb730f450f1`  
		Last Modified: Thu, 12 Dec 2024 01:08:52 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675157972e7dfc7d294dc71464fdfa631b9cd964d0ade85a7a0bb098f1739e7e`  
		Last Modified: Thu, 12 Dec 2024 01:08:52 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:d3cdabc2997fbb9eb5c3e57027869d526a2b518c2aeb49208ba6bacbe9210841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5fdd5cf7d6707bed1b309859925236066bc95efa6389dcd8d988660cf5f431`

```dockerfile
```

-	Layers:
	-	`sha256:111d60ec9b823588d8a578f29773b962f20cf088b208edda151ac35df389e550`  
		Last Modified: Thu, 12 Dec 2024 01:08:51 GMT  
		Size: 2.2 MB (2159406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b1c2c3afaa2c2d883884a06800fc18c3859999a936b023cce0428ea2e562ed`  
		Last Modified: Thu, 12 Dec 2024 01:08:51 GMT  
		Size: 30.7 KB (30664 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:05405855883dd01626b72eb307c78d95bba8cd7a5fa2828780200bd3a35af19c
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
$ docker pull composer@sha256:1e2d7273ccd17acb7c3492abb432220db1d3013bcf55c550555c71cfc37bc9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74091940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee07706e551cc6a6b3ad6ef4cfa1fa5af87339a7006a37ce31d66a4c52f6eb5`
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
	-	`sha256:bbcf41220f696f1ec3f3f3b53534f127b841636f0ca74e73210df73c7afefd94`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 13.6 MB (13573084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809689fb0b0450d700790c2f857ee46f0365fcb59cd3a227a736a8490de3c543`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ce08adea5bc33bdbdd66d6a505b2121998cfa91dd21b795b357eddd2e39b35`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 20.4 MB (20431405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ae36b542eb59f1f97688d2b4eff8d5e2772fe2c54c924a04d4b5c624307eea`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27d88523f19c0d0489fc13f34a3ce1166db9f0768337a9f3eccddfe7b511fbf`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 19.9 KB (19891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfa30f31250098695573d0af31f5d6241bcc6e651d4869a41bbb7dd377e83ba`  
		Last Modified: Thu, 12 Dec 2024 01:32:35 GMT  
		Size: 32.0 MB (32002990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad774222e92c8e35a5b78acc18db3f756bd2ab88623b5b116d1141660bc7e57`  
		Last Modified: Thu, 12 Dec 2024 01:32:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ac0e4ac113caea7eadd428f87ec7fdee449d348377f6f51919ef57267eb20`  
		Last Modified: Thu, 12 Dec 2024 01:33:11 GMT  
		Size: 734.9 KB (734945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337d5a2b89002f8d71e07df8e468d35f43bbb9adf04785a4384c20d479317d3d`  
		Last Modified: Thu, 12 Dec 2024 01:33:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ededd848983dff2aecf20fa9653ee5d7a7fc0f97e7b62129af777a5e8044d5ca`  
		Last Modified: Thu, 12 Dec 2024 01:33:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:0fa90e3cf424f9ac31146b878e2222466d9fb1f6b1bded5c697a684d8d0a9d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2193051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ba1993b74968107b5331cf5f2ecf6584cc97b8cb60d4a2cc436c912447b1ed`

```dockerfile
```

-	Layers:
	-	`sha256:18fbbfa34563d8030c88b1aa90af403d2778f2a37d5b8987ec0f8902ca8c54c2`  
		Last Modified: Thu, 12 Dec 2024 01:33:11 GMT  
		Size: 2.2 MB (2162265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6690f6046aaae684cb7236cdf58caae0bfcb2fcbce81177a978fb427851601`  
		Last Modified: Thu, 12 Dec 2024 01:33:10 GMT  
		Size: 30.8 KB (30786 bytes)  
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
$ docker pull composer@sha256:8cb3575258a34ce35f457eb65215c60278ea1aebd0bbbf9a37e2d14bfe1a8d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74404914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b478c43d543db5a53fe39603e1c4496194d9cba0cfd2f6b9ab6020fc9405a5bb`
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
	-	`sha256:7fedb1f25ba3b80074435858fc7794f83dc60e8736ca21254eab5159475f8ce4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 13.6 MB (13573088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c1315e733813b79535cafe40777595657596cda0a210db51f85480bfef1d4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee25f5bf4dbcae92e377529e99cb4c6fa1cddf3d1f43f8a63f4c01fffbc168f`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 21.4 MB (21362101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefb014c07c692f915ec490b55896346a687632ed71b8639d478c6573b16d88`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c7a618991f31a5ebdf26fbe9b53afeeaf94c829681cf294eb65ff6100da285`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 19.9 KB (19883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70251eda3f8e3a22e23ade26da5ea0d2b6dd1124907cb91a168a968d99172a4`  
		Last Modified: Thu, 12 Dec 2024 01:07:56 GMT  
		Size: 31.7 MB (31675572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071b32b1e7922ec5606ce28fd8866edd970297da1052a382440e3f930929be0`  
		Last Modified: Thu, 12 Dec 2024 01:07:55 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f85764e069052ebde3b88528c7a5ba363eddb4afdb279a0e3c3f88f086047a`  
		Last Modified: Thu, 12 Dec 2024 01:08:52 GMT  
		Size: 738.1 KB (738146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e226fd56bf3b0fea17f1d6097d0d76d569344e028ed8002371adb730f450f1`  
		Last Modified: Thu, 12 Dec 2024 01:08:52 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675157972e7dfc7d294dc71464fdfa631b9cd964d0ade85a7a0bb098f1739e7e`  
		Last Modified: Thu, 12 Dec 2024 01:08:52 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:d3cdabc2997fbb9eb5c3e57027869d526a2b518c2aeb49208ba6bacbe9210841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5fdd5cf7d6707bed1b309859925236066bc95efa6389dcd8d988660cf5f431`

```dockerfile
```

-	Layers:
	-	`sha256:111d60ec9b823588d8a578f29773b962f20cf088b208edda151ac35df389e550`  
		Last Modified: Thu, 12 Dec 2024 01:08:51 GMT  
		Size: 2.2 MB (2159406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b1c2c3afaa2c2d883884a06800fc18c3859999a936b023cce0428ea2e562ed`  
		Last Modified: Thu, 12 Dec 2024 01:08:51 GMT  
		Size: 30.7 KB (30664 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:94dcb77533422e67673ab9085fecdb809ab30664209cedcaf4eb953b4395f5f7
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
$ docker pull composer@sha256:f865e29c0603e1544ff28cc676e9eed77468591bd867936c277fce89dae561e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74797892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc8ea0ea6f2d835455b3bea9bd6ad04e8d031d6a1e29c7ed4a2502da428683e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:bbcf41220f696f1ec3f3f3b53534f127b841636f0ca74e73210df73c7afefd94`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 13.6 MB (13573084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809689fb0b0450d700790c2f857ee46f0365fcb59cd3a227a736a8490de3c543`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ce08adea5bc33bdbdd66d6a505b2121998cfa91dd21b795b357eddd2e39b35`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 20.4 MB (20431405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ae36b542eb59f1f97688d2b4eff8d5e2772fe2c54c924a04d4b5c624307eea`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27d88523f19c0d0489fc13f34a3ce1166db9f0768337a9f3eccddfe7b511fbf`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 19.9 KB (19891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfa30f31250098695573d0af31f5d6241bcc6e651d4869a41bbb7dd377e83ba`  
		Last Modified: Thu, 12 Dec 2024 01:32:35 GMT  
		Size: 32.0 MB (32002990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad774222e92c8e35a5b78acc18db3f756bd2ab88623b5b116d1141660bc7e57`  
		Last Modified: Thu, 12 Dec 2024 01:32:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3b22e3c620b5363ac187f16afa4d533caea356a3a80cbc5eee1e6e77b28d7`  
		Last Modified: Thu, 12 Dec 2024 19:27:08 GMT  
		Size: 1.4 MB (1440886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f290aa66bbfd2404a31b0d174e712550b028dd275c4a852db42604f79c8c9b3`  
		Last Modified: Thu, 12 Dec 2024 19:27:07 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b87d1132db24546259508b47776ae8e3d75028b81983a6abba1fcf6064a2c77`  
		Last Modified: Thu, 12 Dec 2024 19:27:06 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:6a6bd5a03665704be84b63a947ce9d87ca0c12d3b2584a17faf405091772db82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2194857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa72d8f5bbfbdd1e697bb2b0f909436d884d83a41fd98ddd7c59d55dc1df9b76`

```dockerfile
```

-	Layers:
	-	`sha256:2990268e2a1bcde30ec2f7e7028f67b79507e20aea295ca12ee0914b1eab368a`  
		Last Modified: Thu, 12 Dec 2024 19:27:07 GMT  
		Size: 2.2 MB (2163762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2406d1593a256be0aa22b809c95f41974e10cdcdee7cfb1094513cddf0364580`  
		Last Modified: Thu, 12 Dec 2024 19:27:07 GMT  
		Size: 31.1 KB (31095 bytes)  
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
$ docker pull composer@sha256:6d4a6bd39737764c9488247e86dde00facc86550884fc5891785c80faca2419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75135300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ef17730ba76bbcb7f6a23e6230065640cd61596b3d1a08496be790bbbfdff1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
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
	-	`sha256:7fedb1f25ba3b80074435858fc7794f83dc60e8736ca21254eab5159475f8ce4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 13.6 MB (13573088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c1315e733813b79535cafe40777595657596cda0a210db51f85480bfef1d4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee25f5bf4dbcae92e377529e99cb4c6fa1cddf3d1f43f8a63f4c01fffbc168f`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 21.4 MB (21362101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefb014c07c692f915ec490b55896346a687632ed71b8639d478c6573b16d88`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c7a618991f31a5ebdf26fbe9b53afeeaf94c829681cf294eb65ff6100da285`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 19.9 KB (19883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70251eda3f8e3a22e23ade26da5ea0d2b6dd1124907cb91a168a968d99172a4`  
		Last Modified: Thu, 12 Dec 2024 01:07:56 GMT  
		Size: 31.7 MB (31675572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071b32b1e7922ec5606ce28fd8866edd970297da1052a382440e3f930929be0`  
		Last Modified: Thu, 12 Dec 2024 01:07:55 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a92a012f3feed1d4e08d9f04ab2e9645d1b8bc17343d24d8cd23d415c6a279`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 1.5 MB (1468520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff550af47a42e0447290defc58101e57f28fad9981948968c184667c59cc2d3b`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698dc814782addf2ee7972b897afeacf919557cd8593cb6257b0b8e779c8bd8a`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:4c8b338ed397cd5d073db61e986e44aed3268437290559736d60cfd63f9726c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae45997a5dcb1ac218e35a3fc40f326d91caf431c354a59497bb9dbae8c43046`

```dockerfile
```

-	Layers:
	-	`sha256:fef4d070b413305ac5acb6e4e43f6e86a27acf04ed3faf5395c55b159f55055f`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 2.2 MB (2160891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57b85fbfc928b1829521c63148678189a32ece7509374bd56f6bd02d4f6fec15`  
		Last Modified: Thu, 12 Dec 2024 19:28:26 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:a4540d5136eff247cff5080104f4adeab80916831db6e62476a7bcb29ae73e0b
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
$ docker pull composer@sha256:9ceea854e08c0340f1f563236a9a2da4a34ca1b34d8e6f54c72b2e7ab94787fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74653900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0951f4d6770678c5208b7e91d9bcbd1bbad826d973b6d2708d59137e66957379`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:bbcf41220f696f1ec3f3f3b53534f127b841636f0ca74e73210df73c7afefd94`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 13.6 MB (13573084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809689fb0b0450d700790c2f857ee46f0365fcb59cd3a227a736a8490de3c543`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ce08adea5bc33bdbdd66d6a505b2121998cfa91dd21b795b357eddd2e39b35`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 20.4 MB (20431405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ae36b542eb59f1f97688d2b4eff8d5e2772fe2c54c924a04d4b5c624307eea`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27d88523f19c0d0489fc13f34a3ce1166db9f0768337a9f3eccddfe7b511fbf`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 19.9 KB (19891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfa30f31250098695573d0af31f5d6241bcc6e651d4869a41bbb7dd377e83ba`  
		Last Modified: Thu, 12 Dec 2024 01:32:35 GMT  
		Size: 32.0 MB (32002990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad774222e92c8e35a5b78acc18db3f756bd2ab88623b5b116d1141660bc7e57`  
		Last Modified: Thu, 12 Dec 2024 01:32:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714e9f3b60701b820b1229a2c085c6a42cd6d641648c8e294a7ef6224c2995ea`  
		Last Modified: Thu, 12 Dec 2024 19:27:44 GMT  
		Size: 1.3 MB (1296894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1053635d638953cfe4b04b2255c3f6c2b6b9b7a29974b8aebffd10e76e5080`  
		Last Modified: Thu, 12 Dec 2024 19:27:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc762272b07fd8ea8045b4e579c131206f3889dff3a00b8bfcdab8cc5f1baf02`  
		Last Modified: Thu, 12 Dec 2024 19:27:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:95f6e131ae36866d64851af153c64173e35622afdefa20bbb681f1b2a183d6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2194235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701308b71439d5d5d1cc5cbf772a55370857acf12c27aa07e0b529302e6a8a12`

```dockerfile
```

-	Layers:
	-	`sha256:d2a1c2d0dd6a7961b0b76842aeb361885d85ea0ff36128301e870aaebbf45166`  
		Last Modified: Thu, 12 Dec 2024 19:27:43 GMT  
		Size: 2.2 MB (2163456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13946642c18e0052fde1e7b3c40c908fd2da72e14ee0812a7a07418173f85295`  
		Last Modified: Thu, 12 Dec 2024 19:27:43 GMT  
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
$ docker pull composer@sha256:fa4cd33728088e01893ffe54098e10ca272c1880b3d6e9c4257423374cf49bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74991156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5710fcf0a73bbdc55abd3670a2a9659946a8e7374e2b1d815f491af5a7feabb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
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
	-	`sha256:7fedb1f25ba3b80074435858fc7794f83dc60e8736ca21254eab5159475f8ce4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 13.6 MB (13573088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c1315e733813b79535cafe40777595657596cda0a210db51f85480bfef1d4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee25f5bf4dbcae92e377529e99cb4c6fa1cddf3d1f43f8a63f4c01fffbc168f`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 21.4 MB (21362101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefb014c07c692f915ec490b55896346a687632ed71b8639d478c6573b16d88`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c7a618991f31a5ebdf26fbe9b53afeeaf94c829681cf294eb65ff6100da285`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 19.9 KB (19883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70251eda3f8e3a22e23ade26da5ea0d2b6dd1124907cb91a168a968d99172a4`  
		Last Modified: Thu, 12 Dec 2024 01:07:56 GMT  
		Size: 31.7 MB (31675572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071b32b1e7922ec5606ce28fd8866edd970297da1052a382440e3f930929be0`  
		Last Modified: Thu, 12 Dec 2024 01:07:55 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c7af96732a60a60018b4694b1ec404d65626fbb26659638f99aaea3166908c`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 1.3 MB (1324377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d42b3595f6646482a611de916e32173dd2400620f470fb0cb95d345d7a499bc`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940f027ec6bc203545e87fd444f9dd5b6ab6b921505d7e48759531cfd27fe382`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:47edd55f9ea3c26980f074b39586faffc9cec3a2c16078d490684f15b1633cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6879f872b4dbecba400dd9d63a7bf9ae07005fab1d1846481c7e6fe872d0b9`

```dockerfile
```

-	Layers:
	-	`sha256:7b1ae057ce7fdfb2d2b7fb106fcf429a01c59233b82c91cd6eedec2244551125`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 2.2 MB (2160597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38dea7ed434db90dff60a7903568034aae2581d1640719085942204bbb102925`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 30.7 KB (30656 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.25`

```console
$ docker pull composer@sha256:a4540d5136eff247cff5080104f4adeab80916831db6e62476a7bcb29ae73e0b
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
$ docker pull composer@sha256:9ceea854e08c0340f1f563236a9a2da4a34ca1b34d8e6f54c72b2e7ab94787fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74653900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0951f4d6770678c5208b7e91d9bcbd1bbad826d973b6d2708d59137e66957379`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:bbcf41220f696f1ec3f3f3b53534f127b841636f0ca74e73210df73c7afefd94`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 13.6 MB (13573084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809689fb0b0450d700790c2f857ee46f0365fcb59cd3a227a736a8490de3c543`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ce08adea5bc33bdbdd66d6a505b2121998cfa91dd21b795b357eddd2e39b35`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 20.4 MB (20431405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ae36b542eb59f1f97688d2b4eff8d5e2772fe2c54c924a04d4b5c624307eea`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27d88523f19c0d0489fc13f34a3ce1166db9f0768337a9f3eccddfe7b511fbf`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 19.9 KB (19891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfa30f31250098695573d0af31f5d6241bcc6e651d4869a41bbb7dd377e83ba`  
		Last Modified: Thu, 12 Dec 2024 01:32:35 GMT  
		Size: 32.0 MB (32002990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad774222e92c8e35a5b78acc18db3f756bd2ab88623b5b116d1141660bc7e57`  
		Last Modified: Thu, 12 Dec 2024 01:32:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714e9f3b60701b820b1229a2c085c6a42cd6d641648c8e294a7ef6224c2995ea`  
		Last Modified: Thu, 12 Dec 2024 19:27:44 GMT  
		Size: 1.3 MB (1296894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1053635d638953cfe4b04b2255c3f6c2b6b9b7a29974b8aebffd10e76e5080`  
		Last Modified: Thu, 12 Dec 2024 19:27:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc762272b07fd8ea8045b4e579c131206f3889dff3a00b8bfcdab8cc5f1baf02`  
		Last Modified: Thu, 12 Dec 2024 19:27:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:95f6e131ae36866d64851af153c64173e35622afdefa20bbb681f1b2a183d6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2194235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701308b71439d5d5d1cc5cbf772a55370857acf12c27aa07e0b529302e6a8a12`

```dockerfile
```

-	Layers:
	-	`sha256:d2a1c2d0dd6a7961b0b76842aeb361885d85ea0ff36128301e870aaebbf45166`  
		Last Modified: Thu, 12 Dec 2024 19:27:43 GMT  
		Size: 2.2 MB (2163456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13946642c18e0052fde1e7b3c40c908fd2da72e14ee0812a7a07418173f85295`  
		Last Modified: Thu, 12 Dec 2024 19:27:43 GMT  
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
$ docker pull composer@sha256:fa4cd33728088e01893ffe54098e10ca272c1880b3d6e9c4257423374cf49bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74991156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5710fcf0a73bbdc55abd3670a2a9659946a8e7374e2b1d815f491af5a7feabb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
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
	-	`sha256:7fedb1f25ba3b80074435858fc7794f83dc60e8736ca21254eab5159475f8ce4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 13.6 MB (13573088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c1315e733813b79535cafe40777595657596cda0a210db51f85480bfef1d4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee25f5bf4dbcae92e377529e99cb4c6fa1cddf3d1f43f8a63f4c01fffbc168f`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 21.4 MB (21362101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefb014c07c692f915ec490b55896346a687632ed71b8639d478c6573b16d88`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c7a618991f31a5ebdf26fbe9b53afeeaf94c829681cf294eb65ff6100da285`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 19.9 KB (19883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70251eda3f8e3a22e23ade26da5ea0d2b6dd1124907cb91a168a968d99172a4`  
		Last Modified: Thu, 12 Dec 2024 01:07:56 GMT  
		Size: 31.7 MB (31675572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071b32b1e7922ec5606ce28fd8866edd970297da1052a382440e3f930929be0`  
		Last Modified: Thu, 12 Dec 2024 01:07:55 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c7af96732a60a60018b4694b1ec404d65626fbb26659638f99aaea3166908c`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 1.3 MB (1324377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d42b3595f6646482a611de916e32173dd2400620f470fb0cb95d345d7a499bc`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940f027ec6bc203545e87fd444f9dd5b6ab6b921505d7e48759531cfd27fe382`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:47edd55f9ea3c26980f074b39586faffc9cec3a2c16078d490684f15b1633cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6879f872b4dbecba400dd9d63a7bf9ae07005fab1d1846481c7e6fe872d0b9`

```dockerfile
```

-	Layers:
	-	`sha256:7b1ae057ce7fdfb2d2b7fb106fcf429a01c59233b82c91cd6eedec2244551125`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 2.2 MB (2160597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38dea7ed434db90dff60a7903568034aae2581d1640719085942204bbb102925`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 30.7 KB (30656 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8`

```console
$ docker pull composer@sha256:94dcb77533422e67673ab9085fecdb809ab30664209cedcaf4eb953b4395f5f7
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
$ docker pull composer@sha256:f865e29c0603e1544ff28cc676e9eed77468591bd867936c277fce89dae561e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74797892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc8ea0ea6f2d835455b3bea9bd6ad04e8d031d6a1e29c7ed4a2502da428683e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:bbcf41220f696f1ec3f3f3b53534f127b841636f0ca74e73210df73c7afefd94`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 13.6 MB (13573084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809689fb0b0450d700790c2f857ee46f0365fcb59cd3a227a736a8490de3c543`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ce08adea5bc33bdbdd66d6a505b2121998cfa91dd21b795b357eddd2e39b35`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 20.4 MB (20431405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ae36b542eb59f1f97688d2b4eff8d5e2772fe2c54c924a04d4b5c624307eea`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27d88523f19c0d0489fc13f34a3ce1166db9f0768337a9f3eccddfe7b511fbf`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 19.9 KB (19891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfa30f31250098695573d0af31f5d6241bcc6e651d4869a41bbb7dd377e83ba`  
		Last Modified: Thu, 12 Dec 2024 01:32:35 GMT  
		Size: 32.0 MB (32002990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad774222e92c8e35a5b78acc18db3f756bd2ab88623b5b116d1141660bc7e57`  
		Last Modified: Thu, 12 Dec 2024 01:32:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3b22e3c620b5363ac187f16afa4d533caea356a3a80cbc5eee1e6e77b28d7`  
		Last Modified: Thu, 12 Dec 2024 19:27:08 GMT  
		Size: 1.4 MB (1440886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f290aa66bbfd2404a31b0d174e712550b028dd275c4a852db42604f79c8c9b3`  
		Last Modified: Thu, 12 Dec 2024 19:27:07 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b87d1132db24546259508b47776ae8e3d75028b81983a6abba1fcf6064a2c77`  
		Last Modified: Thu, 12 Dec 2024 19:27:06 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:6a6bd5a03665704be84b63a947ce9d87ca0c12d3b2584a17faf405091772db82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2194857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa72d8f5bbfbdd1e697bb2b0f909436d884d83a41fd98ddd7c59d55dc1df9b76`

```dockerfile
```

-	Layers:
	-	`sha256:2990268e2a1bcde30ec2f7e7028f67b79507e20aea295ca12ee0914b1eab368a`  
		Last Modified: Thu, 12 Dec 2024 19:27:07 GMT  
		Size: 2.2 MB (2163762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2406d1593a256be0aa22b809c95f41974e10cdcdee7cfb1094513cddf0364580`  
		Last Modified: Thu, 12 Dec 2024 19:27:07 GMT  
		Size: 31.1 KB (31095 bytes)  
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
$ docker pull composer@sha256:6d4a6bd39737764c9488247e86dde00facc86550884fc5891785c80faca2419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75135300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ef17730ba76bbcb7f6a23e6230065640cd61596b3d1a08496be790bbbfdff1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
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
	-	`sha256:7fedb1f25ba3b80074435858fc7794f83dc60e8736ca21254eab5159475f8ce4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 13.6 MB (13573088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c1315e733813b79535cafe40777595657596cda0a210db51f85480bfef1d4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee25f5bf4dbcae92e377529e99cb4c6fa1cddf3d1f43f8a63f4c01fffbc168f`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 21.4 MB (21362101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefb014c07c692f915ec490b55896346a687632ed71b8639d478c6573b16d88`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c7a618991f31a5ebdf26fbe9b53afeeaf94c829681cf294eb65ff6100da285`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 19.9 KB (19883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70251eda3f8e3a22e23ade26da5ea0d2b6dd1124907cb91a168a968d99172a4`  
		Last Modified: Thu, 12 Dec 2024 01:07:56 GMT  
		Size: 31.7 MB (31675572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071b32b1e7922ec5606ce28fd8866edd970297da1052a382440e3f930929be0`  
		Last Modified: Thu, 12 Dec 2024 01:07:55 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a92a012f3feed1d4e08d9f04ab2e9645d1b8bc17343d24d8cd23d415c6a279`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 1.5 MB (1468520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff550af47a42e0447290defc58101e57f28fad9981948968c184667c59cc2d3b`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698dc814782addf2ee7972b897afeacf919557cd8593cb6257b0b8e779c8bd8a`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:4c8b338ed397cd5d073db61e986e44aed3268437290559736d60cfd63f9726c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae45997a5dcb1ac218e35a3fc40f326d91caf431c354a59497bb9dbae8c43046`

```dockerfile
```

-	Layers:
	-	`sha256:fef4d070b413305ac5acb6e4e43f6e86a27acf04ed3faf5395c55b159f55055f`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 2.2 MB (2160891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57b85fbfc928b1829521c63148678189a32ece7509374bd56f6bd02d4f6fec15`  
		Last Modified: Thu, 12 Dec 2024 19:28:26 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8.4`

```console
$ docker pull composer@sha256:94dcb77533422e67673ab9085fecdb809ab30664209cedcaf4eb953b4395f5f7
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
$ docker pull composer@sha256:f865e29c0603e1544ff28cc676e9eed77468591bd867936c277fce89dae561e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74797892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc8ea0ea6f2d835455b3bea9bd6ad04e8d031d6a1e29c7ed4a2502da428683e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:bbcf41220f696f1ec3f3f3b53534f127b841636f0ca74e73210df73c7afefd94`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 13.6 MB (13573084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809689fb0b0450d700790c2f857ee46f0365fcb59cd3a227a736a8490de3c543`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ce08adea5bc33bdbdd66d6a505b2121998cfa91dd21b795b357eddd2e39b35`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 20.4 MB (20431405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ae36b542eb59f1f97688d2b4eff8d5e2772fe2c54c924a04d4b5c624307eea`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27d88523f19c0d0489fc13f34a3ce1166db9f0768337a9f3eccddfe7b511fbf`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 19.9 KB (19891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfa30f31250098695573d0af31f5d6241bcc6e651d4869a41bbb7dd377e83ba`  
		Last Modified: Thu, 12 Dec 2024 01:32:35 GMT  
		Size: 32.0 MB (32002990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad774222e92c8e35a5b78acc18db3f756bd2ab88623b5b116d1141660bc7e57`  
		Last Modified: Thu, 12 Dec 2024 01:32:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3b22e3c620b5363ac187f16afa4d533caea356a3a80cbc5eee1e6e77b28d7`  
		Last Modified: Thu, 12 Dec 2024 19:27:08 GMT  
		Size: 1.4 MB (1440886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f290aa66bbfd2404a31b0d174e712550b028dd275c4a852db42604f79c8c9b3`  
		Last Modified: Thu, 12 Dec 2024 19:27:07 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b87d1132db24546259508b47776ae8e3d75028b81983a6abba1fcf6064a2c77`  
		Last Modified: Thu, 12 Dec 2024 19:27:06 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:6a6bd5a03665704be84b63a947ce9d87ca0c12d3b2584a17faf405091772db82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2194857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa72d8f5bbfbdd1e697bb2b0f909436d884d83a41fd98ddd7c59d55dc1df9b76`

```dockerfile
```

-	Layers:
	-	`sha256:2990268e2a1bcde30ec2f7e7028f67b79507e20aea295ca12ee0914b1eab368a`  
		Last Modified: Thu, 12 Dec 2024 19:27:07 GMT  
		Size: 2.2 MB (2163762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2406d1593a256be0aa22b809c95f41974e10cdcdee7cfb1094513cddf0364580`  
		Last Modified: Thu, 12 Dec 2024 19:27:07 GMT  
		Size: 31.1 KB (31095 bytes)  
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
$ docker pull composer@sha256:6d4a6bd39737764c9488247e86dde00facc86550884fc5891785c80faca2419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75135300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ef17730ba76bbcb7f6a23e6230065640cd61596b3d1a08496be790bbbfdff1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
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
	-	`sha256:7fedb1f25ba3b80074435858fc7794f83dc60e8736ca21254eab5159475f8ce4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 13.6 MB (13573088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c1315e733813b79535cafe40777595657596cda0a210db51f85480bfef1d4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee25f5bf4dbcae92e377529e99cb4c6fa1cddf3d1f43f8a63f4c01fffbc168f`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 21.4 MB (21362101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefb014c07c692f915ec490b55896346a687632ed71b8639d478c6573b16d88`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c7a618991f31a5ebdf26fbe9b53afeeaf94c829681cf294eb65ff6100da285`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 19.9 KB (19883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70251eda3f8e3a22e23ade26da5ea0d2b6dd1124907cb91a168a968d99172a4`  
		Last Modified: Thu, 12 Dec 2024 01:07:56 GMT  
		Size: 31.7 MB (31675572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071b32b1e7922ec5606ce28fd8866edd970297da1052a382440e3f930929be0`  
		Last Modified: Thu, 12 Dec 2024 01:07:55 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a92a012f3feed1d4e08d9f04ab2e9645d1b8bc17343d24d8cd23d415c6a279`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 1.5 MB (1468520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff550af47a42e0447290defc58101e57f28fad9981948968c184667c59cc2d3b`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698dc814782addf2ee7972b897afeacf919557cd8593cb6257b0b8e779c8bd8a`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.4` - unknown; unknown

```console
$ docker pull composer@sha256:4c8b338ed397cd5d073db61e986e44aed3268437290559736d60cfd63f9726c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae45997a5dcb1ac218e35a3fc40f326d91caf431c354a59497bb9dbae8c43046`

```dockerfile
```

-	Layers:
	-	`sha256:fef4d070b413305ac5acb6e4e43f6e86a27acf04ed3faf5395c55b159f55055f`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 2.2 MB (2160891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57b85fbfc928b1829521c63148678189a32ece7509374bd56f6bd02d4f6fec15`  
		Last Modified: Thu, 12 Dec 2024 19:28:26 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:94dcb77533422e67673ab9085fecdb809ab30664209cedcaf4eb953b4395f5f7
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
$ docker pull composer@sha256:f865e29c0603e1544ff28cc676e9eed77468591bd867936c277fce89dae561e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74797892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc8ea0ea6f2d835455b3bea9bd6ad04e8d031d6a1e29c7ed4a2502da428683e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:bbcf41220f696f1ec3f3f3b53534f127b841636f0ca74e73210df73c7afefd94`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 13.6 MB (13573084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809689fb0b0450d700790c2f857ee46f0365fcb59cd3a227a736a8490de3c543`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ce08adea5bc33bdbdd66d6a505b2121998cfa91dd21b795b357eddd2e39b35`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 20.4 MB (20431405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ae36b542eb59f1f97688d2b4eff8d5e2772fe2c54c924a04d4b5c624307eea`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27d88523f19c0d0489fc13f34a3ce1166db9f0768337a9f3eccddfe7b511fbf`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 19.9 KB (19891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfa30f31250098695573d0af31f5d6241bcc6e651d4869a41bbb7dd377e83ba`  
		Last Modified: Thu, 12 Dec 2024 01:32:35 GMT  
		Size: 32.0 MB (32002990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad774222e92c8e35a5b78acc18db3f756bd2ab88623b5b116d1141660bc7e57`  
		Last Modified: Thu, 12 Dec 2024 01:32:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed3b22e3c620b5363ac187f16afa4d533caea356a3a80cbc5eee1e6e77b28d7`  
		Last Modified: Thu, 12 Dec 2024 19:27:08 GMT  
		Size: 1.4 MB (1440886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f290aa66bbfd2404a31b0d174e712550b028dd275c4a852db42604f79c8c9b3`  
		Last Modified: Thu, 12 Dec 2024 19:27:07 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b87d1132db24546259508b47776ae8e3d75028b81983a6abba1fcf6064a2c77`  
		Last Modified: Thu, 12 Dec 2024 19:27:06 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:6a6bd5a03665704be84b63a947ce9d87ca0c12d3b2584a17faf405091772db82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2194857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa72d8f5bbfbdd1e697bb2b0f909436d884d83a41fd98ddd7c59d55dc1df9b76`

```dockerfile
```

-	Layers:
	-	`sha256:2990268e2a1bcde30ec2f7e7028f67b79507e20aea295ca12ee0914b1eab368a`  
		Last Modified: Thu, 12 Dec 2024 19:27:07 GMT  
		Size: 2.2 MB (2163762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2406d1593a256be0aa22b809c95f41974e10cdcdee7cfb1094513cddf0364580`  
		Last Modified: Thu, 12 Dec 2024 19:27:07 GMT  
		Size: 31.1 KB (31095 bytes)  
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
$ docker pull composer@sha256:6d4a6bd39737764c9488247e86dde00facc86550884fc5891785c80faca2419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75135300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ef17730ba76bbcb7f6a23e6230065640cd61596b3d1a08496be790bbbfdff1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
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
	-	`sha256:7fedb1f25ba3b80074435858fc7794f83dc60e8736ca21254eab5159475f8ce4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 13.6 MB (13573088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c1315e733813b79535cafe40777595657596cda0a210db51f85480bfef1d4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee25f5bf4dbcae92e377529e99cb4c6fa1cddf3d1f43f8a63f4c01fffbc168f`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 21.4 MB (21362101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefb014c07c692f915ec490b55896346a687632ed71b8639d478c6573b16d88`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c7a618991f31a5ebdf26fbe9b53afeeaf94c829681cf294eb65ff6100da285`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 19.9 KB (19883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70251eda3f8e3a22e23ade26da5ea0d2b6dd1124907cb91a168a968d99172a4`  
		Last Modified: Thu, 12 Dec 2024 01:07:56 GMT  
		Size: 31.7 MB (31675572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071b32b1e7922ec5606ce28fd8866edd970297da1052a382440e3f930929be0`  
		Last Modified: Thu, 12 Dec 2024 01:07:55 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a92a012f3feed1d4e08d9f04ab2e9645d1b8bc17343d24d8cd23d415c6a279`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 1.5 MB (1468520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff550af47a42e0447290defc58101e57f28fad9981948968c184667c59cc2d3b`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698dc814782addf2ee7972b897afeacf919557cd8593cb6257b0b8e779c8bd8a`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:4c8b338ed397cd5d073db61e986e44aed3268437290559736d60cfd63f9726c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae45997a5dcb1ac218e35a3fc40f326d91caf431c354a59497bb9dbae8c43046`

```dockerfile
```

-	Layers:
	-	`sha256:fef4d070b413305ac5acb6e4e43f6e86a27acf04ed3faf5395c55b159f55055f`  
		Last Modified: Thu, 12 Dec 2024 19:28:27 GMT  
		Size: 2.2 MB (2160891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57b85fbfc928b1829521c63148678189a32ece7509374bd56f6bd02d4f6fec15`  
		Last Modified: Thu, 12 Dec 2024 19:28:26 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:lts`

```console
$ docker pull composer@sha256:a4540d5136eff247cff5080104f4adeab80916831db6e62476a7bcb29ae73e0b
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
$ docker pull composer@sha256:9ceea854e08c0340f1f563236a9a2da4a34ca1b34d8e6f54c72b2e7ab94787fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74653900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0951f4d6770678c5208b7e91d9bcbd1bbad826d973b6d2708d59137e66957379`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:bbcf41220f696f1ec3f3f3b53534f127b841636f0ca74e73210df73c7afefd94`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 13.6 MB (13573084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809689fb0b0450d700790c2f857ee46f0365fcb59cd3a227a736a8490de3c543`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ce08adea5bc33bdbdd66d6a505b2121998cfa91dd21b795b357eddd2e39b35`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 20.4 MB (20431405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ae36b542eb59f1f97688d2b4eff8d5e2772fe2c54c924a04d4b5c624307eea`  
		Last Modified: Wed, 11 Dec 2024 23:45:43 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27d88523f19c0d0489fc13f34a3ce1166db9f0768337a9f3eccddfe7b511fbf`  
		Last Modified: Wed, 11 Dec 2024 23:45:44 GMT  
		Size: 19.9 KB (19891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfa30f31250098695573d0af31f5d6241bcc6e651d4869a41bbb7dd377e83ba`  
		Last Modified: Thu, 12 Dec 2024 01:32:35 GMT  
		Size: 32.0 MB (32002990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad774222e92c8e35a5b78acc18db3f756bd2ab88623b5b116d1141660bc7e57`  
		Last Modified: Thu, 12 Dec 2024 01:32:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714e9f3b60701b820b1229a2c085c6a42cd6d641648c8e294a7ef6224c2995ea`  
		Last Modified: Thu, 12 Dec 2024 19:27:44 GMT  
		Size: 1.3 MB (1296894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1053635d638953cfe4b04b2255c3f6c2b6b9b7a29974b8aebffd10e76e5080`  
		Last Modified: Thu, 12 Dec 2024 19:27:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc762272b07fd8ea8045b4e579c131206f3889dff3a00b8bfcdab8cc5f1baf02`  
		Last Modified: Thu, 12 Dec 2024 19:27:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:95f6e131ae36866d64851af153c64173e35622afdefa20bbb681f1b2a183d6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2194235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701308b71439d5d5d1cc5cbf772a55370857acf12c27aa07e0b529302e6a8a12`

```dockerfile
```

-	Layers:
	-	`sha256:d2a1c2d0dd6a7961b0b76842aeb361885d85ea0ff36128301e870aaebbf45166`  
		Last Modified: Thu, 12 Dec 2024 19:27:43 GMT  
		Size: 2.2 MB (2163456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13946642c18e0052fde1e7b3c40c908fd2da72e14ee0812a7a07418173f85295`  
		Last Modified: Thu, 12 Dec 2024 19:27:43 GMT  
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
$ docker pull composer@sha256:fa4cd33728088e01893ffe54098e10ca272c1880b3d6e9c4257423374cf49bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74991156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5710fcf0a73bbdc55abd3670a2a9659946a8e7374e2b1d815f491af5a7feabb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
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
	-	`sha256:7fedb1f25ba3b80074435858fc7794f83dc60e8736ca21254eab5159475f8ce4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 13.6 MB (13573088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c1315e733813b79535cafe40777595657596cda0a210db51f85480bfef1d4`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee25f5bf4dbcae92e377529e99cb4c6fa1cddf3d1f43f8a63f4c01fffbc168f`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 21.4 MB (21362101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefb014c07c692f915ec490b55896346a687632ed71b8639d478c6573b16d88`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c7a618991f31a5ebdf26fbe9b53afeeaf94c829681cf294eb65ff6100da285`  
		Last Modified: Wed, 11 Dec 2024 23:44:53 GMT  
		Size: 19.9 KB (19883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70251eda3f8e3a22e23ade26da5ea0d2b6dd1124907cb91a168a968d99172a4`  
		Last Modified: Thu, 12 Dec 2024 01:07:56 GMT  
		Size: 31.7 MB (31675572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071b32b1e7922ec5606ce28fd8866edd970297da1052a382440e3f930929be0`  
		Last Modified: Thu, 12 Dec 2024 01:07:55 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c7af96732a60a60018b4694b1ec404d65626fbb26659638f99aaea3166908c`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 1.3 MB (1324377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d42b3595f6646482a611de916e32173dd2400620f470fb0cb95d345d7a499bc`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940f027ec6bc203545e87fd444f9dd5b6ab6b921505d7e48759531cfd27fe382`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:47edd55f9ea3c26980f074b39586faffc9cec3a2c16078d490684f15b1633cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2191253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6879f872b4dbecba400dd9d63a7bf9ae07005fab1d1846481c7e6fe872d0b9`

```dockerfile
```

-	Layers:
	-	`sha256:7b1ae057ce7fdfb2d2b7fb106fcf429a01c59233b82c91cd6eedec2244551125`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 2.2 MB (2160597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38dea7ed434db90dff60a7903568034aae2581d1640719085942204bbb102925`  
		Last Modified: Thu, 12 Dec 2024 19:27:33 GMT  
		Size: 30.7 KB (30656 bytes)  
		MIME: application/vnd.in-toto+json
