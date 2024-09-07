<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.27`](#composer11027)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.24`](#composer2224)
-	[`composer:2.7`](#composer27)
-	[`composer:2.7.9`](#composer279)
-	[`composer:latest`](#composerlatest)
-	[`composer:lts`](#composerlts)

## `composer:1`

```console
$ docker pull composer@sha256:0f1e587f773ca5e7595477b84613de9a54d273c4acb059b33d657c2ee0214545
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
$ docker pull composer@sha256:7854521ce3fd2f7018636256bbd5f679989e11d82e5cb07058877e7d3cfcbdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68024536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a81db78c15dfdce65ef829acee8c47c9d6ec3e1ebed3baf688b2407fec3c9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15916673af8229814dcc44164d4616a6141bc5b586ae9362e741d64c6e4c91`  
		Last Modified: Sat, 07 Sep 2024 02:15:12 GMT  
		Size: 3.3 MB (3282678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb3258c4c6a46b7e182fa372bfe03ff37fd0fdf7f6894ca97b564fc382d7d4`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e436918c34ed4c536bdbaeace5213a8aaeb796ec65951fe681a10758ae2677`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6c87b6d10c2d5a9226b306e7fc3370cab80f9f41fe049706de7a51f8e1cf5a`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 12.5 MB (12502103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90d2c6f0ff71e78e4e311ebe4b83b2abbe5fdda23eaa28c5711e68b23c578da`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5cf8a88be3fd539ff5a60321e916df9fa78268109a78972d9411217023bf61`  
		Last Modified: Sat, 07 Sep 2024 02:16:52 GMT  
		Size: 17.2 MB (17212749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eea6dbc4cb9e274ad2228dfea58ecabec99b9336c8d528206ce4c41f6724ad`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f889a53b48220a2103d38ac31ed15adb68d8e5de71c03c475792439675576304`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb4916ca53279f53edcf4b1c977dc7e5486001fedd925f6f199dedd6ae2676f`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 30.6 MB (30647241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecd4819a1382c724645ef5ff5d4bd4d1965de9778a21ae7420bbdd5c3ae74fe`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a740ee85731801e28fc6e072e0d7bb053ae59e466ca49d36c96c1dd7effebd1`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 731.4 KB (731387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0973440a5cb6fedc1a58ba74cd8270d1b173a9790fefa3a888df4b068ceac95`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db0479371de30561eeeb00b17d7b75c81ac293dcf11c4556cb6a71bc59ac403`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:028263803ca2ed519100a3b2bdf013e15f3aea5168e06e28b29e6ea2d3f9d9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ea06e5499dc5df530faab4964eeb1b8b7b8034f78c96d6cb0f3f787b3f3fa0`

```dockerfile
```

-	Layers:
	-	`sha256:85becb9c92c63dffe4fd4e8196f79847b3607a47759bd80a8bc308d536c36658`  
		Last Modified: Sat, 07 Sep 2024 02:57:23 GMT  
		Size: 2.1 MB (2146087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c226f930338ccc811566d219d9faf7762a79c3c513fd7fe8f4767d94c648efa`  
		Last Modified: Sat, 07 Sep 2024 02:57:23 GMT  
		Size: 30.8 KB (30837 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:b6d5c099fa88cc921d8c7242bba125d7fbf0da0c32fcfad59eabf114d1f56e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65696796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77813782d8700088cb00c975415e0bd2ddd265f87e37140781ba41d87c964c6c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b041a1a670328abed5fe2b73e068aba477e969ddbfe65c606c8054a4c36067b2`  
		Last Modified: Tue, 23 Jul 2024 01:00:35 GMT  
		Size: 3.3 MB (3263638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51daa6109cd19af541c6fc2600ad5a2f2382e50d3938e2b51f30d24df583fee`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b57c8706e4f06f42a10294d5c9eef985613e48298dedb390c6e6816b60a8f78`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b27cb594dc713e8223f5363b7505f762ad934cbf1c4f47ed7885c05db8e13`  
		Last Modified: Fri, 30 Aug 2024 20:20:12 GMT  
		Size: 12.5 MB (12502099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22237d0261563edb9ca222f6a36c5e175cf1d62c16f38e41755982d955f0e39c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ea243fc20547ec3f93ecbe653822d8a49a7c9c61fd5b7ad229cf6ee331209`  
		Last Modified: Fri, 30 Aug 2024 20:20:15 GMT  
		Size: 16.4 MB (16360114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a08c99e5b1cb1537070b37b1f8f3c78a107be7dd6efdd3a197aa7867d3d7a5c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68481b9e1f3b14557aa8d598c31b8ec7b735f77a5aeac9431ef7b69560d46a92`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c939352561246c630164d6835a0997969adc47f5e678a95dc31e21f57e94926d`  
		Last Modified: Fri, 30 Aug 2024 21:19:20 GMT  
		Size: 29.5 MB (29450758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f957f60156f9b6e900c9f3e132d2e377afa2f2d79dd2350288d3c3cf994fc2`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec8fc3636cf8ae1505b2708291b352bb5c4fee94abe1cd819c8e2c53e6a9049`  
		Last Modified: Fri, 30 Aug 2024 21:20:02 GMT  
		Size: 730.6 KB (730626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5e376500c1dbf9e6b542bbd48cd51904faf1049e0278e1c2b18582fa895d55`  
		Last Modified: Fri, 30 Aug 2024 21:20:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69655ab9a4e94d9f6e302be56113fb79772c50b4c1630c34fec4940208712f1d`  
		Last Modified: Fri, 30 Aug 2024 21:20:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:3b80e0e7c88f074c2dc3fac1c5bf0ca63621267dd0c4d4c6ced4c03ad081f650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eba2ef3743ea56174ec791b48c8a2ce9972013ffd59c6286bd3fbc4247014a2`

```dockerfile
```

-	Layers:
	-	`sha256:149df9329ac2ea8c63c732c77999b219899fa2887f8864d08a94c8bd9471abaa`  
		Last Modified: Fri, 30 Aug 2024 21:20:01 GMT  
		Size: 30.7 KB (30670 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:14ad6f124ececd98cfecf19cc0913ddd2d82d2ca6365a21ce688b9dace31463a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63793116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99550fa2d8788346f4167dd3b2b259e8c63df4b79aa2d98ea8e2c6c7c4af9ed7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57db3d4836535044109c42cf341df21ab1def6a06fecbaf98ffac833b47f15b`  
		Last Modified: Tue, 23 Jul 2024 01:14:20 GMT  
		Size: 3.1 MB (3073093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991e70be4838afae3979e2bef4b2a7682dffac44793431e072ffbc9fc1686e5`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967a6fef2cedd5f47096963a74875b542f5e4f6667543712aa16505b281dcf7`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c472efc6552ca3c22ddd3afc3423433498a05fa5b26d79a2c74d9c71a5db0515`  
		Last Modified: Fri, 30 Aug 2024 21:50:47 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227ac46a3f3d5c7590120d9f555b6439500ed7212cdfe872e2850b122dc0be1`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba069329678371ed2d3ebd6d6b31019c124d7b205dd0cbc451d0f894c48081d1`  
		Last Modified: Fri, 30 Aug 2024 21:50:49 GMT  
		Size: 15.3 MB (15303131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f1b71f79757d6cb7ae12dc0d78c803efa304cf2be041b5e150fa74c97255c4`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da1f4159b65619170a1816f8957041566fec819f4092f532a9be4fae0766e2`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590a47b24d3ac1c6d1e93d41854d378374a6915b7752990a9bee3fc8716f4c34`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 29.1 MB (29073898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a7d4062ccea4fdf5ed8de172dbc9d1db681bcd5b390a4ffcb54fead69672`  
		Last Modified: Sat, 31 Aug 2024 02:31:06 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4db4380a5272248743937293db7b38194008f88539f7ccc564b3bed1bb5cd79`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 721.5 KB (721550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33f3a44fc41a0c9992469ecc0edc41e0159aa2e08f4efeccea804932ef311bf`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59cafb62783296c3132fc857a1b60d14ea43a4e76db24f8c2a0479869f3ab7a`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:921737fcf2c92f3ac4695d0aec6828e890f5b4d08bc6c70f56734ede56722df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56971ec72cabda406f617c3cc24ea97360d6da6ecb71f0e23010e72cf8c6bea`

```dockerfile
```

-	Layers:
	-	`sha256:cb12e5d1ebeacc0fceb674070dd7df4773f10915897eaa1eddd7cbac71311b94`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 2.1 MB (2146400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29ff867be45a3aeb01278f3118a6085a72e3b87beca82f559c4fabffc5fe43b8`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 30.9 KB (30925 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:073bc4633c923664558abf6d5ce4a99823ef75e16e944a468157d06c8249eba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69691530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83be9553a3d2f49e410c5897f2840d74a7ef1ae2d11bd8cdd71e57b98c08b56`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f069fb86c015646c4497d6fa3beaf8bd3f9f04d8f77a1a865ff47fc9922c27e3`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 3.3 MB (3324720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298458c1fe168646ba7edf3e03804ff1a01f1fac6b41ef2a94ef5bf333311f2b`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71c5e072e5141e780c5bbd4c1e2a34f9248a4b4a0983717a6c98be7560b899`  
		Last Modified: Tue, 23 Jul 2024 02:00:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eb94c855017ccb6e05ed05ab6089ac13ef31b7c2c4f68ac1aa7871f5e50f05`  
		Last Modified: Fri, 30 Aug 2024 21:23:23 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7788e2267fee70d1ccfd7ae5b7bdc051ea44976ed82a8dcce577cc9b0c8d6a`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d38576090a615f5e4f5732ed6ca99ac0f1721a6ed93df8c2a86c7b7d9a2539`  
		Last Modified: Fri, 30 Aug 2024 21:23:24 GMT  
		Size: 17.9 MB (17857930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb7c168c56b49540c07601d6cab358cafc4340a5f0dae6ef942aff3d828fa14`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f44bd4d0b7f587d16c7c70ac77c4a0a8d22a607399c38b6eb5ae4d5cd7d78b3`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 19.5 KB (19488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee874a6d0bc05b34617460b975ed3786bc3fb8320c0a847a478a06d8137ad3c`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 31.2 MB (31163203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab4e408f7d446ed2ebe4e87b8fc9ac34818639a1d6bd84e5e45a06bc7106695`  
		Last Modified: Sat, 31 Aug 2024 01:35:35 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d91d0b55a63351d17e9911db6bab49045bfafbdbc273a9b5a4116e298bac065`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 732.3 KB (732293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c32acd3eed5b3fed93e298ab5e0d8eb7efbbcd9082c26f7f7b5ca4317492d`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393221758014c491651ea5645fa14ebdf497800c775367b1804a5a3b18940de9`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:172bf1f9970e2360b6ac165018d38e20af6ab9500201cb1c2f8b374863c26f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a38a0d4cb7acb3bfacf00beda2539bfb2bddb8fb127093a799705f6df488a7a`

```dockerfile
```

-	Layers:
	-	`sha256:092a394ccecc23f4bc6c3b8ea0b60fcaa33856edd5cafa5d82fd0a3ff13c71b0`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 2.1 MB (2146226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41716e1295545592da4d3986e093e9d1bb0d6f94f5555cd7493f59b05483e463`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 31.1 KB (31126 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:be003ca163e5d66dd6fffbab33a5196358ab539dac1a67186f85dcb030ced2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48972123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb4aaf6a0e38d8203228cce1a7adc1a0ab3ede909ca4257f235291d3dc2da87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17866811de1cdb9710f37a522dde62051d068230716118d22b6b987216e037ef`  
		Last Modified: Sat, 07 Sep 2024 01:49:46 GMT  
		Size: 3.3 MB (3331976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513ca5d3e6e64e8e064f1b178ad39b5d375a65559181a7f4964c9471461ba8f`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90338393c7a779c5576927d742c98b6841aa39aa84fe1b137708bd8f4d0ae68e`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20961f4e3b99e90c174a4f87f2af7f93ae78322283dde5d669a4c76c2c3cebd8`  
		Last Modified: Sat, 07 Sep 2024 01:51:38 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42171d227440b8721b3056f4e4f3a4916baf777d09c6f844c8f8056fbc70c42`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dabae8861b481fcfb1e16733b346f40d06038d6a5cd82cceb87bd8c3ee3ecd`  
		Last Modified: Sat, 07 Sep 2024 01:51:42 GMT  
		Size: 17.7 MB (17656052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d394881214b919e13be7206b61f0f6743c86558096cefb3ea4f89e68ad0c8d2`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357eacc586709ee7f5d5f8c1962caf6215d0ea35d2d9ed17c68628bfff98004d`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8161d69d4ddf88fb74644faf68168690961a520ba07507622283a5da34a1619`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 11.3 MB (11281307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6648f7668a226dbb6c5c5d25590e31fbc3dddfef6b0906403fe9954bc65d658a`  
		Last Modified: Sat, 07 Sep 2024 02:57:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f980798686f082e1f7a21c78cc64ad7d57e85520f940bbecb97454bbfda490`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 707.0 KB (706967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0973440a5cb6fedc1a58ba74cd8270d1b173a9790fefa3a888df4b068ceac95`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc20d4a5058e00ce4cdcd9cfd7681def3ad0321a72623550a21e47bab615d61`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:39a70225bfa305f3f430def00df9b342dcb1b09d7bbcf467c628c7662d551a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.6 KB (450570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5085a2080691fe10f388ede18409103c9e330ada47561002d53fa16b6a99eb8e`

```dockerfile
```

-	Layers:
	-	`sha256:7bd2556fecbd3f888503c02046cc258e0dbadb86e081e567abd36b2f8fb0ffa1`  
		Last Modified: Sat, 07 Sep 2024 02:57:19 GMT  
		Size: 419.8 KB (419761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfc10434af42839f969e97a5d1a948657084b8fa4785ce8016281dcf519b4d4`  
		Last Modified: Sat, 07 Sep 2024 02:57:19 GMT  
		Size: 30.8 KB (30809 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:d2b1fbd62be3473501275c1a09cb2d93b3890c5f04549801326473c169a3c663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70692695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e262fbb58dc2b46cb4dcc7c208063ef413e09f1447c845f1ef2a33c9b20d47`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3b3ac21bbea54c953ea1f2d18929d69c201c50acbb70a6157944a16d881644`  
		Last Modified: Mon, 22 Jul 2024 23:40:54 GMT  
		Size: 3.4 MB (3400973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab89bd2c65997355b0f8d6c170e8ada77fc5d87ae04f4e525032aad1d1c519`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9ea05d06440c67793ed8359925d4dcf5e15c76e0e78b5d20fad34b553a253f`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512248dd3ed75a17d321bc96ddef6ecae12695170f3a768584fe46b6fec8b581`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f97a91111a935f934126b9b5e843f52e61ce5a0d268da80ce88a7e9637e46b`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e963895597cd82f3e2562f1193ef440f635d77e3ce7d65a2d29a5f952d1ee09`  
		Last Modified: Fri, 30 Aug 2024 21:39:34 GMT  
		Size: 18.8 MB (18776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd6fc58c5780a4980b31da9f3258387aa34ad2ae9aa0edd08d9a5b90aaea95`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb9ba050d100c1c32d4f5b3c3975a0ebb302f1b9d8fb6c9b5c21dd9b7279d50`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b5ba9d088f76b4f58ad424d166ff3328d5c7af19e83e9bf897da73af9c27e5`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 31.7 MB (31678361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980ba58d45390240ed5b943d865d41bc6ceaa59661e4c900661678594a767b3f`  
		Last Modified: Sat, 31 Aug 2024 02:19:13 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8810c1afb240b6bda7c0a32e7c5e6c71e6eb98ac5b6bd055ae704b4ef486a5`  
		Last Modified: Sat, 31 Aug 2024 02:20:14 GMT  
		Size: 738.5 KB (738495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4769b5a39f750d4627aaa2cf84236ef17a394a3cdbbf754e55af53275aa2f011`  
		Last Modified: Sat, 31 Aug 2024 02:20:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e242bd4593e9a5e885fa383bcd62e1e04535d43a93ebb97f96a6f05f7942d36`  
		Last Modified: Sat, 31 Aug 2024 02:20:14 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:946ae00a68c967b3f2c39a60a091f7630adcb95a1494cb899407fc4f1759eae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a7f2921f6b6a12c6931450e7bd0324cff121181a568e0fa61eba76c4df6a52`

```dockerfile
```

-	Layers:
	-	`sha256:00b2e417955ef9a8107fc2f978390276914e10db4fd258bca3e5affbb230bd45`  
		Last Modified: Sat, 31 Aug 2024 02:20:13 GMT  
		Size: 2.1 MB (2144636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:308f310e617cf7a4d25e55d73a28c90f9355c2f52dcf099bb9e814ce8acc65aa`  
		Last Modified: Sat, 31 Aug 2024 02:20:13 GMT  
		Size: 30.9 KB (30873 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:5cf0c06b7bdccaf9fd8573b7be89638d511debd49f9eef18168052fe41558bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68550619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f9110b5667db2b35be2234440177d181e746b7e4152f24139006ae9fc9f2c1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2d0e03d7a4d4766a64c04a50abfb02e217be153dd68888273b46568c4cac04`  
		Last Modified: Tue, 23 Jul 2024 12:29:02 GMT  
		Size: 3.4 MB (3397181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56268c2d820d6bf5bbf0e86c5bc55e50edc209a552c0844c6a9f787a880a2c6`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d3b9188b0e4a61167b2493ce280347bad9dfe72e9ecf4c18c5572f2cb6719`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d23ac9bf2deff71588cfd4b3f47c1364b66f45e05cb5d2518adb6a0396df50`  
		Last Modified: Sat, 31 Aug 2024 02:36:17 GMT  
		Size: 12.5 MB (12502106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869116b457f2e31f8fdb3c69a1bab7e4c51f76c00076389e0239f62c730528cf`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b247cb48214eaf57917fe6fa9b468fc196954c87b0933090b00ffbacd4cb7bd`  
		Last Modified: Sat, 31 Aug 2024 02:36:29 GMT  
		Size: 17.4 MB (17440090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f94c80d7718bd1bbc656205b6b9a90ee074a66d9466f41da567a907abd70f17`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a299e457c645ef0ea5f4f77590cbf1f9bbb149ab3b6d35be1e03c232e21b4298`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb74b37352199c3a76042764443f478982d69b68687aaf3b025bbe890eb8ac3f`  
		Last Modified: Sat, 31 Aug 2024 02:59:25 GMT  
		Size: 31.1 MB (31085763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5e8f63a80e285c25bb4838990371cbc88754639c0329cd9959283425dcc5eb`  
		Last Modified: Sat, 31 Aug 2024 02:59:22 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624a5f8850d83462423adce18ed2fa9a90291d0c8ddea31cd01858a2196c40eb`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 730.4 KB (730428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707d53407b40544b3d5a796be51fba6cf6410787e3eb907704d782c7928c19a4`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c5632aea6ba298a8fcea359761cfe78b9288cca4de8ae8ff43a8ffe5d35a3e`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:b8249e3c9fe77c8f9ea1b1a763bfaa0578bde5fb913e8dcb0fdd5e1b083e4101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacc3c814863c674ee4abf5ab1c30a9f690e25f82cd504f593ccead968f86833`

```dockerfile
```

-	Layers:
	-	`sha256:17accd5881c67816b847bf6c51f048491d9bc4defb841e2019a2897772b84a7e`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 2.1 MB (2144252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6f55bd37e6f86308569feac16976b1ed8b71784c9a74e2fffda6c84eadbc30`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 30.9 KB (30873 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:2d6d4c38ef985a287f760f25418ca505dfcc772dc74e4d37259a0593ffb5dd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70268665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee818012c01b69e8a3e5cad40e393a06889635e77692ebf9a6b93559867dc30`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bee85c5a5fc33ed0d0f61a077ed76c922b87c42c5cb3a4dbba408dd62a64def`  
		Last Modified: Tue, 23 Jul 2024 00:56:03 GMT  
		Size: 3.5 MB (3467756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1505ad7d669e91b715e2a1bc7ec0c52dd53433332ad45653571cbe2c3643d5`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d87c5417e12df9b44287d4f554dd37d0b5b446d100409e5c49a17ac509a5b2`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2c4b161c20f3e37aa088308da3bb1a01ec5125d77c20033c4794149cec443`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 12.5 MB (12502092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c122a67a16e90a3dfd6817a2f8845d6e6a1bc5b93a02733eed109b49ac9ac44e`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b9a37a60aa5eac97b05abfe815776138ce85dc5ba1906d5c9515c50c45b044`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 18.0 MB (17977689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c966b6ee628194de003583de4dd26ad320f0da92fbe22a571ce2a42dff75c605`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32192d5d915f2f8aabf39455fe449c2d46c8d50ae7e98d0de6c301ac1d15f45a`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7f663cd19fdb2482f23a049a2e83117b526da0ad73131e73fcfe4dc5e53635`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 31.6 MB (31612727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c1e4c810b0e1cb879cad0bec7f75826c9040aceeb755690532fc1181d9fb1`  
		Last Modified: Sat, 31 Aug 2024 01:54:05 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab7a86eaa546c024f5e9ddee632893656826057a1957952e8365c6b63e1d3c3`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 1.2 MB (1222989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2202ce0f4d64908acbb70be0eacc070096a74d265d966c71540ca6d7d708a242`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36ad3eb3c6d4f9552e034bb8b38e3abdaa2d247e50a71bebdd8bd89b066001b`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:91ed90c36f5bdb9f294ebbcfefa227c7c1efd671c51833e9ed7b007ddfdbef11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2174878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd01b56af78a62537b4aa71443e497fff365d8e907830c62ddbc99923d67a726`

```dockerfile
```

-	Layers:
	-	`sha256:dc7949c249539fe44554b71122c88c53dc66d1577afbbdd2e875847af4cf11c6`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 2.1 MB (2144038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a07a08cae27fa931c5c030f5204074b4fa957e809e695daac82f2c28083eba2`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 30.8 KB (30840 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:0f1e587f773ca5e7595477b84613de9a54d273c4acb059b33d657c2ee0214545
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
$ docker pull composer@sha256:7854521ce3fd2f7018636256bbd5f679989e11d82e5cb07058877e7d3cfcbdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68024536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a81db78c15dfdce65ef829acee8c47c9d6ec3e1ebed3baf688b2407fec3c9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15916673af8229814dcc44164d4616a6141bc5b586ae9362e741d64c6e4c91`  
		Last Modified: Sat, 07 Sep 2024 02:15:12 GMT  
		Size: 3.3 MB (3282678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb3258c4c6a46b7e182fa372bfe03ff37fd0fdf7f6894ca97b564fc382d7d4`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e436918c34ed4c536bdbaeace5213a8aaeb796ec65951fe681a10758ae2677`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6c87b6d10c2d5a9226b306e7fc3370cab80f9f41fe049706de7a51f8e1cf5a`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 12.5 MB (12502103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90d2c6f0ff71e78e4e311ebe4b83b2abbe5fdda23eaa28c5711e68b23c578da`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5cf8a88be3fd539ff5a60321e916df9fa78268109a78972d9411217023bf61`  
		Last Modified: Sat, 07 Sep 2024 02:16:52 GMT  
		Size: 17.2 MB (17212749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eea6dbc4cb9e274ad2228dfea58ecabec99b9336c8d528206ce4c41f6724ad`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f889a53b48220a2103d38ac31ed15adb68d8e5de71c03c475792439675576304`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb4916ca53279f53edcf4b1c977dc7e5486001fedd925f6f199dedd6ae2676f`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 30.6 MB (30647241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecd4819a1382c724645ef5ff5d4bd4d1965de9778a21ae7420bbdd5c3ae74fe`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a740ee85731801e28fc6e072e0d7bb053ae59e466ca49d36c96c1dd7effebd1`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 731.4 KB (731387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0973440a5cb6fedc1a58ba74cd8270d1b173a9790fefa3a888df4b068ceac95`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db0479371de30561eeeb00b17d7b75c81ac293dcf11c4556cb6a71bc59ac403`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:028263803ca2ed519100a3b2bdf013e15f3aea5168e06e28b29e6ea2d3f9d9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ea06e5499dc5df530faab4964eeb1b8b7b8034f78c96d6cb0f3f787b3f3fa0`

```dockerfile
```

-	Layers:
	-	`sha256:85becb9c92c63dffe4fd4e8196f79847b3607a47759bd80a8bc308d536c36658`  
		Last Modified: Sat, 07 Sep 2024 02:57:23 GMT  
		Size: 2.1 MB (2146087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c226f930338ccc811566d219d9faf7762a79c3c513fd7fe8f4767d94c648efa`  
		Last Modified: Sat, 07 Sep 2024 02:57:23 GMT  
		Size: 30.8 KB (30837 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:b6d5c099fa88cc921d8c7242bba125d7fbf0da0c32fcfad59eabf114d1f56e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65696796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77813782d8700088cb00c975415e0bd2ddd265f87e37140781ba41d87c964c6c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b041a1a670328abed5fe2b73e068aba477e969ddbfe65c606c8054a4c36067b2`  
		Last Modified: Tue, 23 Jul 2024 01:00:35 GMT  
		Size: 3.3 MB (3263638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51daa6109cd19af541c6fc2600ad5a2f2382e50d3938e2b51f30d24df583fee`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b57c8706e4f06f42a10294d5c9eef985613e48298dedb390c6e6816b60a8f78`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b27cb594dc713e8223f5363b7505f762ad934cbf1c4f47ed7885c05db8e13`  
		Last Modified: Fri, 30 Aug 2024 20:20:12 GMT  
		Size: 12.5 MB (12502099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22237d0261563edb9ca222f6a36c5e175cf1d62c16f38e41755982d955f0e39c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ea243fc20547ec3f93ecbe653822d8a49a7c9c61fd5b7ad229cf6ee331209`  
		Last Modified: Fri, 30 Aug 2024 20:20:15 GMT  
		Size: 16.4 MB (16360114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a08c99e5b1cb1537070b37b1f8f3c78a107be7dd6efdd3a197aa7867d3d7a5c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68481b9e1f3b14557aa8d598c31b8ec7b735f77a5aeac9431ef7b69560d46a92`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c939352561246c630164d6835a0997969adc47f5e678a95dc31e21f57e94926d`  
		Last Modified: Fri, 30 Aug 2024 21:19:20 GMT  
		Size: 29.5 MB (29450758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f957f60156f9b6e900c9f3e132d2e377afa2f2d79dd2350288d3c3cf994fc2`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec8fc3636cf8ae1505b2708291b352bb5c4fee94abe1cd819c8e2c53e6a9049`  
		Last Modified: Fri, 30 Aug 2024 21:20:02 GMT  
		Size: 730.6 KB (730626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5e376500c1dbf9e6b542bbd48cd51904faf1049e0278e1c2b18582fa895d55`  
		Last Modified: Fri, 30 Aug 2024 21:20:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69655ab9a4e94d9f6e302be56113fb79772c50b4c1630c34fec4940208712f1d`  
		Last Modified: Fri, 30 Aug 2024 21:20:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:3b80e0e7c88f074c2dc3fac1c5bf0ca63621267dd0c4d4c6ced4c03ad081f650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eba2ef3743ea56174ec791b48c8a2ce9972013ffd59c6286bd3fbc4247014a2`

```dockerfile
```

-	Layers:
	-	`sha256:149df9329ac2ea8c63c732c77999b219899fa2887f8864d08a94c8bd9471abaa`  
		Last Modified: Fri, 30 Aug 2024 21:20:01 GMT  
		Size: 30.7 KB (30670 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:14ad6f124ececd98cfecf19cc0913ddd2d82d2ca6365a21ce688b9dace31463a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63793116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99550fa2d8788346f4167dd3b2b259e8c63df4b79aa2d98ea8e2c6c7c4af9ed7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57db3d4836535044109c42cf341df21ab1def6a06fecbaf98ffac833b47f15b`  
		Last Modified: Tue, 23 Jul 2024 01:14:20 GMT  
		Size: 3.1 MB (3073093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991e70be4838afae3979e2bef4b2a7682dffac44793431e072ffbc9fc1686e5`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967a6fef2cedd5f47096963a74875b542f5e4f6667543712aa16505b281dcf7`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c472efc6552ca3c22ddd3afc3423433498a05fa5b26d79a2c74d9c71a5db0515`  
		Last Modified: Fri, 30 Aug 2024 21:50:47 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227ac46a3f3d5c7590120d9f555b6439500ed7212cdfe872e2850b122dc0be1`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba069329678371ed2d3ebd6d6b31019c124d7b205dd0cbc451d0f894c48081d1`  
		Last Modified: Fri, 30 Aug 2024 21:50:49 GMT  
		Size: 15.3 MB (15303131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f1b71f79757d6cb7ae12dc0d78c803efa304cf2be041b5e150fa74c97255c4`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da1f4159b65619170a1816f8957041566fec819f4092f532a9be4fae0766e2`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590a47b24d3ac1c6d1e93d41854d378374a6915b7752990a9bee3fc8716f4c34`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 29.1 MB (29073898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a7d4062ccea4fdf5ed8de172dbc9d1db681bcd5b390a4ffcb54fead69672`  
		Last Modified: Sat, 31 Aug 2024 02:31:06 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4db4380a5272248743937293db7b38194008f88539f7ccc564b3bed1bb5cd79`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 721.5 KB (721550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33f3a44fc41a0c9992469ecc0edc41e0159aa2e08f4efeccea804932ef311bf`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59cafb62783296c3132fc857a1b60d14ea43a4e76db24f8c2a0479869f3ab7a`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:921737fcf2c92f3ac4695d0aec6828e890f5b4d08bc6c70f56734ede56722df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56971ec72cabda406f617c3cc24ea97360d6da6ecb71f0e23010e72cf8c6bea`

```dockerfile
```

-	Layers:
	-	`sha256:cb12e5d1ebeacc0fceb674070dd7df4773f10915897eaa1eddd7cbac71311b94`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 2.1 MB (2146400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29ff867be45a3aeb01278f3118a6085a72e3b87beca82f559c4fabffc5fe43b8`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 30.9 KB (30925 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:073bc4633c923664558abf6d5ce4a99823ef75e16e944a468157d06c8249eba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69691530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83be9553a3d2f49e410c5897f2840d74a7ef1ae2d11bd8cdd71e57b98c08b56`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f069fb86c015646c4497d6fa3beaf8bd3f9f04d8f77a1a865ff47fc9922c27e3`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 3.3 MB (3324720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298458c1fe168646ba7edf3e03804ff1a01f1fac6b41ef2a94ef5bf333311f2b`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71c5e072e5141e780c5bbd4c1e2a34f9248a4b4a0983717a6c98be7560b899`  
		Last Modified: Tue, 23 Jul 2024 02:00:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eb94c855017ccb6e05ed05ab6089ac13ef31b7c2c4f68ac1aa7871f5e50f05`  
		Last Modified: Fri, 30 Aug 2024 21:23:23 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7788e2267fee70d1ccfd7ae5b7bdc051ea44976ed82a8dcce577cc9b0c8d6a`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d38576090a615f5e4f5732ed6ca99ac0f1721a6ed93df8c2a86c7b7d9a2539`  
		Last Modified: Fri, 30 Aug 2024 21:23:24 GMT  
		Size: 17.9 MB (17857930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb7c168c56b49540c07601d6cab358cafc4340a5f0dae6ef942aff3d828fa14`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f44bd4d0b7f587d16c7c70ac77c4a0a8d22a607399c38b6eb5ae4d5cd7d78b3`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 19.5 KB (19488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee874a6d0bc05b34617460b975ed3786bc3fb8320c0a847a478a06d8137ad3c`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 31.2 MB (31163203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab4e408f7d446ed2ebe4e87b8fc9ac34818639a1d6bd84e5e45a06bc7106695`  
		Last Modified: Sat, 31 Aug 2024 01:35:35 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d91d0b55a63351d17e9911db6bab49045bfafbdbc273a9b5a4116e298bac065`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 732.3 KB (732293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c32acd3eed5b3fed93e298ab5e0d8eb7efbbcd9082c26f7f7b5ca4317492d`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393221758014c491651ea5645fa14ebdf497800c775367b1804a5a3b18940de9`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:172bf1f9970e2360b6ac165018d38e20af6ab9500201cb1c2f8b374863c26f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a38a0d4cb7acb3bfacf00beda2539bfb2bddb8fb127093a799705f6df488a7a`

```dockerfile
```

-	Layers:
	-	`sha256:092a394ccecc23f4bc6c3b8ea0b60fcaa33856edd5cafa5d82fd0a3ff13c71b0`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 2.1 MB (2146226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41716e1295545592da4d3986e093e9d1bb0d6f94f5555cd7493f59b05483e463`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 31.1 KB (31126 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:be003ca163e5d66dd6fffbab33a5196358ab539dac1a67186f85dcb030ced2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48972123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb4aaf6a0e38d8203228cce1a7adc1a0ab3ede909ca4257f235291d3dc2da87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17866811de1cdb9710f37a522dde62051d068230716118d22b6b987216e037ef`  
		Last Modified: Sat, 07 Sep 2024 01:49:46 GMT  
		Size: 3.3 MB (3331976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513ca5d3e6e64e8e064f1b178ad39b5d375a65559181a7f4964c9471461ba8f`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90338393c7a779c5576927d742c98b6841aa39aa84fe1b137708bd8f4d0ae68e`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20961f4e3b99e90c174a4f87f2af7f93ae78322283dde5d669a4c76c2c3cebd8`  
		Last Modified: Sat, 07 Sep 2024 01:51:38 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42171d227440b8721b3056f4e4f3a4916baf777d09c6f844c8f8056fbc70c42`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dabae8861b481fcfb1e16733b346f40d06038d6a5cd82cceb87bd8c3ee3ecd`  
		Last Modified: Sat, 07 Sep 2024 01:51:42 GMT  
		Size: 17.7 MB (17656052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d394881214b919e13be7206b61f0f6743c86558096cefb3ea4f89e68ad0c8d2`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357eacc586709ee7f5d5f8c1962caf6215d0ea35d2d9ed17c68628bfff98004d`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8161d69d4ddf88fb74644faf68168690961a520ba07507622283a5da34a1619`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 11.3 MB (11281307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6648f7668a226dbb6c5c5d25590e31fbc3dddfef6b0906403fe9954bc65d658a`  
		Last Modified: Sat, 07 Sep 2024 02:57:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f980798686f082e1f7a21c78cc64ad7d57e85520f940bbecb97454bbfda490`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 707.0 KB (706967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0973440a5cb6fedc1a58ba74cd8270d1b173a9790fefa3a888df4b068ceac95`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc20d4a5058e00ce4cdcd9cfd7681def3ad0321a72623550a21e47bab615d61`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:39a70225bfa305f3f430def00df9b342dcb1b09d7bbcf467c628c7662d551a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.6 KB (450570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5085a2080691fe10f388ede18409103c9e330ada47561002d53fa16b6a99eb8e`

```dockerfile
```

-	Layers:
	-	`sha256:7bd2556fecbd3f888503c02046cc258e0dbadb86e081e567abd36b2f8fb0ffa1`  
		Last Modified: Sat, 07 Sep 2024 02:57:19 GMT  
		Size: 419.8 KB (419761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfc10434af42839f969e97a5d1a948657084b8fa4785ce8016281dcf519b4d4`  
		Last Modified: Sat, 07 Sep 2024 02:57:19 GMT  
		Size: 30.8 KB (30809 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:d2b1fbd62be3473501275c1a09cb2d93b3890c5f04549801326473c169a3c663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70692695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e262fbb58dc2b46cb4dcc7c208063ef413e09f1447c845f1ef2a33c9b20d47`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3b3ac21bbea54c953ea1f2d18929d69c201c50acbb70a6157944a16d881644`  
		Last Modified: Mon, 22 Jul 2024 23:40:54 GMT  
		Size: 3.4 MB (3400973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab89bd2c65997355b0f8d6c170e8ada77fc5d87ae04f4e525032aad1d1c519`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9ea05d06440c67793ed8359925d4dcf5e15c76e0e78b5d20fad34b553a253f`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512248dd3ed75a17d321bc96ddef6ecae12695170f3a768584fe46b6fec8b581`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f97a91111a935f934126b9b5e843f52e61ce5a0d268da80ce88a7e9637e46b`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e963895597cd82f3e2562f1193ef440f635d77e3ce7d65a2d29a5f952d1ee09`  
		Last Modified: Fri, 30 Aug 2024 21:39:34 GMT  
		Size: 18.8 MB (18776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd6fc58c5780a4980b31da9f3258387aa34ad2ae9aa0edd08d9a5b90aaea95`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb9ba050d100c1c32d4f5b3c3975a0ebb302f1b9d8fb6c9b5c21dd9b7279d50`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b5ba9d088f76b4f58ad424d166ff3328d5c7af19e83e9bf897da73af9c27e5`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 31.7 MB (31678361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980ba58d45390240ed5b943d865d41bc6ceaa59661e4c900661678594a767b3f`  
		Last Modified: Sat, 31 Aug 2024 02:19:13 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8810c1afb240b6bda7c0a32e7c5e6c71e6eb98ac5b6bd055ae704b4ef486a5`  
		Last Modified: Sat, 31 Aug 2024 02:20:14 GMT  
		Size: 738.5 KB (738495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4769b5a39f750d4627aaa2cf84236ef17a394a3cdbbf754e55af53275aa2f011`  
		Last Modified: Sat, 31 Aug 2024 02:20:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e242bd4593e9a5e885fa383bcd62e1e04535d43a93ebb97f96a6f05f7942d36`  
		Last Modified: Sat, 31 Aug 2024 02:20:14 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:946ae00a68c967b3f2c39a60a091f7630adcb95a1494cb899407fc4f1759eae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a7f2921f6b6a12c6931450e7bd0324cff121181a568e0fa61eba76c4df6a52`

```dockerfile
```

-	Layers:
	-	`sha256:00b2e417955ef9a8107fc2f978390276914e10db4fd258bca3e5affbb230bd45`  
		Last Modified: Sat, 31 Aug 2024 02:20:13 GMT  
		Size: 2.1 MB (2144636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:308f310e617cf7a4d25e55d73a28c90f9355c2f52dcf099bb9e814ce8acc65aa`  
		Last Modified: Sat, 31 Aug 2024 02:20:13 GMT  
		Size: 30.9 KB (30873 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:5cf0c06b7bdccaf9fd8573b7be89638d511debd49f9eef18168052fe41558bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68550619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f9110b5667db2b35be2234440177d181e746b7e4152f24139006ae9fc9f2c1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2d0e03d7a4d4766a64c04a50abfb02e217be153dd68888273b46568c4cac04`  
		Last Modified: Tue, 23 Jul 2024 12:29:02 GMT  
		Size: 3.4 MB (3397181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56268c2d820d6bf5bbf0e86c5bc55e50edc209a552c0844c6a9f787a880a2c6`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d3b9188b0e4a61167b2493ce280347bad9dfe72e9ecf4c18c5572f2cb6719`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d23ac9bf2deff71588cfd4b3f47c1364b66f45e05cb5d2518adb6a0396df50`  
		Last Modified: Sat, 31 Aug 2024 02:36:17 GMT  
		Size: 12.5 MB (12502106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869116b457f2e31f8fdb3c69a1bab7e4c51f76c00076389e0239f62c730528cf`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b247cb48214eaf57917fe6fa9b468fc196954c87b0933090b00ffbacd4cb7bd`  
		Last Modified: Sat, 31 Aug 2024 02:36:29 GMT  
		Size: 17.4 MB (17440090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f94c80d7718bd1bbc656205b6b9a90ee074a66d9466f41da567a907abd70f17`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a299e457c645ef0ea5f4f77590cbf1f9bbb149ab3b6d35be1e03c232e21b4298`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb74b37352199c3a76042764443f478982d69b68687aaf3b025bbe890eb8ac3f`  
		Last Modified: Sat, 31 Aug 2024 02:59:25 GMT  
		Size: 31.1 MB (31085763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5e8f63a80e285c25bb4838990371cbc88754639c0329cd9959283425dcc5eb`  
		Last Modified: Sat, 31 Aug 2024 02:59:22 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624a5f8850d83462423adce18ed2fa9a90291d0c8ddea31cd01858a2196c40eb`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 730.4 KB (730428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707d53407b40544b3d5a796be51fba6cf6410787e3eb907704d782c7928c19a4`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c5632aea6ba298a8fcea359761cfe78b9288cca4de8ae8ff43a8ffe5d35a3e`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:b8249e3c9fe77c8f9ea1b1a763bfaa0578bde5fb913e8dcb0fdd5e1b083e4101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacc3c814863c674ee4abf5ab1c30a9f690e25f82cd504f593ccead968f86833`

```dockerfile
```

-	Layers:
	-	`sha256:17accd5881c67816b847bf6c51f048491d9bc4defb841e2019a2897772b84a7e`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 2.1 MB (2144252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6f55bd37e6f86308569feac16976b1ed8b71784c9a74e2fffda6c84eadbc30`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 30.9 KB (30873 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:2d6d4c38ef985a287f760f25418ca505dfcc772dc74e4d37259a0593ffb5dd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70268665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee818012c01b69e8a3e5cad40e393a06889635e77692ebf9a6b93559867dc30`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bee85c5a5fc33ed0d0f61a077ed76c922b87c42c5cb3a4dbba408dd62a64def`  
		Last Modified: Tue, 23 Jul 2024 00:56:03 GMT  
		Size: 3.5 MB (3467756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1505ad7d669e91b715e2a1bc7ec0c52dd53433332ad45653571cbe2c3643d5`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d87c5417e12df9b44287d4f554dd37d0b5b446d100409e5c49a17ac509a5b2`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2c4b161c20f3e37aa088308da3bb1a01ec5125d77c20033c4794149cec443`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 12.5 MB (12502092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c122a67a16e90a3dfd6817a2f8845d6e6a1bc5b93a02733eed109b49ac9ac44e`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b9a37a60aa5eac97b05abfe815776138ce85dc5ba1906d5c9515c50c45b044`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 18.0 MB (17977689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c966b6ee628194de003583de4dd26ad320f0da92fbe22a571ce2a42dff75c605`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32192d5d915f2f8aabf39455fe449c2d46c8d50ae7e98d0de6c301ac1d15f45a`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7f663cd19fdb2482f23a049a2e83117b526da0ad73131e73fcfe4dc5e53635`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 31.6 MB (31612727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c1e4c810b0e1cb879cad0bec7f75826c9040aceeb755690532fc1181d9fb1`  
		Last Modified: Sat, 31 Aug 2024 01:54:05 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab7a86eaa546c024f5e9ddee632893656826057a1957952e8365c6b63e1d3c3`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 1.2 MB (1222989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2202ce0f4d64908acbb70be0eacc070096a74d265d966c71540ca6d7d708a242`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36ad3eb3c6d4f9552e034bb8b38e3abdaa2d247e50a71bebdd8bd89b066001b`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:91ed90c36f5bdb9f294ebbcfefa227c7c1efd671c51833e9ed7b007ddfdbef11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2174878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd01b56af78a62537b4aa71443e497fff365d8e907830c62ddbc99923d67a726`

```dockerfile
```

-	Layers:
	-	`sha256:dc7949c249539fe44554b71122c88c53dc66d1577afbbdd2e875847af4cf11c6`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 2.1 MB (2144038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a07a08cae27fa931c5c030f5204074b4fa957e809e695daac82f2c28083eba2`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 30.8 KB (30840 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:0f1e587f773ca5e7595477b84613de9a54d273c4acb059b33d657c2ee0214545
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
$ docker pull composer@sha256:7854521ce3fd2f7018636256bbd5f679989e11d82e5cb07058877e7d3cfcbdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68024536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a81db78c15dfdce65ef829acee8c47c9d6ec3e1ebed3baf688b2407fec3c9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15916673af8229814dcc44164d4616a6141bc5b586ae9362e741d64c6e4c91`  
		Last Modified: Sat, 07 Sep 2024 02:15:12 GMT  
		Size: 3.3 MB (3282678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb3258c4c6a46b7e182fa372bfe03ff37fd0fdf7f6894ca97b564fc382d7d4`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e436918c34ed4c536bdbaeace5213a8aaeb796ec65951fe681a10758ae2677`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6c87b6d10c2d5a9226b306e7fc3370cab80f9f41fe049706de7a51f8e1cf5a`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 12.5 MB (12502103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90d2c6f0ff71e78e4e311ebe4b83b2abbe5fdda23eaa28c5711e68b23c578da`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5cf8a88be3fd539ff5a60321e916df9fa78268109a78972d9411217023bf61`  
		Last Modified: Sat, 07 Sep 2024 02:16:52 GMT  
		Size: 17.2 MB (17212749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eea6dbc4cb9e274ad2228dfea58ecabec99b9336c8d528206ce4c41f6724ad`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f889a53b48220a2103d38ac31ed15adb68d8e5de71c03c475792439675576304`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb4916ca53279f53edcf4b1c977dc7e5486001fedd925f6f199dedd6ae2676f`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 30.6 MB (30647241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecd4819a1382c724645ef5ff5d4bd4d1965de9778a21ae7420bbdd5c3ae74fe`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a740ee85731801e28fc6e072e0d7bb053ae59e466ca49d36c96c1dd7effebd1`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 731.4 KB (731387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0973440a5cb6fedc1a58ba74cd8270d1b173a9790fefa3a888df4b068ceac95`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db0479371de30561eeeb00b17d7b75c81ac293dcf11c4556cb6a71bc59ac403`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:028263803ca2ed519100a3b2bdf013e15f3aea5168e06e28b29e6ea2d3f9d9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ea06e5499dc5df530faab4964eeb1b8b7b8034f78c96d6cb0f3f787b3f3fa0`

```dockerfile
```

-	Layers:
	-	`sha256:85becb9c92c63dffe4fd4e8196f79847b3607a47759bd80a8bc308d536c36658`  
		Last Modified: Sat, 07 Sep 2024 02:57:23 GMT  
		Size: 2.1 MB (2146087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c226f930338ccc811566d219d9faf7762a79c3c513fd7fe8f4767d94c648efa`  
		Last Modified: Sat, 07 Sep 2024 02:57:23 GMT  
		Size: 30.8 KB (30837 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v6

```console
$ docker pull composer@sha256:b6d5c099fa88cc921d8c7242bba125d7fbf0da0c32fcfad59eabf114d1f56e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65696796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77813782d8700088cb00c975415e0bd2ddd265f87e37140781ba41d87c964c6c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b041a1a670328abed5fe2b73e068aba477e969ddbfe65c606c8054a4c36067b2`  
		Last Modified: Tue, 23 Jul 2024 01:00:35 GMT  
		Size: 3.3 MB (3263638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51daa6109cd19af541c6fc2600ad5a2f2382e50d3938e2b51f30d24df583fee`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b57c8706e4f06f42a10294d5c9eef985613e48298dedb390c6e6816b60a8f78`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b27cb594dc713e8223f5363b7505f762ad934cbf1c4f47ed7885c05db8e13`  
		Last Modified: Fri, 30 Aug 2024 20:20:12 GMT  
		Size: 12.5 MB (12502099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22237d0261563edb9ca222f6a36c5e175cf1d62c16f38e41755982d955f0e39c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ea243fc20547ec3f93ecbe653822d8a49a7c9c61fd5b7ad229cf6ee331209`  
		Last Modified: Fri, 30 Aug 2024 20:20:15 GMT  
		Size: 16.4 MB (16360114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a08c99e5b1cb1537070b37b1f8f3c78a107be7dd6efdd3a197aa7867d3d7a5c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68481b9e1f3b14557aa8d598c31b8ec7b735f77a5aeac9431ef7b69560d46a92`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c939352561246c630164d6835a0997969adc47f5e678a95dc31e21f57e94926d`  
		Last Modified: Fri, 30 Aug 2024 21:19:20 GMT  
		Size: 29.5 MB (29450758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f957f60156f9b6e900c9f3e132d2e377afa2f2d79dd2350288d3c3cf994fc2`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec8fc3636cf8ae1505b2708291b352bb5c4fee94abe1cd819c8e2c53e6a9049`  
		Last Modified: Fri, 30 Aug 2024 21:20:02 GMT  
		Size: 730.6 KB (730626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5e376500c1dbf9e6b542bbd48cd51904faf1049e0278e1c2b18582fa895d55`  
		Last Modified: Fri, 30 Aug 2024 21:20:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69655ab9a4e94d9f6e302be56113fb79772c50b4c1630c34fec4940208712f1d`  
		Last Modified: Fri, 30 Aug 2024 21:20:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:3b80e0e7c88f074c2dc3fac1c5bf0ca63621267dd0c4d4c6ced4c03ad081f650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eba2ef3743ea56174ec791b48c8a2ce9972013ffd59c6286bd3fbc4247014a2`

```dockerfile
```

-	Layers:
	-	`sha256:149df9329ac2ea8c63c732c77999b219899fa2887f8864d08a94c8bd9471abaa`  
		Last Modified: Fri, 30 Aug 2024 21:20:01 GMT  
		Size: 30.7 KB (30670 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v7

```console
$ docker pull composer@sha256:14ad6f124ececd98cfecf19cc0913ddd2d82d2ca6365a21ce688b9dace31463a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63793116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99550fa2d8788346f4167dd3b2b259e8c63df4b79aa2d98ea8e2c6c7c4af9ed7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57db3d4836535044109c42cf341df21ab1def6a06fecbaf98ffac833b47f15b`  
		Last Modified: Tue, 23 Jul 2024 01:14:20 GMT  
		Size: 3.1 MB (3073093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991e70be4838afae3979e2bef4b2a7682dffac44793431e072ffbc9fc1686e5`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967a6fef2cedd5f47096963a74875b542f5e4f6667543712aa16505b281dcf7`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c472efc6552ca3c22ddd3afc3423433498a05fa5b26d79a2c74d9c71a5db0515`  
		Last Modified: Fri, 30 Aug 2024 21:50:47 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227ac46a3f3d5c7590120d9f555b6439500ed7212cdfe872e2850b122dc0be1`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba069329678371ed2d3ebd6d6b31019c124d7b205dd0cbc451d0f894c48081d1`  
		Last Modified: Fri, 30 Aug 2024 21:50:49 GMT  
		Size: 15.3 MB (15303131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f1b71f79757d6cb7ae12dc0d78c803efa304cf2be041b5e150fa74c97255c4`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da1f4159b65619170a1816f8957041566fec819f4092f532a9be4fae0766e2`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590a47b24d3ac1c6d1e93d41854d378374a6915b7752990a9bee3fc8716f4c34`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 29.1 MB (29073898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a7d4062ccea4fdf5ed8de172dbc9d1db681bcd5b390a4ffcb54fead69672`  
		Last Modified: Sat, 31 Aug 2024 02:31:06 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4db4380a5272248743937293db7b38194008f88539f7ccc564b3bed1bb5cd79`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 721.5 KB (721550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33f3a44fc41a0c9992469ecc0edc41e0159aa2e08f4efeccea804932ef311bf`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59cafb62783296c3132fc857a1b60d14ea43a4e76db24f8c2a0479869f3ab7a`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:921737fcf2c92f3ac4695d0aec6828e890f5b4d08bc6c70f56734ede56722df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56971ec72cabda406f617c3cc24ea97360d6da6ecb71f0e23010e72cf8c6bea`

```dockerfile
```

-	Layers:
	-	`sha256:cb12e5d1ebeacc0fceb674070dd7df4773f10915897eaa1eddd7cbac71311b94`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 2.1 MB (2146400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29ff867be45a3aeb01278f3118a6085a72e3b87beca82f559c4fabffc5fe43b8`  
		Last Modified: Sat, 31 Aug 2024 02:31:51 GMT  
		Size: 30.9 KB (30925 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:073bc4633c923664558abf6d5ce4a99823ef75e16e944a468157d06c8249eba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69691530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83be9553a3d2f49e410c5897f2840d74a7ef1ae2d11bd8cdd71e57b98c08b56`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f069fb86c015646c4497d6fa3beaf8bd3f9f04d8f77a1a865ff47fc9922c27e3`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 3.3 MB (3324720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298458c1fe168646ba7edf3e03804ff1a01f1fac6b41ef2a94ef5bf333311f2b`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71c5e072e5141e780c5bbd4c1e2a34f9248a4b4a0983717a6c98be7560b899`  
		Last Modified: Tue, 23 Jul 2024 02:00:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eb94c855017ccb6e05ed05ab6089ac13ef31b7c2c4f68ac1aa7871f5e50f05`  
		Last Modified: Fri, 30 Aug 2024 21:23:23 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7788e2267fee70d1ccfd7ae5b7bdc051ea44976ed82a8dcce577cc9b0c8d6a`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d38576090a615f5e4f5732ed6ca99ac0f1721a6ed93df8c2a86c7b7d9a2539`  
		Last Modified: Fri, 30 Aug 2024 21:23:24 GMT  
		Size: 17.9 MB (17857930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb7c168c56b49540c07601d6cab358cafc4340a5f0dae6ef942aff3d828fa14`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f44bd4d0b7f587d16c7c70ac77c4a0a8d22a607399c38b6eb5ae4d5cd7d78b3`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 19.5 KB (19488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee874a6d0bc05b34617460b975ed3786bc3fb8320c0a847a478a06d8137ad3c`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 31.2 MB (31163203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab4e408f7d446ed2ebe4e87b8fc9ac34818639a1d6bd84e5e45a06bc7106695`  
		Last Modified: Sat, 31 Aug 2024 01:35:35 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d91d0b55a63351d17e9911db6bab49045bfafbdbc273a9b5a4116e298bac065`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 732.3 KB (732293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c32acd3eed5b3fed93e298ab5e0d8eb7efbbcd9082c26f7f7b5ca4317492d`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393221758014c491651ea5645fa14ebdf497800c775367b1804a5a3b18940de9`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:172bf1f9970e2360b6ac165018d38e20af6ab9500201cb1c2f8b374863c26f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a38a0d4cb7acb3bfacf00beda2539bfb2bddb8fb127093a799705f6df488a7a`

```dockerfile
```

-	Layers:
	-	`sha256:092a394ccecc23f4bc6c3b8ea0b60fcaa33856edd5cafa5d82fd0a3ff13c71b0`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 2.1 MB (2146226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41716e1295545592da4d3986e093e9d1bb0d6f94f5555cd7493f59b05483e463`  
		Last Modified: Sat, 31 Aug 2024 01:36:16 GMT  
		Size: 31.1 KB (31126 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; 386

```console
$ docker pull composer@sha256:be003ca163e5d66dd6fffbab33a5196358ab539dac1a67186f85dcb030ced2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48972123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb4aaf6a0e38d8203228cce1a7adc1a0ab3ede909ca4257f235291d3dc2da87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17866811de1cdb9710f37a522dde62051d068230716118d22b6b987216e037ef`  
		Last Modified: Sat, 07 Sep 2024 01:49:46 GMT  
		Size: 3.3 MB (3331976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513ca5d3e6e64e8e064f1b178ad39b5d375a65559181a7f4964c9471461ba8f`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90338393c7a779c5576927d742c98b6841aa39aa84fe1b137708bd8f4d0ae68e`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20961f4e3b99e90c174a4f87f2af7f93ae78322283dde5d669a4c76c2c3cebd8`  
		Last Modified: Sat, 07 Sep 2024 01:51:38 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42171d227440b8721b3056f4e4f3a4916baf777d09c6f844c8f8056fbc70c42`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dabae8861b481fcfb1e16733b346f40d06038d6a5cd82cceb87bd8c3ee3ecd`  
		Last Modified: Sat, 07 Sep 2024 01:51:42 GMT  
		Size: 17.7 MB (17656052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d394881214b919e13be7206b61f0f6743c86558096cefb3ea4f89e68ad0c8d2`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357eacc586709ee7f5d5f8c1962caf6215d0ea35d2d9ed17c68628bfff98004d`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8161d69d4ddf88fb74644faf68168690961a520ba07507622283a5da34a1619`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 11.3 MB (11281307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6648f7668a226dbb6c5c5d25590e31fbc3dddfef6b0906403fe9954bc65d658a`  
		Last Modified: Sat, 07 Sep 2024 02:57:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f980798686f082e1f7a21c78cc64ad7d57e85520f940bbecb97454bbfda490`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 707.0 KB (706967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0973440a5cb6fedc1a58ba74cd8270d1b173a9790fefa3a888df4b068ceac95`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc20d4a5058e00ce4cdcd9cfd7681def3ad0321a72623550a21e47bab615d61`  
		Last Modified: Sat, 07 Sep 2024 02:57:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:39a70225bfa305f3f430def00df9b342dcb1b09d7bbcf467c628c7662d551a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.6 KB (450570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5085a2080691fe10f388ede18409103c9e330ada47561002d53fa16b6a99eb8e`

```dockerfile
```

-	Layers:
	-	`sha256:7bd2556fecbd3f888503c02046cc258e0dbadb86e081e567abd36b2f8fb0ffa1`  
		Last Modified: Sat, 07 Sep 2024 02:57:19 GMT  
		Size: 419.8 KB (419761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfc10434af42839f969e97a5d1a948657084b8fa4785ce8016281dcf519b4d4`  
		Last Modified: Sat, 07 Sep 2024 02:57:19 GMT  
		Size: 30.8 KB (30809 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; ppc64le

```console
$ docker pull composer@sha256:d2b1fbd62be3473501275c1a09cb2d93b3890c5f04549801326473c169a3c663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70692695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e262fbb58dc2b46cb4dcc7c208063ef413e09f1447c845f1ef2a33c9b20d47`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3b3ac21bbea54c953ea1f2d18929d69c201c50acbb70a6157944a16d881644`  
		Last Modified: Mon, 22 Jul 2024 23:40:54 GMT  
		Size: 3.4 MB (3400973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab89bd2c65997355b0f8d6c170e8ada77fc5d87ae04f4e525032aad1d1c519`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9ea05d06440c67793ed8359925d4dcf5e15c76e0e78b5d20fad34b553a253f`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512248dd3ed75a17d321bc96ddef6ecae12695170f3a768584fe46b6fec8b581`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f97a91111a935f934126b9b5e843f52e61ce5a0d268da80ce88a7e9637e46b`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e963895597cd82f3e2562f1193ef440f635d77e3ce7d65a2d29a5f952d1ee09`  
		Last Modified: Fri, 30 Aug 2024 21:39:34 GMT  
		Size: 18.8 MB (18776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd6fc58c5780a4980b31da9f3258387aa34ad2ae9aa0edd08d9a5b90aaea95`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb9ba050d100c1c32d4f5b3c3975a0ebb302f1b9d8fb6c9b5c21dd9b7279d50`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b5ba9d088f76b4f58ad424d166ff3328d5c7af19e83e9bf897da73af9c27e5`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 31.7 MB (31678361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980ba58d45390240ed5b943d865d41bc6ceaa59661e4c900661678594a767b3f`  
		Last Modified: Sat, 31 Aug 2024 02:19:13 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8810c1afb240b6bda7c0a32e7c5e6c71e6eb98ac5b6bd055ae704b4ef486a5`  
		Last Modified: Sat, 31 Aug 2024 02:20:14 GMT  
		Size: 738.5 KB (738495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4769b5a39f750d4627aaa2cf84236ef17a394a3cdbbf754e55af53275aa2f011`  
		Last Modified: Sat, 31 Aug 2024 02:20:22 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e242bd4593e9a5e885fa383bcd62e1e04535d43a93ebb97f96a6f05f7942d36`  
		Last Modified: Sat, 31 Aug 2024 02:20:14 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:946ae00a68c967b3f2c39a60a091f7630adcb95a1494cb899407fc4f1759eae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a7f2921f6b6a12c6931450e7bd0324cff121181a568e0fa61eba76c4df6a52`

```dockerfile
```

-	Layers:
	-	`sha256:00b2e417955ef9a8107fc2f978390276914e10db4fd258bca3e5affbb230bd45`  
		Last Modified: Sat, 31 Aug 2024 02:20:13 GMT  
		Size: 2.1 MB (2144636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:308f310e617cf7a4d25e55d73a28c90f9355c2f52dcf099bb9e814ce8acc65aa`  
		Last Modified: Sat, 31 Aug 2024 02:20:13 GMT  
		Size: 30.9 KB (30873 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; riscv64

```console
$ docker pull composer@sha256:5cf0c06b7bdccaf9fd8573b7be89638d511debd49f9eef18168052fe41558bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68550619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f9110b5667db2b35be2234440177d181e746b7e4152f24139006ae9fc9f2c1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2d0e03d7a4d4766a64c04a50abfb02e217be153dd68888273b46568c4cac04`  
		Last Modified: Tue, 23 Jul 2024 12:29:02 GMT  
		Size: 3.4 MB (3397181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56268c2d820d6bf5bbf0e86c5bc55e50edc209a552c0844c6a9f787a880a2c6`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d3b9188b0e4a61167b2493ce280347bad9dfe72e9ecf4c18c5572f2cb6719`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d23ac9bf2deff71588cfd4b3f47c1364b66f45e05cb5d2518adb6a0396df50`  
		Last Modified: Sat, 31 Aug 2024 02:36:17 GMT  
		Size: 12.5 MB (12502106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869116b457f2e31f8fdb3c69a1bab7e4c51f76c00076389e0239f62c730528cf`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b247cb48214eaf57917fe6fa9b468fc196954c87b0933090b00ffbacd4cb7bd`  
		Last Modified: Sat, 31 Aug 2024 02:36:29 GMT  
		Size: 17.4 MB (17440090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f94c80d7718bd1bbc656205b6b9a90ee074a66d9466f41da567a907abd70f17`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a299e457c645ef0ea5f4f77590cbf1f9bbb149ab3b6d35be1e03c232e21b4298`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb74b37352199c3a76042764443f478982d69b68687aaf3b025bbe890eb8ac3f`  
		Last Modified: Sat, 31 Aug 2024 02:59:25 GMT  
		Size: 31.1 MB (31085763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5e8f63a80e285c25bb4838990371cbc88754639c0329cd9959283425dcc5eb`  
		Last Modified: Sat, 31 Aug 2024 02:59:22 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624a5f8850d83462423adce18ed2fa9a90291d0c8ddea31cd01858a2196c40eb`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 730.4 KB (730428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707d53407b40544b3d5a796be51fba6cf6410787e3eb907704d782c7928c19a4`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c5632aea6ba298a8fcea359761cfe78b9288cca4de8ae8ff43a8ffe5d35a3e`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:b8249e3c9fe77c8f9ea1b1a763bfaa0578bde5fb913e8dcb0fdd5e1b083e4101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacc3c814863c674ee4abf5ab1c30a9f690e25f82cd504f593ccead968f86833`

```dockerfile
```

-	Layers:
	-	`sha256:17accd5881c67816b847bf6c51f048491d9bc4defb841e2019a2897772b84a7e`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 2.1 MB (2144252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6f55bd37e6f86308569feac16976b1ed8b71784c9a74e2fffda6c84eadbc30`  
		Last Modified: Sat, 31 Aug 2024 06:02:26 GMT  
		Size: 30.9 KB (30873 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; s390x

```console
$ docker pull composer@sha256:2d6d4c38ef985a287f760f25418ca505dfcc772dc74e4d37259a0593ffb5dd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70268665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee818012c01b69e8a3e5cad40e393a06889635e77692ebf9a6b93559867dc30`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bee85c5a5fc33ed0d0f61a077ed76c922b87c42c5cb3a4dbba408dd62a64def`  
		Last Modified: Tue, 23 Jul 2024 00:56:03 GMT  
		Size: 3.5 MB (3467756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1505ad7d669e91b715e2a1bc7ec0c52dd53433332ad45653571cbe2c3643d5`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d87c5417e12df9b44287d4f554dd37d0b5b446d100409e5c49a17ac509a5b2`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2c4b161c20f3e37aa088308da3bb1a01ec5125d77c20033c4794149cec443`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 12.5 MB (12502092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c122a67a16e90a3dfd6817a2f8845d6e6a1bc5b93a02733eed109b49ac9ac44e`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b9a37a60aa5eac97b05abfe815776138ce85dc5ba1906d5c9515c50c45b044`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 18.0 MB (17977689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c966b6ee628194de003583de4dd26ad320f0da92fbe22a571ce2a42dff75c605`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32192d5d915f2f8aabf39455fe449c2d46c8d50ae7e98d0de6c301ac1d15f45a`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7f663cd19fdb2482f23a049a2e83117b526da0ad73131e73fcfe4dc5e53635`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 31.6 MB (31612727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c1e4c810b0e1cb879cad0bec7f75826c9040aceeb755690532fc1181d9fb1`  
		Last Modified: Sat, 31 Aug 2024 01:54:05 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab7a86eaa546c024f5e9ddee632893656826057a1957952e8365c6b63e1d3c3`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 1.2 MB (1222989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2202ce0f4d64908acbb70be0eacc070096a74d265d966c71540ca6d7d708a242`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36ad3eb3c6d4f9552e034bb8b38e3abdaa2d247e50a71bebdd8bd89b066001b`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:91ed90c36f5bdb9f294ebbcfefa227c7c1efd671c51833e9ed7b007ddfdbef11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2174878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd01b56af78a62537b4aa71443e497fff365d8e907830c62ddbc99923d67a726`

```dockerfile
```

-	Layers:
	-	`sha256:dc7949c249539fe44554b71122c88c53dc66d1577afbbdd2e875847af4cf11c6`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 2.1 MB (2144038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a07a08cae27fa931c5c030f5204074b4fa957e809e695daac82f2c28083eba2`  
		Last Modified: Sat, 31 Aug 2024 01:54:50 GMT  
		Size: 30.8 KB (30840 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:a710f61aab1ce8a99c19a4024cf965d3ec937dcc2e153937cabe001d9b4b5db4
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
$ docker pull composer@sha256:76a2677544ab9e928c98186b37d4327efd3e74a5b6b0e6cf1c9399624f5d2c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68243059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d70afc6bb36eacbb3d15b53b6aa3afaae51a2eaff9f01721f55c5d9b57921d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Sep 2024 08:44:06 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Sep 2024 08:44:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Sep 2024 08:44:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_VERSION=8.3.11
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 05 Sep 2024 08:44:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Sep 2024 08:44:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15916673af8229814dcc44164d4616a6141bc5b586ae9362e741d64c6e4c91`  
		Last Modified: Sat, 07 Sep 2024 02:15:12 GMT  
		Size: 3.3 MB (3282678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb3258c4c6a46b7e182fa372bfe03ff37fd0fdf7f6894ca97b564fc382d7d4`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e436918c34ed4c536bdbaeace5213a8aaeb796ec65951fe681a10758ae2677`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6c87b6d10c2d5a9226b306e7fc3370cab80f9f41fe049706de7a51f8e1cf5a`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 12.5 MB (12502103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90d2c6f0ff71e78e4e311ebe4b83b2abbe5fdda23eaa28c5711e68b23c578da`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5cf8a88be3fd539ff5a60321e916df9fa78268109a78972d9411217023bf61`  
		Last Modified: Sat, 07 Sep 2024 02:16:52 GMT  
		Size: 17.2 MB (17212749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eea6dbc4cb9e274ad2228dfea58ecabec99b9336c8d528206ce4c41f6724ad`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f889a53b48220a2103d38ac31ed15adb68d8e5de71c03c475792439675576304`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fa61b2c2dec3cde7d7b254fe7cc695f7e1fcb5f9625f6e42c07b4976c2b4bb`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 30.6 MB (30647241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc185b71db015be6ffb966d849004a9b1afd7a3d9099d9ea8d2b743a4a6affc1`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeddc56dcb85f3b58b490f826f2b8a02a323be04c7e85ee4d67c52805fa43f9b`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 949.9 KB (949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77db48088bf9fcafb03ff9e33ceb1a2be151dcd65566c5fb764c0ac5d261e5b8`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01bd6daab7e4f446ad3a64e1bca2a2425cee9a5999a854476f33bbec8ab8f27`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:380fdcb085ccb206fec4f4b50b8bcf931391fffd2debdf6b738283b3d47535bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2311f82e2f94a4859282c18dbd009a3b9cf910062b4ac4f0a35d53f631178a75`

```dockerfile
```

-	Layers:
	-	`sha256:2502d4bff665dce0aa9952c0fd0a09899110a082f8081b55c899663df32d7c53`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 2.1 MB (2147466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3de91917cccb756e8648efe06ec60e26924d4b0093965412f052790c2ec35c`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 31.1 KB (31131 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:c9de0c54c9ad664ec3718bd74409988036df84f052f65ae5a844237837975b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68494557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087f2f76d1a94a9bcc3555f5f1857ae64bf69071de81794c4e05e3d2d9565d82`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:16:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:16:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:16:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:16:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:16:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:16:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:16:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:16:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 22:44:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 19:18:35 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 19:18:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 19:18:35 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 19:18:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 19:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 19:23:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 19:23:08 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 19:23:10 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 19:23:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 19:23:11 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b041a1a670328abed5fe2b73e068aba477e969ddbfe65c606c8054a4c36067b2`  
		Last Modified: Tue, 23 Jul 2024 01:00:35 GMT  
		Size: 3.3 MB (3263638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51daa6109cd19af541c6fc2600ad5a2f2382e50d3938e2b51f30d24df583fee`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b57c8706e4f06f42a10294d5c9eef985613e48298dedb390c6e6816b60a8f78`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b27cb594dc713e8223f5363b7505f762ad934cbf1c4f47ed7885c05db8e13`  
		Last Modified: Fri, 30 Aug 2024 20:20:12 GMT  
		Size: 12.5 MB (12502099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22237d0261563edb9ca222f6a36c5e175cf1d62c16f38e41755982d955f0e39c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ea243fc20547ec3f93ecbe653822d8a49a7c9c61fd5b7ad229cf6ee331209`  
		Last Modified: Fri, 30 Aug 2024 20:20:15 GMT  
		Size: 16.4 MB (16360114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a08c99e5b1cb1537070b37b1f8f3c78a107be7dd6efdd3a197aa7867d3d7a5c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68481b9e1f3b14557aa8d598c31b8ec7b735f77a5aeac9431ef7b69560d46a92`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c939352561246c630164d6835a0997969adc47f5e678a95dc31e21f57e94926d`  
		Last Modified: Fri, 30 Aug 2024 21:19:20 GMT  
		Size: 29.5 MB (29450758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f957f60156f9b6e900c9f3e132d2e377afa2f2d79dd2350288d3c3cf994fc2`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f354e7435ab3ecb4dc85feb20065dcc85c5b6bdc8e73172c0c130f2ae7cd9`  
		Last Modified: Thu, 05 Sep 2024 22:03:17 GMT  
		Size: 3.5 MB (3528377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12ece5c7e8ab6982a7044cbac04f6e5410efdba180cf3f82d3664a6a5b17b46`  
		Last Modified: Thu, 05 Sep 2024 22:03:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1259f25d9b072394ffbf557569b235c7044742bd33a81a9bfae78d674251acfe`  
		Last Modified: Thu, 05 Sep 2024 22:03:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:9e633785fdb4d8d10f84cec08db3b6f89fb96447cc0173e95e9184513e42af7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (30975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3adde16d5c6cafefdabe56b377da4b9d3bff02923e59c6e8c1b1e3adadc299`

```dockerfile
```

-	Layers:
	-	`sha256:686a058a7390a9266296d88cc6c40607dd67ef5b59d5e5281a954da2c53de8c9`  
		Last Modified: Thu, 05 Sep 2024 22:03:16 GMT  
		Size: 31.0 KB (30975 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:3bbff8da1174ec04349fa78e7ff4738c90ead0b737dd94018dace167d8b85b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66402051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df778fccceef1a7ad544eaff20cdf5cba33ef4ef9612f94e6d77290d4f2e8ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:31:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:31:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:31:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:31:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:31:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:01:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:38:44 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:38:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:38:45 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:38:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:38:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:41:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:41:37 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:41:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:41:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:41:38 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57db3d4836535044109c42cf341df21ab1def6a06fecbaf98ffac833b47f15b`  
		Last Modified: Tue, 23 Jul 2024 01:14:20 GMT  
		Size: 3.1 MB (3073093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991e70be4838afae3979e2bef4b2a7682dffac44793431e072ffbc9fc1686e5`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967a6fef2cedd5f47096963a74875b542f5e4f6667543712aa16505b281dcf7`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c472efc6552ca3c22ddd3afc3423433498a05fa5b26d79a2c74d9c71a5db0515`  
		Last Modified: Fri, 30 Aug 2024 21:50:47 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227ac46a3f3d5c7590120d9f555b6439500ed7212cdfe872e2850b122dc0be1`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba069329678371ed2d3ebd6d6b31019c124d7b205dd0cbc451d0f894c48081d1`  
		Last Modified: Fri, 30 Aug 2024 21:50:49 GMT  
		Size: 15.3 MB (15303131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f1b71f79757d6cb7ae12dc0d78c803efa304cf2be041b5e150fa74c97255c4`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da1f4159b65619170a1816f8957041566fec819f4092f532a9be4fae0766e2`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590a47b24d3ac1c6d1e93d41854d378374a6915b7752990a9bee3fc8716f4c34`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 29.1 MB (29073898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a7d4062ccea4fdf5ed8de172dbc9d1db681bcd5b390a4ffcb54fead69672`  
		Last Modified: Sat, 31 Aug 2024 02:31:06 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ad76e191ec614b29590aed98f8511a696131750ba8ef90780b12d7c01e6a32`  
		Last Modified: Fri, 06 Sep 2024 05:23:13 GMT  
		Size: 3.3 MB (3330474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e96125ef27271af0631684d5f71f871a29af21f239006963b59523149e60154`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4d0f7be48b8b2a1f66d091203ba34585babec9ea0a242b20f051e2e6a4153c`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:cf965cc496769a6d89a79df4f86c9511cdcfc4fae3d1812ee9c0d17a3350f139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414062359f838bcb24d9ae63386a189ce994a98cdc69f5668a083cc43fbe8f33`

```dockerfile
```

-	Layers:
	-	`sha256:06e04688ebe91d0536813dbc53e26f8ef0775ca460042a866ea8fa8a0ca3fa88`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 2.1 MB (2147787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38503d9dfee385b915286c453838f2d94fed6d661d99d2d083ba0ff7fe268092`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 31.2 KB (31230 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:b869809691619076c257df807eea0a48aaa51d4e429db786ea735884edc778f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73242776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe18a77bd397705e87bd4ec8268d8233aada7eb48bf2f1ef4c35f3f556be535`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:30:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 23:30:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 23:30:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 23:30:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:50:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 19:56:37 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 19:56:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 19:56:37 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 19:56:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 19:56:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:01:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:01:00 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:01:01 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:01:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:01:01 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f069fb86c015646c4497d6fa3beaf8bd3f9f04d8f77a1a865ff47fc9922c27e3`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 3.3 MB (3324720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298458c1fe168646ba7edf3e03804ff1a01f1fac6b41ef2a94ef5bf333311f2b`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71c5e072e5141e780c5bbd4c1e2a34f9248a4b4a0983717a6c98be7560b899`  
		Last Modified: Tue, 23 Jul 2024 02:00:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eb94c855017ccb6e05ed05ab6089ac13ef31b7c2c4f68ac1aa7871f5e50f05`  
		Last Modified: Fri, 30 Aug 2024 21:23:23 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7788e2267fee70d1ccfd7ae5b7bdc051ea44976ed82a8dcce577cc9b0c8d6a`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d38576090a615f5e4f5732ed6ca99ac0f1721a6ed93df8c2a86c7b7d9a2539`  
		Last Modified: Fri, 30 Aug 2024 21:23:24 GMT  
		Size: 17.9 MB (17857930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb7c168c56b49540c07601d6cab358cafc4340a5f0dae6ef942aff3d828fa14`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f44bd4d0b7f587d16c7c70ac77c4a0a8d22a607399c38b6eb5ae4d5cd7d78b3`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 19.5 KB (19488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee874a6d0bc05b34617460b975ed3786bc3fb8320c0a847a478a06d8137ad3c`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 31.2 MB (31163203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab4e408f7d446ed2ebe4e87b8fc9ac34818639a1d6bd84e5e45a06bc7106695`  
		Last Modified: Sat, 31 Aug 2024 01:35:35 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471d29effa5f2eb83b2f0a7046bbe384437b0fdb94371156ddb902fcbae0c57d`  
		Last Modified: Thu, 05 Sep 2024 22:04:55 GMT  
		Size: 4.3 MB (4283528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93f6d78874f59727226d8b0f5d434289cfddd237bf281ce65ee61cbf48aed3d`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3de2366387cc3110c6029a23f39e799fee5b9af39ca4d6fd24935000537d74e`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:f671ade9cf000abfebed98797ba31a95e4b9e7c9a66abd8809ee449566a48cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c03772129e8978c8d7e3bf6d6b7628e243c359bf386c62625b423c670dee84`

```dockerfile
```

-	Layers:
	-	`sha256:5b2817a406bb8bbe15f0e63d07de7c7bc61dd5a16b2fa9a5f81bd6eb82393395`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 2.1 MB (2147617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45290e8d87ce7431906c7c10fa965bc3587af107940530164650c6eb891c40a5`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 31.4 KB (31435 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:8312b8751b142b0a015dd9590e85278dc3a744c583f26917cc298274c257f717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49192907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19f9445ebcafde08291d1740ca48717f04d634fcfcfe719397192e34b54f346`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Sep 2024 08:44:06 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Sep 2024 08:44:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Sep 2024 08:44:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_VERSION=8.3.11
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 05 Sep 2024 08:44:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Sep 2024 08:44:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17866811de1cdb9710f37a522dde62051d068230716118d22b6b987216e037ef`  
		Last Modified: Sat, 07 Sep 2024 01:49:46 GMT  
		Size: 3.3 MB (3331976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513ca5d3e6e64e8e064f1b178ad39b5d375a65559181a7f4964c9471461ba8f`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90338393c7a779c5576927d742c98b6841aa39aa84fe1b137708bd8f4d0ae68e`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20961f4e3b99e90c174a4f87f2af7f93ae78322283dde5d669a4c76c2c3cebd8`  
		Last Modified: Sat, 07 Sep 2024 01:51:38 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42171d227440b8721b3056f4e4f3a4916baf777d09c6f844c8f8056fbc70c42`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dabae8861b481fcfb1e16733b346f40d06038d6a5cd82cceb87bd8c3ee3ecd`  
		Last Modified: Sat, 07 Sep 2024 01:51:42 GMT  
		Size: 17.7 MB (17656052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d394881214b919e13be7206b61f0f6743c86558096cefb3ea4f89e68ad0c8d2`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357eacc586709ee7f5d5f8c1962caf6215d0ea35d2d9ed17c68628bfff98004d`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ceaf7eb2dca105a56d8088ae20e32e04da87d85e9f3f09128670d827655bf7`  
		Last Modified: Sat, 07 Sep 2024 02:57:36 GMT  
		Size: 11.3 MB (11281268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f027e9fbe9cf77b0fce954ce8fbd052e739b2ff93e8da28371a6d5e94a0e2cbe`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26346643aadaa9a17917fd876775e1dd782dee44797eb19fffa15a6041861dba`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 927.8 KB (927779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afa2275f20f7dd58d5cfed55223d78856a410a10571131099c93c96790fe01e`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731311864dda11557754fea1b4d013140d3888f5ae6a9ebdf49ab6817c32db2`  
		Last Modified: Sat, 07 Sep 2024 02:57:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:b7ead7cbc4ea95097c0765936f81f348282e2988e0a38da34af421c9e0fb9b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.2 KB (452233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15ae0e3c0095d9fc4067abeed65ebd7323312c0802e512309d7ef6a6f1f3441`

```dockerfile
```

-	Layers:
	-	`sha256:79ad4e506a516203b8ec59310d39679f1819e1ddf6e4eeaf2e829bc8e6c8f719`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 421.1 KB (421135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a25d9908a80b2d5c7108c6c649b0ce7ac73d06c70f6bc5f3f94f655c81dc34`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 31.1 KB (31098 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:bc8587a56d445402ad83ed08b4fa4547ecd680b4c018d5ef5b80cd9c71a89ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73690032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57f38462579c8ced3b7f7847a77a0dfd7b8410d48af550afb90fe24f76fe2d3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 21:55:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 21:55:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 21:55:11 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 21:55:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 21:55:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 21:55:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 21:55:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 21:55:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 22:13:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:31:39 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:31:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:31:39 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:31:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:31:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:34:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:34:17 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:34:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:34:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:34:20 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3b3ac21bbea54c953ea1f2d18929d69c201c50acbb70a6157944a16d881644`  
		Last Modified: Mon, 22 Jul 2024 23:40:54 GMT  
		Size: 3.4 MB (3400973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab89bd2c65997355b0f8d6c170e8ada77fc5d87ae04f4e525032aad1d1c519`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9ea05d06440c67793ed8359925d4dcf5e15c76e0e78b5d20fad34b553a253f`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512248dd3ed75a17d321bc96ddef6ecae12695170f3a768584fe46b6fec8b581`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f97a91111a935f934126b9b5e843f52e61ce5a0d268da80ce88a7e9637e46b`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e963895597cd82f3e2562f1193ef440f635d77e3ce7d65a2d29a5f952d1ee09`  
		Last Modified: Fri, 30 Aug 2024 21:39:34 GMT  
		Size: 18.8 MB (18776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd6fc58c5780a4980b31da9f3258387aa34ad2ae9aa0edd08d9a5b90aaea95`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb9ba050d100c1c32d4f5b3c3975a0ebb302f1b9d8fb6c9b5c21dd9b7279d50`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b5ba9d088f76b4f58ad424d166ff3328d5c7af19e83e9bf897da73af9c27e5`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 31.7 MB (31678361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980ba58d45390240ed5b943d865d41bc6ceaa59661e4c900661678594a767b3f`  
		Last Modified: Sat, 31 Aug 2024 02:19:13 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc9d7e6a424d5f21f867ce20dd0412a843bc862bbfa52a72c8fec70a91e9820`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 3.7 MB (3735823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c66371ed6bb411621f796beb53658e55775622499a2e3cb680d11aef50836b`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e195cdfe80738ab413e61c2c78199d6ce718a1cc53c0e4009150b0b9e080233e`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:efab4d657adc63f8f5ec446309628d53ae9c1619621d59baffac7e8848599a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c0df070a167df4c3900ea024b5889a7c16cd645bc574984ff0d023102c384e`

```dockerfile
```

-	Layers:
	-	`sha256:05f796980c4a0d5999b42b6362b266f43d3c281b065548ce493711bf6784ca18`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 2.1 MB (2146021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa61ab546b7b90ac789c29cb289298af77d133d2b3e4a9c4730de6952b1c4663`  
		Last Modified: Thu, 05 Sep 2024 23:26:45 GMT  
		Size: 31.2 KB (31175 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:bf673fa5bf49303d1284204bbbaebf69ce04845f99f9e2c2306fba331c9dd5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71357432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb65159493a0c7780698a7df08edba41813cfcb4b96941d9f076a7c58890f68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:40:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:40:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:40:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:40:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:40:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:40:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:40:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:40:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 01:15:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 22:01:05 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 22:01:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 22:01:06 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 22:01:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 22:01:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 22:49:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 22:49:31 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 22:49:37 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 22:49:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 22:49:39 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2d0e03d7a4d4766a64c04a50abfb02e217be153dd68888273b46568c4cac04`  
		Last Modified: Tue, 23 Jul 2024 12:29:02 GMT  
		Size: 3.4 MB (3397181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56268c2d820d6bf5bbf0e86c5bc55e50edc209a552c0844c6a9f787a880a2c6`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d3b9188b0e4a61167b2493ce280347bad9dfe72e9ecf4c18c5572f2cb6719`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d23ac9bf2deff71588cfd4b3f47c1364b66f45e05cb5d2518adb6a0396df50`  
		Last Modified: Sat, 31 Aug 2024 02:36:17 GMT  
		Size: 12.5 MB (12502106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869116b457f2e31f8fdb3c69a1bab7e4c51f76c00076389e0239f62c730528cf`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b247cb48214eaf57917fe6fa9b468fc196954c87b0933090b00ffbacd4cb7bd`  
		Last Modified: Sat, 31 Aug 2024 02:36:29 GMT  
		Size: 17.4 MB (17440090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f94c80d7718bd1bbc656205b6b9a90ee074a66d9466f41da567a907abd70f17`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a299e457c645ef0ea5f4f77590cbf1f9bbb149ab3b6d35be1e03c232e21b4298`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb74b37352199c3a76042764443f478982d69b68687aaf3b025bbe890eb8ac3f`  
		Last Modified: Sat, 31 Aug 2024 02:59:25 GMT  
		Size: 31.1 MB (31085763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5e8f63a80e285c25bb4838990371cbc88754639c0329cd9959283425dcc5eb`  
		Last Modified: Sat, 31 Aug 2024 02:59:22 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478ce11c08f84b8b7ef024ae95064e16cbf6ca32a8a9cd7f410dc361463eca95`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 3.5 MB (3537231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ae820656a3026d75cd896ddfb8c712b63434f5e78ca547f38a87da2d57760c`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eab9f887e2c0cae13ef41f6342ed9ff724873ce2065692a1e4cebd9660f3875`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:8e1dca6e31e5eb0d3cdf8a537041418b35bcdadfd2b2c9a2a2647f0ef9f6359b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0580b08ef8ef61d4939757c82ce29de24638ed0fd241ed6af77bf60e5ef3b4`

```dockerfile
```

-	Layers:
	-	`sha256:31a0c112e4561f1142fe90ba25be7145131a0daa0115e16bef20cb4a5e4e596e`  
		Last Modified: Thu, 05 Sep 2024 22:07:28 GMT  
		Size: 2.1 MB (2145637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc47b1511335b2b61390c61f237078daae30b87e51e2d5bbd0c89f5d6e329459`  
		Last Modified: Thu, 05 Sep 2024 22:07:28 GMT  
		Size: 31.2 KB (31176 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:1df015ec24cd23ae2d860ff918845a6067da37bae3e377cc24a7308496b987d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73197813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b68d12485ac34ba23fca979b223aa60d4a14122500e410ef718ce17654bacc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:33:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:33:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:33:37 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:33:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:33:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:33:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:33:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:33:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:08:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:02:04 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:02:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:02:04 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:02:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:02:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:05:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:05:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:05:07 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:05:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:05:07 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bee85c5a5fc33ed0d0f61a077ed76c922b87c42c5cb3a4dbba408dd62a64def`  
		Last Modified: Tue, 23 Jul 2024 00:56:03 GMT  
		Size: 3.5 MB (3467756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1505ad7d669e91b715e2a1bc7ec0c52dd53433332ad45653571cbe2c3643d5`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d87c5417e12df9b44287d4f554dd37d0b5b446d100409e5c49a17ac509a5b2`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2c4b161c20f3e37aa088308da3bb1a01ec5125d77c20033c4794149cec443`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 12.5 MB (12502092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c122a67a16e90a3dfd6817a2f8845d6e6a1bc5b93a02733eed109b49ac9ac44e`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b9a37a60aa5eac97b05abfe815776138ce85dc5ba1906d5c9515c50c45b044`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 18.0 MB (17977689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c966b6ee628194de003583de4dd26ad320f0da92fbe22a571ce2a42dff75c605`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32192d5d915f2f8aabf39455fe449c2d46c8d50ae7e98d0de6c301ac1d15f45a`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7f663cd19fdb2482f23a049a2e83117b526da0ad73131e73fcfe4dc5e53635`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 31.6 MB (31612727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c1e4c810b0e1cb879cad0bec7f75826c9040aceeb755690532fc1181d9fb1`  
		Last Modified: Sat, 31 Aug 2024 01:54:05 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5bd271a220b3b436116cae2105bb3a177c48e043c4dd3fd0d6ed9ab8015848`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 4.2 MB (4152127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d7d905b04205f119efc606778b4f1d82a6e2e5d5e3655790529aae14e90ba6`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b7918b5450a89e93a44512990195960e1a4e0502cb49f82ba3a78eba9350ab`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:ec53877138e3fcd05768b1dc4bb3b19d3728790af26c97b2baf9bf5613b09c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8541813da59e7a04600e48f87a9ab19275d55e61cfbf734906f1bc9ebf5db813`

```dockerfile
```

-	Layers:
	-	`sha256:9e395b5be33bfe7fe5010adb29de378bdee4b6157103397beac3ac320251440a`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 2.1 MB (2145417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ee5098920bf84b8da06f1004dff77d5f0c006fb1cab68bc7718d23ffd153f8`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 31.1 KB (31134 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:85efd59b11f33fc18374fa0e5c86709f8a5fea3e9650df18053cd6d7b04d7714
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
$ docker pull composer@sha256:ef354ecde80d7fcb643c9f6f6aa2e2423078362ff7d12a323fd2c5186dd3d599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68107267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9994d5774040963d44077e2b5c3a689fac3bdfad5312bb016dd94244fbfaee49`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15916673af8229814dcc44164d4616a6141bc5b586ae9362e741d64c6e4c91`  
		Last Modified: Sat, 07 Sep 2024 02:15:12 GMT  
		Size: 3.3 MB (3282678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb3258c4c6a46b7e182fa372bfe03ff37fd0fdf7f6894ca97b564fc382d7d4`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e436918c34ed4c536bdbaeace5213a8aaeb796ec65951fe681a10758ae2677`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6c87b6d10c2d5a9226b306e7fc3370cab80f9f41fe049706de7a51f8e1cf5a`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 12.5 MB (12502103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90d2c6f0ff71e78e4e311ebe4b83b2abbe5fdda23eaa28c5711e68b23c578da`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5cf8a88be3fd539ff5a60321e916df9fa78268109a78972d9411217023bf61`  
		Last Modified: Sat, 07 Sep 2024 02:16:52 GMT  
		Size: 17.2 MB (17212749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eea6dbc4cb9e274ad2228dfea58ecabec99b9336c8d528206ce4c41f6724ad`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f889a53b48220a2103d38ac31ed15adb68d8e5de71c03c475792439675576304`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3080dfea9076e6b057ffd6e2fda1f2313882a16cb3b2be620d444d8716f47ed`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 30.6 MB (30647258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a21f363d6f1fab5e89d290f6716804f9b9506191d9b6c58871a9b11f8bfd2f5`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8b8ffc85688c7454f6c910028225d2b682797bd1677a0ce223545108c4c1c9`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 814.1 KB (814091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493b1985a4a796f58d1385e50c98d9872e2c9a346e575f45768ab2f6a5b0629e`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db0479371de30561eeeb00b17d7b75c81ac293dcf11c4556cb6a71bc59ac403`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:130e8b688936f3b028e396bea0208b91e0e19712fed8e3ae9a1e46b1ca32c778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2242271ab15d1a11c14d542e696cfa8cf177b197dee4d760ba5a20154f2027b8`

```dockerfile
```

-	Layers:
	-	`sha256:65ed272d5ffc6cc8ad2496a3e9b79a1ffb8c4a52ebab178e7e5f5e4eb448bf3b`  
		Last Modified: Sat, 07 Sep 2024 02:57:23 GMT  
		Size: 2.1 MB (2147172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f727a2ffde7c99d01bde1c4bf2d23563b58ba88753e9881f71538c69670a609f`  
		Last Modified: Sat, 07 Sep 2024 02:57:22 GMT  
		Size: 30.8 KB (30827 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:ab4df0f3dfbd1d8965fd3e2de431c1eee1f9beb71e4820a6b4c71b17b4669e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65779848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa7e3a1dedc7be2215c685d01f57637e2bf27ad51bd1e0e71a71abb97fd147f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b041a1a670328abed5fe2b73e068aba477e969ddbfe65c606c8054a4c36067b2`  
		Last Modified: Tue, 23 Jul 2024 01:00:35 GMT  
		Size: 3.3 MB (3263638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51daa6109cd19af541c6fc2600ad5a2f2382e50d3938e2b51f30d24df583fee`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b57c8706e4f06f42a10294d5c9eef985613e48298dedb390c6e6816b60a8f78`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b27cb594dc713e8223f5363b7505f762ad934cbf1c4f47ed7885c05db8e13`  
		Last Modified: Fri, 30 Aug 2024 20:20:12 GMT  
		Size: 12.5 MB (12502099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22237d0261563edb9ca222f6a36c5e175cf1d62c16f38e41755982d955f0e39c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ea243fc20547ec3f93ecbe653822d8a49a7c9c61fd5b7ad229cf6ee331209`  
		Last Modified: Fri, 30 Aug 2024 20:20:15 GMT  
		Size: 16.4 MB (16360114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a08c99e5b1cb1537070b37b1f8f3c78a107be7dd6efdd3a197aa7867d3d7a5c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68481b9e1f3b14557aa8d598c31b8ec7b735f77a5aeac9431ef7b69560d46a92`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c939352561246c630164d6835a0997969adc47f5e678a95dc31e21f57e94926d`  
		Last Modified: Fri, 30 Aug 2024 21:19:20 GMT  
		Size: 29.5 MB (29450758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f957f60156f9b6e900c9f3e132d2e377afa2f2d79dd2350288d3c3cf994fc2`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0024ec06ef23ce4ec077a63b60db5ffb584e27216e5be4423204ed6b3ee9d9ff`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 813.7 KB (813668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff00edb04cb0f9ff5be423ef9e64b2cc05ec099877d249544ab29d1038f5de3d`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849dafc07c8b03b2973789919523ffe9f0c9052a63652530c735314f8942657c`  
		Last Modified: Fri, 30 Aug 2024 21:19:20 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:515fe315f96216572fe9c92807daa2364060f55adb0939343f2e6f9c2ee5fab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0dde179ac6a00aee0b55cd0d47db549566a3234a33f45f2b16cfa4330eb46d`

```dockerfile
```

-	Layers:
	-	`sha256:f1dce4243535ccf2d00cbd4d3919988ef14db980db9aec68d4cdcbd5921a2ecf`  
		Last Modified: Fri, 30 Aug 2024 21:19:17 GMT  
		Size: 30.7 KB (30659 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:22599a3b141c242ec907a22de0a45dc607d4663fa65663ed4ce7fcae0b8e515e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63876262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30061f8b6f60071707176e9d676ae5f17ead9642086e9888c2aa65dc3176bdf8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57db3d4836535044109c42cf341df21ab1def6a06fecbaf98ffac833b47f15b`  
		Last Modified: Tue, 23 Jul 2024 01:14:20 GMT  
		Size: 3.1 MB (3073093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991e70be4838afae3979e2bef4b2a7682dffac44793431e072ffbc9fc1686e5`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967a6fef2cedd5f47096963a74875b542f5e4f6667543712aa16505b281dcf7`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c472efc6552ca3c22ddd3afc3423433498a05fa5b26d79a2c74d9c71a5db0515`  
		Last Modified: Fri, 30 Aug 2024 21:50:47 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227ac46a3f3d5c7590120d9f555b6439500ed7212cdfe872e2850b122dc0be1`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba069329678371ed2d3ebd6d6b31019c124d7b205dd0cbc451d0f894c48081d1`  
		Last Modified: Fri, 30 Aug 2024 21:50:49 GMT  
		Size: 15.3 MB (15303131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f1b71f79757d6cb7ae12dc0d78c803efa304cf2be041b5e150fa74c97255c4`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da1f4159b65619170a1816f8957041566fec819f4092f532a9be4fae0766e2`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590a47b24d3ac1c6d1e93d41854d378374a6915b7752990a9bee3fc8716f4c34`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 29.1 MB (29073898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a7d4062ccea4fdf5ed8de172dbc9d1db681bcd5b390a4ffcb54fead69672`  
		Last Modified: Sat, 31 Aug 2024 02:31:06 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bcd20a2a658d50ec683a43833566710b84f4216194938d7af7cbf8c10210dd`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 804.7 KB (804685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905190ed1bd03845eedb722e18ffc45b80ef025ab1c6f43997c55f1f800ceb`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944773c52e9f707928b0d29b7bf87541ac3570feff0f533ced8b01645298d971`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:7fe76e5b9a9780c9cdbd9a895cc83c3b2476377536e62b87dbf161a9d0f338cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22918c5d8eba2985f99f9354a988108467181b3ec0587cfa0d276b25b148816d`

```dockerfile
```

-	Layers:
	-	`sha256:118580ec0c28ea60bb073b0529386d6410c5c3273787f1a0148d457792bdf79e`  
		Last Modified: Sat, 31 Aug 2024 02:31:05 GMT  
		Size: 2.1 MB (2147485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ac676009902101bbbc64e493d54a458bf29a597d82a7e60d159f970a30ca75d`  
		Last Modified: Sat, 31 Aug 2024 02:31:05 GMT  
		Size: 30.9 KB (30914 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:70a06924a1e1de676becb0dc74871a52c4236a11f810813c33eafacd3afed37e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69774571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d481a74ee31aad0920de6ddaad5d09e95246121f99bffee6edcd55bc4753b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f069fb86c015646c4497d6fa3beaf8bd3f9f04d8f77a1a865ff47fc9922c27e3`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 3.3 MB (3324720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298458c1fe168646ba7edf3e03804ff1a01f1fac6b41ef2a94ef5bf333311f2b`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71c5e072e5141e780c5bbd4c1e2a34f9248a4b4a0983717a6c98be7560b899`  
		Last Modified: Tue, 23 Jul 2024 02:00:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eb94c855017ccb6e05ed05ab6089ac13ef31b7c2c4f68ac1aa7871f5e50f05`  
		Last Modified: Fri, 30 Aug 2024 21:23:23 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7788e2267fee70d1ccfd7ae5b7bdc051ea44976ed82a8dcce577cc9b0c8d6a`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d38576090a615f5e4f5732ed6ca99ac0f1721a6ed93df8c2a86c7b7d9a2539`  
		Last Modified: Fri, 30 Aug 2024 21:23:24 GMT  
		Size: 17.9 MB (17857930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb7c168c56b49540c07601d6cab358cafc4340a5f0dae6ef942aff3d828fa14`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f44bd4d0b7f587d16c7c70ac77c4a0a8d22a607399c38b6eb5ae4d5cd7d78b3`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 19.5 KB (19488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee874a6d0bc05b34617460b975ed3786bc3fb8320c0a847a478a06d8137ad3c`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 31.2 MB (31163203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab4e408f7d446ed2ebe4e87b8fc9ac34818639a1d6bd84e5e45a06bc7106695`  
		Last Modified: Sat, 31 Aug 2024 01:35:35 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf88b56f2caff98fcaa837bcf1d25e968ad076d11a4b61bfeb3c6b5cb980212`  
		Last Modified: Sat, 31 Aug 2024 01:35:35 GMT  
		Size: 815.3 KB (815324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ed584abd72db3d3f41e633a17439ea5d6bbd61a8b8665eec82007ba1f083db`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75117c9eb6ed3b4cec0958d69174c5b7e7e490066ac0b82c25e9f9aa41b51326`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:680855afdfda70272d7bd80eda23b12167edb0f61bd1cbc3b94fdb0edf031025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729e6a7d8a05bb40c7ad680fb68991849ef818a43f82b8a33486f821729d49e1`

```dockerfile
```

-	Layers:
	-	`sha256:f383e20574737e2d7e47e5b7459e472aa1655e78a05434eb57222186191c3937`  
		Last Modified: Sat, 31 Aug 2024 01:35:34 GMT  
		Size: 2.1 MB (2147311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918075db4af02abd114ef74c8ef7850a61efd057308a01599c2a509e05136945`  
		Last Modified: Sat, 31 Aug 2024 01:35:33 GMT  
		Size: 31.1 KB (31116 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:c285efacb3574249fdedf50f233480f6f3a622d40ce8f013d01ec36b29f87402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49056520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfce11e18c987a6a1d470dd14b899f54bed07bf2249f5cd66e473e33531f2a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17866811de1cdb9710f37a522dde62051d068230716118d22b6b987216e037ef`  
		Last Modified: Sat, 07 Sep 2024 01:49:46 GMT  
		Size: 3.3 MB (3331976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513ca5d3e6e64e8e064f1b178ad39b5d375a65559181a7f4964c9471461ba8f`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90338393c7a779c5576927d742c98b6841aa39aa84fe1b137708bd8f4d0ae68e`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20961f4e3b99e90c174a4f87f2af7f93ae78322283dde5d669a4c76c2c3cebd8`  
		Last Modified: Sat, 07 Sep 2024 01:51:38 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42171d227440b8721b3056f4e4f3a4916baf777d09c6f844c8f8056fbc70c42`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dabae8861b481fcfb1e16733b346f40d06038d6a5cd82cceb87bd8c3ee3ecd`  
		Last Modified: Sat, 07 Sep 2024 01:51:42 GMT  
		Size: 17.7 MB (17656052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d394881214b919e13be7206b61f0f6743c86558096cefb3ea4f89e68ad0c8d2`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357eacc586709ee7f5d5f8c1962caf6215d0ea35d2d9ed17c68628bfff98004d`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c0582899ef276d3ef7782d863b75dc242b983d81f3ba38e9c2526cd4b66124`  
		Last Modified: Sat, 07 Sep 2024 02:57:38 GMT  
		Size: 11.3 MB (11281287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d9b78c504cbbb63a0444a48b1d4abf81c85399c46d67ae6bfe5b3e592c9b07`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a00cf43fce9b7a0f59f2513c440ceec89371153bcd9718ee7bf9392be0af70`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 791.4 KB (791375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002ae015b5c77256a349e1730eb8973dd000ba3b28d58f103d2ae02f5bdfd086`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370385d9ee8afe32b45f8acb99057b97b2791438daa050af3567f9b2011e5ba7`  
		Last Modified: Sat, 07 Sep 2024 02:57:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:5560243fa9b4a0bf35a669d325d6f47575b763d236dad10a588b2794f6e19fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.6 KB (451645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbf874329e4a41ef89503cb290d41ce3e36b666436c0e3aceac07aa9559dae0`

```dockerfile
```

-	Layers:
	-	`sha256:9a25c0d8e3da3517fbb36dbae00efe024ab4215f087b5a0470aac811b8e86ee7`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 420.8 KB (420846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0189d0fc46ef2c7b6d129d2de1b6c3fd667779e48e4c8fa308b37bc400b42457`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 30.8 KB (30799 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:a98e733029bd8bd44adf828da681cc6c0da1b605d06cba3baf2a8b80ee1350b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70775287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfff63a4151c0efd88ae55b48123f440bcd7921a92db6c257f8a438cfb51f23`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3b3ac21bbea54c953ea1f2d18929d69c201c50acbb70a6157944a16d881644`  
		Last Modified: Mon, 22 Jul 2024 23:40:54 GMT  
		Size: 3.4 MB (3400973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab89bd2c65997355b0f8d6c170e8ada77fc5d87ae04f4e525032aad1d1c519`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9ea05d06440c67793ed8359925d4dcf5e15c76e0e78b5d20fad34b553a253f`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512248dd3ed75a17d321bc96ddef6ecae12695170f3a768584fe46b6fec8b581`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f97a91111a935f934126b9b5e843f52e61ce5a0d268da80ce88a7e9637e46b`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e963895597cd82f3e2562f1193ef440f635d77e3ce7d65a2d29a5f952d1ee09`  
		Last Modified: Fri, 30 Aug 2024 21:39:34 GMT  
		Size: 18.8 MB (18776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd6fc58c5780a4980b31da9f3258387aa34ad2ae9aa0edd08d9a5b90aaea95`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb9ba050d100c1c32d4f5b3c3975a0ebb302f1b9d8fb6c9b5c21dd9b7279d50`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b5ba9d088f76b4f58ad424d166ff3328d5c7af19e83e9bf897da73af9c27e5`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 31.7 MB (31678361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980ba58d45390240ed5b943d865d41bc6ceaa59661e4c900661678594a767b3f`  
		Last Modified: Sat, 31 Aug 2024 02:19:13 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07828b0dd98ae703ba1a00be52e896320b18f9b775c708e0176dd7eb96c55318`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 821.1 KB (821079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56202f9e9bddca31133a9f7d83d52de986e3ded88d49ca9325295c16ec61e825`  
		Last Modified: Sat, 31 Aug 2024 02:19:13 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5829414f07c88033c7b407bc997bf4ed280a090d6494a4ca8c5a43d9f9d507d`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:c2fb27528e57fcdedc855613535ad95bb72b53d89902100e6c13347f655f3e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20ba4e929e3a856a4e26b6fa2bae28094763c8c6e038738cb3819c81f60bff0`

```dockerfile
```

-	Layers:
	-	`sha256:bf98f04c0fc52370a048dbc21243cd1217109a725f6167ca0fe28f0d161d8746`  
		Last Modified: Sat, 31 Aug 2024 02:19:12 GMT  
		Size: 2.1 MB (2145721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e647917393f3fc730762c47f394b76bd81338d62c29a6829e595ec0a11acb9b0`  
		Last Modified: Sat, 31 Aug 2024 02:19:11 GMT  
		Size: 30.9 KB (30863 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:a4541babb1bf884f8dedb757ea86c56b94440baba3cf51eefa25d4b8ca347831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68633473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0545a0bc5ecec19f06ebf5d04b5fc85fcf2b61af79fcf2d19934a221486b28c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2d0e03d7a4d4766a64c04a50abfb02e217be153dd68888273b46568c4cac04`  
		Last Modified: Tue, 23 Jul 2024 12:29:02 GMT  
		Size: 3.4 MB (3397181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56268c2d820d6bf5bbf0e86c5bc55e50edc209a552c0844c6a9f787a880a2c6`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d3b9188b0e4a61167b2493ce280347bad9dfe72e9ecf4c18c5572f2cb6719`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d23ac9bf2deff71588cfd4b3f47c1364b66f45e05cb5d2518adb6a0396df50`  
		Last Modified: Sat, 31 Aug 2024 02:36:17 GMT  
		Size: 12.5 MB (12502106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869116b457f2e31f8fdb3c69a1bab7e4c51f76c00076389e0239f62c730528cf`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b247cb48214eaf57917fe6fa9b468fc196954c87b0933090b00ffbacd4cb7bd`  
		Last Modified: Sat, 31 Aug 2024 02:36:29 GMT  
		Size: 17.4 MB (17440090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f94c80d7718bd1bbc656205b6b9a90ee074a66d9466f41da567a907abd70f17`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a299e457c645ef0ea5f4f77590cbf1f9bbb149ab3b6d35be1e03c232e21b4298`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb74b37352199c3a76042764443f478982d69b68687aaf3b025bbe890eb8ac3f`  
		Last Modified: Sat, 31 Aug 2024 02:59:25 GMT  
		Size: 31.1 MB (31085763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5e8f63a80e285c25bb4838990371cbc88754639c0329cd9959283425dcc5eb`  
		Last Modified: Sat, 31 Aug 2024 02:59:22 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd31bfeaed307e2701b79ab306d11ba9930bdf53c96eae5d5be586fdd1a56c6`  
		Last Modified: Sat, 31 Aug 2024 02:59:23 GMT  
		Size: 813.3 KB (813274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d571efdeb9bf54898af4e90923d32cc1c04e057a94ef91d1f753564f845bbb3b`  
		Last Modified: Sat, 31 Aug 2024 02:59:23 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2ab762566804d399ae0112a549d382e9e600b6b797048e440647dc4068be0c`  
		Last Modified: Sat, 31 Aug 2024 02:59:24 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:74044b90f011c891b06d80de02d02a56176762bbb679773a6d2446aec14584a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9783a359efa8738da17df08006fa430317809a32da56f2c37fa5ac913f69a720`

```dockerfile
```

-	Layers:
	-	`sha256:da4a7db55dc6e1522447c9d2beba40a94e5e604f7b5975095838d818e014e1b6`  
		Last Modified: Sat, 31 Aug 2024 02:59:20 GMT  
		Size: 2.1 MB (2145337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d69e59b16ea8290aa0ba5b1aff93c6f68ef6c036c9e39e175dec687d048838`  
		Last Modified: Sat, 31 Aug 2024 02:59:20 GMT  
		Size: 30.9 KB (30863 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:462905e539aedfd429d5c4c88d0a261f44f9ec753aaf9ef74a5dce9e53f78dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70350912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a560a0380c0f62794aed4a67120e26db5c383f3c4746d40a44174a1365b76e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bee85c5a5fc33ed0d0f61a077ed76c922b87c42c5cb3a4dbba408dd62a64def`  
		Last Modified: Tue, 23 Jul 2024 00:56:03 GMT  
		Size: 3.5 MB (3467756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1505ad7d669e91b715e2a1bc7ec0c52dd53433332ad45653571cbe2c3643d5`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d87c5417e12df9b44287d4f554dd37d0b5b446d100409e5c49a17ac509a5b2`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2c4b161c20f3e37aa088308da3bb1a01ec5125d77c20033c4794149cec443`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 12.5 MB (12502092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c122a67a16e90a3dfd6817a2f8845d6e6a1bc5b93a02733eed109b49ac9ac44e`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b9a37a60aa5eac97b05abfe815776138ce85dc5ba1906d5c9515c50c45b044`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 18.0 MB (17977689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c966b6ee628194de003583de4dd26ad320f0da92fbe22a571ce2a42dff75c605`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32192d5d915f2f8aabf39455fe449c2d46c8d50ae7e98d0de6c301ac1d15f45a`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7f663cd19fdb2482f23a049a2e83117b526da0ad73131e73fcfe4dc5e53635`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 31.6 MB (31612727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c1e4c810b0e1cb879cad0bec7f75826c9040aceeb755690532fc1181d9fb1`  
		Last Modified: Sat, 31 Aug 2024 01:54:05 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d04ad993fbf3f6aa557c5ae6eab0cd4e7337a5a2ea31afe9f9655f2d2f19db`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 1.3 MB (1305226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57acd2fbfc4b9afdbc3e4bb67dc65e135d60a71d7c7cccb3c4cd632f5304c946`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e753b7b604d5e0a37393a583ddea761ff87299164502e1e51222836366efb986`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:dbddd69d1ea80b21d5d1cf1ae9784cf243be1154a4ee3640cd18b92affeb8004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690c598e3d18036cf2a51a0c1cced0c355ddd077ad7da5e9478be8130385646b`

```dockerfile
```

-	Layers:
	-	`sha256:65eb103a793493d81a73a2c0dfb27394094894f3cea1f0821a49dff434207a0b`  
		Last Modified: Sat, 31 Aug 2024 01:54:04 GMT  
		Size: 2.1 MB (2145123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f57bc9ec7e845944ed195006c8e0df013226a85e7956944dcd7240cab5bc2e9f`  
		Last Modified: Sat, 31 Aug 2024 01:54:04 GMT  
		Size: 30.8 KB (30830 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.24`

```console
$ docker pull composer@sha256:85efd59b11f33fc18374fa0e5c86709f8a5fea3e9650df18053cd6d7b04d7714
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

### `composer:2.2.24` - linux; amd64

```console
$ docker pull composer@sha256:ef354ecde80d7fcb643c9f6f6aa2e2423078362ff7d12a323fd2c5186dd3d599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68107267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9994d5774040963d44077e2b5c3a689fac3bdfad5312bb016dd94244fbfaee49`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15916673af8229814dcc44164d4616a6141bc5b586ae9362e741d64c6e4c91`  
		Last Modified: Sat, 07 Sep 2024 02:15:12 GMT  
		Size: 3.3 MB (3282678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb3258c4c6a46b7e182fa372bfe03ff37fd0fdf7f6894ca97b564fc382d7d4`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e436918c34ed4c536bdbaeace5213a8aaeb796ec65951fe681a10758ae2677`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6c87b6d10c2d5a9226b306e7fc3370cab80f9f41fe049706de7a51f8e1cf5a`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 12.5 MB (12502103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90d2c6f0ff71e78e4e311ebe4b83b2abbe5fdda23eaa28c5711e68b23c578da`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5cf8a88be3fd539ff5a60321e916df9fa78268109a78972d9411217023bf61`  
		Last Modified: Sat, 07 Sep 2024 02:16:52 GMT  
		Size: 17.2 MB (17212749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eea6dbc4cb9e274ad2228dfea58ecabec99b9336c8d528206ce4c41f6724ad`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f889a53b48220a2103d38ac31ed15adb68d8e5de71c03c475792439675576304`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3080dfea9076e6b057ffd6e2fda1f2313882a16cb3b2be620d444d8716f47ed`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 30.6 MB (30647258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a21f363d6f1fab5e89d290f6716804f9b9506191d9b6c58871a9b11f8bfd2f5`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8b8ffc85688c7454f6c910028225d2b682797bd1677a0ce223545108c4c1c9`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 814.1 KB (814091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493b1985a4a796f58d1385e50c98d9872e2c9a346e575f45768ab2f6a5b0629e`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db0479371de30561eeeb00b17d7b75c81ac293dcf11c4556cb6a71bc59ac403`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:130e8b688936f3b028e396bea0208b91e0e19712fed8e3ae9a1e46b1ca32c778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2242271ab15d1a11c14d542e696cfa8cf177b197dee4d760ba5a20154f2027b8`

```dockerfile
```

-	Layers:
	-	`sha256:65ed272d5ffc6cc8ad2496a3e9b79a1ffb8c4a52ebab178e7e5f5e4eb448bf3b`  
		Last Modified: Sat, 07 Sep 2024 02:57:23 GMT  
		Size: 2.1 MB (2147172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f727a2ffde7c99d01bde1c4bf2d23563b58ba88753e9881f71538c69670a609f`  
		Last Modified: Sat, 07 Sep 2024 02:57:22 GMT  
		Size: 30.8 KB (30827 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; arm variant v6

```console
$ docker pull composer@sha256:ab4df0f3dfbd1d8965fd3e2de431c1eee1f9beb71e4820a6b4c71b17b4669e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65779848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa7e3a1dedc7be2215c685d01f57637e2bf27ad51bd1e0e71a71abb97fd147f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b041a1a670328abed5fe2b73e068aba477e969ddbfe65c606c8054a4c36067b2`  
		Last Modified: Tue, 23 Jul 2024 01:00:35 GMT  
		Size: 3.3 MB (3263638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51daa6109cd19af541c6fc2600ad5a2f2382e50d3938e2b51f30d24df583fee`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b57c8706e4f06f42a10294d5c9eef985613e48298dedb390c6e6816b60a8f78`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b27cb594dc713e8223f5363b7505f762ad934cbf1c4f47ed7885c05db8e13`  
		Last Modified: Fri, 30 Aug 2024 20:20:12 GMT  
		Size: 12.5 MB (12502099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22237d0261563edb9ca222f6a36c5e175cf1d62c16f38e41755982d955f0e39c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ea243fc20547ec3f93ecbe653822d8a49a7c9c61fd5b7ad229cf6ee331209`  
		Last Modified: Fri, 30 Aug 2024 20:20:15 GMT  
		Size: 16.4 MB (16360114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a08c99e5b1cb1537070b37b1f8f3c78a107be7dd6efdd3a197aa7867d3d7a5c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68481b9e1f3b14557aa8d598c31b8ec7b735f77a5aeac9431ef7b69560d46a92`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c939352561246c630164d6835a0997969adc47f5e678a95dc31e21f57e94926d`  
		Last Modified: Fri, 30 Aug 2024 21:19:20 GMT  
		Size: 29.5 MB (29450758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f957f60156f9b6e900c9f3e132d2e377afa2f2d79dd2350288d3c3cf994fc2`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0024ec06ef23ce4ec077a63b60db5ffb584e27216e5be4423204ed6b3ee9d9ff`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 813.7 KB (813668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff00edb04cb0f9ff5be423ef9e64b2cc05ec099877d249544ab29d1038f5de3d`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849dafc07c8b03b2973789919523ffe9f0c9052a63652530c735314f8942657c`  
		Last Modified: Fri, 30 Aug 2024 21:19:20 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:515fe315f96216572fe9c92807daa2364060f55adb0939343f2e6f9c2ee5fab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0dde179ac6a00aee0b55cd0d47db549566a3234a33f45f2b16cfa4330eb46d`

```dockerfile
```

-	Layers:
	-	`sha256:f1dce4243535ccf2d00cbd4d3919988ef14db980db9aec68d4cdcbd5921a2ecf`  
		Last Modified: Fri, 30 Aug 2024 21:19:17 GMT  
		Size: 30.7 KB (30659 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; arm variant v7

```console
$ docker pull composer@sha256:22599a3b141c242ec907a22de0a45dc607d4663fa65663ed4ce7fcae0b8e515e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63876262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30061f8b6f60071707176e9d676ae5f17ead9642086e9888c2aa65dc3176bdf8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57db3d4836535044109c42cf341df21ab1def6a06fecbaf98ffac833b47f15b`  
		Last Modified: Tue, 23 Jul 2024 01:14:20 GMT  
		Size: 3.1 MB (3073093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991e70be4838afae3979e2bef4b2a7682dffac44793431e072ffbc9fc1686e5`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967a6fef2cedd5f47096963a74875b542f5e4f6667543712aa16505b281dcf7`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c472efc6552ca3c22ddd3afc3423433498a05fa5b26d79a2c74d9c71a5db0515`  
		Last Modified: Fri, 30 Aug 2024 21:50:47 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227ac46a3f3d5c7590120d9f555b6439500ed7212cdfe872e2850b122dc0be1`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba069329678371ed2d3ebd6d6b31019c124d7b205dd0cbc451d0f894c48081d1`  
		Last Modified: Fri, 30 Aug 2024 21:50:49 GMT  
		Size: 15.3 MB (15303131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f1b71f79757d6cb7ae12dc0d78c803efa304cf2be041b5e150fa74c97255c4`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da1f4159b65619170a1816f8957041566fec819f4092f532a9be4fae0766e2`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590a47b24d3ac1c6d1e93d41854d378374a6915b7752990a9bee3fc8716f4c34`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 29.1 MB (29073898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a7d4062ccea4fdf5ed8de172dbc9d1db681bcd5b390a4ffcb54fead69672`  
		Last Modified: Sat, 31 Aug 2024 02:31:06 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bcd20a2a658d50ec683a43833566710b84f4216194938d7af7cbf8c10210dd`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 804.7 KB (804685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905190ed1bd03845eedb722e18ffc45b80ef025ab1c6f43997c55f1f800ceb`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944773c52e9f707928b0d29b7bf87541ac3570feff0f533ced8b01645298d971`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:7fe76e5b9a9780c9cdbd9a895cc83c3b2476377536e62b87dbf161a9d0f338cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22918c5d8eba2985f99f9354a988108467181b3ec0587cfa0d276b25b148816d`

```dockerfile
```

-	Layers:
	-	`sha256:118580ec0c28ea60bb073b0529386d6410c5c3273787f1a0148d457792bdf79e`  
		Last Modified: Sat, 31 Aug 2024 02:31:05 GMT  
		Size: 2.1 MB (2147485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ac676009902101bbbc64e493d54a458bf29a597d82a7e60d159f970a30ca75d`  
		Last Modified: Sat, 31 Aug 2024 02:31:05 GMT  
		Size: 30.9 KB (30914 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:70a06924a1e1de676becb0dc74871a52c4236a11f810813c33eafacd3afed37e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69774571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d481a74ee31aad0920de6ddaad5d09e95246121f99bffee6edcd55bc4753b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f069fb86c015646c4497d6fa3beaf8bd3f9f04d8f77a1a865ff47fc9922c27e3`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 3.3 MB (3324720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298458c1fe168646ba7edf3e03804ff1a01f1fac6b41ef2a94ef5bf333311f2b`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71c5e072e5141e780c5bbd4c1e2a34f9248a4b4a0983717a6c98be7560b899`  
		Last Modified: Tue, 23 Jul 2024 02:00:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eb94c855017ccb6e05ed05ab6089ac13ef31b7c2c4f68ac1aa7871f5e50f05`  
		Last Modified: Fri, 30 Aug 2024 21:23:23 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7788e2267fee70d1ccfd7ae5b7bdc051ea44976ed82a8dcce577cc9b0c8d6a`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d38576090a615f5e4f5732ed6ca99ac0f1721a6ed93df8c2a86c7b7d9a2539`  
		Last Modified: Fri, 30 Aug 2024 21:23:24 GMT  
		Size: 17.9 MB (17857930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb7c168c56b49540c07601d6cab358cafc4340a5f0dae6ef942aff3d828fa14`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f44bd4d0b7f587d16c7c70ac77c4a0a8d22a607399c38b6eb5ae4d5cd7d78b3`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 19.5 KB (19488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee874a6d0bc05b34617460b975ed3786bc3fb8320c0a847a478a06d8137ad3c`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 31.2 MB (31163203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab4e408f7d446ed2ebe4e87b8fc9ac34818639a1d6bd84e5e45a06bc7106695`  
		Last Modified: Sat, 31 Aug 2024 01:35:35 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf88b56f2caff98fcaa837bcf1d25e968ad076d11a4b61bfeb3c6b5cb980212`  
		Last Modified: Sat, 31 Aug 2024 01:35:35 GMT  
		Size: 815.3 KB (815324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ed584abd72db3d3f41e633a17439ea5d6bbd61a8b8665eec82007ba1f083db`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75117c9eb6ed3b4cec0958d69174c5b7e7e490066ac0b82c25e9f9aa41b51326`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:680855afdfda70272d7bd80eda23b12167edb0f61bd1cbc3b94fdb0edf031025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729e6a7d8a05bb40c7ad680fb68991849ef818a43f82b8a33486f821729d49e1`

```dockerfile
```

-	Layers:
	-	`sha256:f383e20574737e2d7e47e5b7459e472aa1655e78a05434eb57222186191c3937`  
		Last Modified: Sat, 31 Aug 2024 01:35:34 GMT  
		Size: 2.1 MB (2147311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918075db4af02abd114ef74c8ef7850a61efd057308a01599c2a509e05136945`  
		Last Modified: Sat, 31 Aug 2024 01:35:33 GMT  
		Size: 31.1 KB (31116 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; 386

```console
$ docker pull composer@sha256:c285efacb3574249fdedf50f233480f6f3a622d40ce8f013d01ec36b29f87402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49056520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfce11e18c987a6a1d470dd14b899f54bed07bf2249f5cd66e473e33531f2a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17866811de1cdb9710f37a522dde62051d068230716118d22b6b987216e037ef`  
		Last Modified: Sat, 07 Sep 2024 01:49:46 GMT  
		Size: 3.3 MB (3331976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513ca5d3e6e64e8e064f1b178ad39b5d375a65559181a7f4964c9471461ba8f`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90338393c7a779c5576927d742c98b6841aa39aa84fe1b137708bd8f4d0ae68e`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20961f4e3b99e90c174a4f87f2af7f93ae78322283dde5d669a4c76c2c3cebd8`  
		Last Modified: Sat, 07 Sep 2024 01:51:38 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42171d227440b8721b3056f4e4f3a4916baf777d09c6f844c8f8056fbc70c42`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dabae8861b481fcfb1e16733b346f40d06038d6a5cd82cceb87bd8c3ee3ecd`  
		Last Modified: Sat, 07 Sep 2024 01:51:42 GMT  
		Size: 17.7 MB (17656052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d394881214b919e13be7206b61f0f6743c86558096cefb3ea4f89e68ad0c8d2`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357eacc586709ee7f5d5f8c1962caf6215d0ea35d2d9ed17c68628bfff98004d`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c0582899ef276d3ef7782d863b75dc242b983d81f3ba38e9c2526cd4b66124`  
		Last Modified: Sat, 07 Sep 2024 02:57:38 GMT  
		Size: 11.3 MB (11281287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d9b78c504cbbb63a0444a48b1d4abf81c85399c46d67ae6bfe5b3e592c9b07`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a00cf43fce9b7a0f59f2513c440ceec89371153bcd9718ee7bf9392be0af70`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 791.4 KB (791375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002ae015b5c77256a349e1730eb8973dd000ba3b28d58f103d2ae02f5bdfd086`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370385d9ee8afe32b45f8acb99057b97b2791438daa050af3567f9b2011e5ba7`  
		Last Modified: Sat, 07 Sep 2024 02:57:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:5560243fa9b4a0bf35a669d325d6f47575b763d236dad10a588b2794f6e19fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.6 KB (451645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbf874329e4a41ef89503cb290d41ce3e36b666436c0e3aceac07aa9559dae0`

```dockerfile
```

-	Layers:
	-	`sha256:9a25c0d8e3da3517fbb36dbae00efe024ab4215f087b5a0470aac811b8e86ee7`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 420.8 KB (420846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0189d0fc46ef2c7b6d129d2de1b6c3fd667779e48e4c8fa308b37bc400b42457`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 30.8 KB (30799 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; ppc64le

```console
$ docker pull composer@sha256:a98e733029bd8bd44adf828da681cc6c0da1b605d06cba3baf2a8b80ee1350b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70775287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfff63a4151c0efd88ae55b48123f440bcd7921a92db6c257f8a438cfb51f23`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3b3ac21bbea54c953ea1f2d18929d69c201c50acbb70a6157944a16d881644`  
		Last Modified: Mon, 22 Jul 2024 23:40:54 GMT  
		Size: 3.4 MB (3400973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab89bd2c65997355b0f8d6c170e8ada77fc5d87ae04f4e525032aad1d1c519`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9ea05d06440c67793ed8359925d4dcf5e15c76e0e78b5d20fad34b553a253f`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512248dd3ed75a17d321bc96ddef6ecae12695170f3a768584fe46b6fec8b581`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f97a91111a935f934126b9b5e843f52e61ce5a0d268da80ce88a7e9637e46b`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e963895597cd82f3e2562f1193ef440f635d77e3ce7d65a2d29a5f952d1ee09`  
		Last Modified: Fri, 30 Aug 2024 21:39:34 GMT  
		Size: 18.8 MB (18776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd6fc58c5780a4980b31da9f3258387aa34ad2ae9aa0edd08d9a5b90aaea95`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb9ba050d100c1c32d4f5b3c3975a0ebb302f1b9d8fb6c9b5c21dd9b7279d50`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b5ba9d088f76b4f58ad424d166ff3328d5c7af19e83e9bf897da73af9c27e5`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 31.7 MB (31678361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980ba58d45390240ed5b943d865d41bc6ceaa59661e4c900661678594a767b3f`  
		Last Modified: Sat, 31 Aug 2024 02:19:13 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07828b0dd98ae703ba1a00be52e896320b18f9b775c708e0176dd7eb96c55318`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 821.1 KB (821079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56202f9e9bddca31133a9f7d83d52de986e3ded88d49ca9325295c16ec61e825`  
		Last Modified: Sat, 31 Aug 2024 02:19:13 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5829414f07c88033c7b407bc997bf4ed280a090d6494a4ca8c5a43d9f9d507d`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:c2fb27528e57fcdedc855613535ad95bb72b53d89902100e6c13347f655f3e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20ba4e929e3a856a4e26b6fa2bae28094763c8c6e038738cb3819c81f60bff0`

```dockerfile
```

-	Layers:
	-	`sha256:bf98f04c0fc52370a048dbc21243cd1217109a725f6167ca0fe28f0d161d8746`  
		Last Modified: Sat, 31 Aug 2024 02:19:12 GMT  
		Size: 2.1 MB (2145721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e647917393f3fc730762c47f394b76bd81338d62c29a6829e595ec0a11acb9b0`  
		Last Modified: Sat, 31 Aug 2024 02:19:11 GMT  
		Size: 30.9 KB (30863 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; riscv64

```console
$ docker pull composer@sha256:a4541babb1bf884f8dedb757ea86c56b94440baba3cf51eefa25d4b8ca347831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68633473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0545a0bc5ecec19f06ebf5d04b5fc85fcf2b61af79fcf2d19934a221486b28c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2d0e03d7a4d4766a64c04a50abfb02e217be153dd68888273b46568c4cac04`  
		Last Modified: Tue, 23 Jul 2024 12:29:02 GMT  
		Size: 3.4 MB (3397181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56268c2d820d6bf5bbf0e86c5bc55e50edc209a552c0844c6a9f787a880a2c6`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d3b9188b0e4a61167b2493ce280347bad9dfe72e9ecf4c18c5572f2cb6719`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d23ac9bf2deff71588cfd4b3f47c1364b66f45e05cb5d2518adb6a0396df50`  
		Last Modified: Sat, 31 Aug 2024 02:36:17 GMT  
		Size: 12.5 MB (12502106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869116b457f2e31f8fdb3c69a1bab7e4c51f76c00076389e0239f62c730528cf`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b247cb48214eaf57917fe6fa9b468fc196954c87b0933090b00ffbacd4cb7bd`  
		Last Modified: Sat, 31 Aug 2024 02:36:29 GMT  
		Size: 17.4 MB (17440090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f94c80d7718bd1bbc656205b6b9a90ee074a66d9466f41da567a907abd70f17`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a299e457c645ef0ea5f4f77590cbf1f9bbb149ab3b6d35be1e03c232e21b4298`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb74b37352199c3a76042764443f478982d69b68687aaf3b025bbe890eb8ac3f`  
		Last Modified: Sat, 31 Aug 2024 02:59:25 GMT  
		Size: 31.1 MB (31085763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5e8f63a80e285c25bb4838990371cbc88754639c0329cd9959283425dcc5eb`  
		Last Modified: Sat, 31 Aug 2024 02:59:22 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd31bfeaed307e2701b79ab306d11ba9930bdf53c96eae5d5be586fdd1a56c6`  
		Last Modified: Sat, 31 Aug 2024 02:59:23 GMT  
		Size: 813.3 KB (813274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d571efdeb9bf54898af4e90923d32cc1c04e057a94ef91d1f753564f845bbb3b`  
		Last Modified: Sat, 31 Aug 2024 02:59:23 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2ab762566804d399ae0112a549d382e9e600b6b797048e440647dc4068be0c`  
		Last Modified: Sat, 31 Aug 2024 02:59:24 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:74044b90f011c891b06d80de02d02a56176762bbb679773a6d2446aec14584a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9783a359efa8738da17df08006fa430317809a32da56f2c37fa5ac913f69a720`

```dockerfile
```

-	Layers:
	-	`sha256:da4a7db55dc6e1522447c9d2beba40a94e5e604f7b5975095838d818e014e1b6`  
		Last Modified: Sat, 31 Aug 2024 02:59:20 GMT  
		Size: 2.1 MB (2145337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d69e59b16ea8290aa0ba5b1aff93c6f68ef6c036c9e39e175dec687d048838`  
		Last Modified: Sat, 31 Aug 2024 02:59:20 GMT  
		Size: 30.9 KB (30863 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; s390x

```console
$ docker pull composer@sha256:462905e539aedfd429d5c4c88d0a261f44f9ec753aaf9ef74a5dce9e53f78dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70350912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a560a0380c0f62794aed4a67120e26db5c383f3c4746d40a44174a1365b76e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bee85c5a5fc33ed0d0f61a077ed76c922b87c42c5cb3a4dbba408dd62a64def`  
		Last Modified: Tue, 23 Jul 2024 00:56:03 GMT  
		Size: 3.5 MB (3467756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1505ad7d669e91b715e2a1bc7ec0c52dd53433332ad45653571cbe2c3643d5`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d87c5417e12df9b44287d4f554dd37d0b5b446d100409e5c49a17ac509a5b2`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2c4b161c20f3e37aa088308da3bb1a01ec5125d77c20033c4794149cec443`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 12.5 MB (12502092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c122a67a16e90a3dfd6817a2f8845d6e6a1bc5b93a02733eed109b49ac9ac44e`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b9a37a60aa5eac97b05abfe815776138ce85dc5ba1906d5c9515c50c45b044`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 18.0 MB (17977689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c966b6ee628194de003583de4dd26ad320f0da92fbe22a571ce2a42dff75c605`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32192d5d915f2f8aabf39455fe449c2d46c8d50ae7e98d0de6c301ac1d15f45a`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7f663cd19fdb2482f23a049a2e83117b526da0ad73131e73fcfe4dc5e53635`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 31.6 MB (31612727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c1e4c810b0e1cb879cad0bec7f75826c9040aceeb755690532fc1181d9fb1`  
		Last Modified: Sat, 31 Aug 2024 01:54:05 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d04ad993fbf3f6aa557c5ae6eab0cd4e7337a5a2ea31afe9f9655f2d2f19db`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 1.3 MB (1305226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57acd2fbfc4b9afdbc3e4bb67dc65e135d60a71d7c7cccb3c4cd632f5304c946`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e753b7b604d5e0a37393a583ddea761ff87299164502e1e51222836366efb986`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:dbddd69d1ea80b21d5d1cf1ae9784cf243be1154a4ee3640cd18b92affeb8004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690c598e3d18036cf2a51a0c1cced0c355ddd077ad7da5e9478be8130385646b`

```dockerfile
```

-	Layers:
	-	`sha256:65eb103a793493d81a73a2c0dfb27394094894f3cea1f0821a49dff434207a0b`  
		Last Modified: Sat, 31 Aug 2024 01:54:04 GMT  
		Size: 2.1 MB (2145123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f57bc9ec7e845944ed195006c8e0df013226a85e7956944dcd7240cab5bc2e9f`  
		Last Modified: Sat, 31 Aug 2024 01:54:04 GMT  
		Size: 30.8 KB (30830 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.7`

```console
$ docker pull composer@sha256:a710f61aab1ce8a99c19a4024cf965d3ec937dcc2e153937cabe001d9b4b5db4
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

### `composer:2.7` - linux; amd64

```console
$ docker pull composer@sha256:76a2677544ab9e928c98186b37d4327efd3e74a5b6b0e6cf1c9399624f5d2c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68243059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d70afc6bb36eacbb3d15b53b6aa3afaae51a2eaff9f01721f55c5d9b57921d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Sep 2024 08:44:06 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Sep 2024 08:44:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Sep 2024 08:44:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_VERSION=8.3.11
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 05 Sep 2024 08:44:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Sep 2024 08:44:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15916673af8229814dcc44164d4616a6141bc5b586ae9362e741d64c6e4c91`  
		Last Modified: Sat, 07 Sep 2024 02:15:12 GMT  
		Size: 3.3 MB (3282678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb3258c4c6a46b7e182fa372bfe03ff37fd0fdf7f6894ca97b564fc382d7d4`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e436918c34ed4c536bdbaeace5213a8aaeb796ec65951fe681a10758ae2677`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6c87b6d10c2d5a9226b306e7fc3370cab80f9f41fe049706de7a51f8e1cf5a`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 12.5 MB (12502103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90d2c6f0ff71e78e4e311ebe4b83b2abbe5fdda23eaa28c5711e68b23c578da`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5cf8a88be3fd539ff5a60321e916df9fa78268109a78972d9411217023bf61`  
		Last Modified: Sat, 07 Sep 2024 02:16:52 GMT  
		Size: 17.2 MB (17212749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eea6dbc4cb9e274ad2228dfea58ecabec99b9336c8d528206ce4c41f6724ad`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f889a53b48220a2103d38ac31ed15adb68d8e5de71c03c475792439675576304`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fa61b2c2dec3cde7d7b254fe7cc695f7e1fcb5f9625f6e42c07b4976c2b4bb`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 30.6 MB (30647241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc185b71db015be6ffb966d849004a9b1afd7a3d9099d9ea8d2b743a4a6affc1`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeddc56dcb85f3b58b490f826f2b8a02a323be04c7e85ee4d67c52805fa43f9b`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 949.9 KB (949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77db48088bf9fcafb03ff9e33ceb1a2be151dcd65566c5fb764c0ac5d261e5b8`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01bd6daab7e4f446ad3a64e1bca2a2425cee9a5999a854476f33bbec8ab8f27`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7` - unknown; unknown

```console
$ docker pull composer@sha256:380fdcb085ccb206fec4f4b50b8bcf931391fffd2debdf6b738283b3d47535bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2311f82e2f94a4859282c18dbd009a3b9cf910062b4ac4f0a35d53f631178a75`

```dockerfile
```

-	Layers:
	-	`sha256:2502d4bff665dce0aa9952c0fd0a09899110a082f8081b55c899663df32d7c53`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 2.1 MB (2147466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3de91917cccb756e8648efe06ec60e26924d4b0093965412f052790c2ec35c`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 31.1 KB (31131 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.7` - linux; arm variant v6

```console
$ docker pull composer@sha256:c9de0c54c9ad664ec3718bd74409988036df84f052f65ae5a844237837975b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68494557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087f2f76d1a94a9bcc3555f5f1857ae64bf69071de81794c4e05e3d2d9565d82`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:16:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:16:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:16:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:16:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:16:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:16:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:16:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:16:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 22:44:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 19:18:35 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 19:18:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 19:18:35 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 19:18:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 19:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 19:23:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 19:23:08 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 19:23:10 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 19:23:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 19:23:11 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b041a1a670328abed5fe2b73e068aba477e969ddbfe65c606c8054a4c36067b2`  
		Last Modified: Tue, 23 Jul 2024 01:00:35 GMT  
		Size: 3.3 MB (3263638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51daa6109cd19af541c6fc2600ad5a2f2382e50d3938e2b51f30d24df583fee`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b57c8706e4f06f42a10294d5c9eef985613e48298dedb390c6e6816b60a8f78`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b27cb594dc713e8223f5363b7505f762ad934cbf1c4f47ed7885c05db8e13`  
		Last Modified: Fri, 30 Aug 2024 20:20:12 GMT  
		Size: 12.5 MB (12502099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22237d0261563edb9ca222f6a36c5e175cf1d62c16f38e41755982d955f0e39c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ea243fc20547ec3f93ecbe653822d8a49a7c9c61fd5b7ad229cf6ee331209`  
		Last Modified: Fri, 30 Aug 2024 20:20:15 GMT  
		Size: 16.4 MB (16360114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a08c99e5b1cb1537070b37b1f8f3c78a107be7dd6efdd3a197aa7867d3d7a5c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68481b9e1f3b14557aa8d598c31b8ec7b735f77a5aeac9431ef7b69560d46a92`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c939352561246c630164d6835a0997969adc47f5e678a95dc31e21f57e94926d`  
		Last Modified: Fri, 30 Aug 2024 21:19:20 GMT  
		Size: 29.5 MB (29450758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f957f60156f9b6e900c9f3e132d2e377afa2f2d79dd2350288d3c3cf994fc2`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f354e7435ab3ecb4dc85feb20065dcc85c5b6bdc8e73172c0c130f2ae7cd9`  
		Last Modified: Thu, 05 Sep 2024 22:03:17 GMT  
		Size: 3.5 MB (3528377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12ece5c7e8ab6982a7044cbac04f6e5410efdba180cf3f82d3664a6a5b17b46`  
		Last Modified: Thu, 05 Sep 2024 22:03:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1259f25d9b072394ffbf557569b235c7044742bd33a81a9bfae78d674251acfe`  
		Last Modified: Thu, 05 Sep 2024 22:03:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7` - unknown; unknown

```console
$ docker pull composer@sha256:9e633785fdb4d8d10f84cec08db3b6f89fb96447cc0173e95e9184513e42af7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (30975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3adde16d5c6cafefdabe56b377da4b9d3bff02923e59c6e8c1b1e3adadc299`

```dockerfile
```

-	Layers:
	-	`sha256:686a058a7390a9266296d88cc6c40607dd67ef5b59d5e5281a954da2c53de8c9`  
		Last Modified: Thu, 05 Sep 2024 22:03:16 GMT  
		Size: 31.0 KB (30975 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.7` - linux; arm variant v7

```console
$ docker pull composer@sha256:3bbff8da1174ec04349fa78e7ff4738c90ead0b737dd94018dace167d8b85b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66402051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df778fccceef1a7ad544eaff20cdf5cba33ef4ef9612f94e6d77290d4f2e8ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:31:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:31:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:31:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:31:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:31:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:01:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:38:44 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:38:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:38:45 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:38:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:38:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:41:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:41:37 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:41:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:41:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:41:38 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57db3d4836535044109c42cf341df21ab1def6a06fecbaf98ffac833b47f15b`  
		Last Modified: Tue, 23 Jul 2024 01:14:20 GMT  
		Size: 3.1 MB (3073093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991e70be4838afae3979e2bef4b2a7682dffac44793431e072ffbc9fc1686e5`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967a6fef2cedd5f47096963a74875b542f5e4f6667543712aa16505b281dcf7`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c472efc6552ca3c22ddd3afc3423433498a05fa5b26d79a2c74d9c71a5db0515`  
		Last Modified: Fri, 30 Aug 2024 21:50:47 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227ac46a3f3d5c7590120d9f555b6439500ed7212cdfe872e2850b122dc0be1`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba069329678371ed2d3ebd6d6b31019c124d7b205dd0cbc451d0f894c48081d1`  
		Last Modified: Fri, 30 Aug 2024 21:50:49 GMT  
		Size: 15.3 MB (15303131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f1b71f79757d6cb7ae12dc0d78c803efa304cf2be041b5e150fa74c97255c4`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da1f4159b65619170a1816f8957041566fec819f4092f532a9be4fae0766e2`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590a47b24d3ac1c6d1e93d41854d378374a6915b7752990a9bee3fc8716f4c34`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 29.1 MB (29073898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a7d4062ccea4fdf5ed8de172dbc9d1db681bcd5b390a4ffcb54fead69672`  
		Last Modified: Sat, 31 Aug 2024 02:31:06 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ad76e191ec614b29590aed98f8511a696131750ba8ef90780b12d7c01e6a32`  
		Last Modified: Fri, 06 Sep 2024 05:23:13 GMT  
		Size: 3.3 MB (3330474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e96125ef27271af0631684d5f71f871a29af21f239006963b59523149e60154`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4d0f7be48b8b2a1f66d091203ba34585babec9ea0a242b20f051e2e6a4153c`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7` - unknown; unknown

```console
$ docker pull composer@sha256:cf965cc496769a6d89a79df4f86c9511cdcfc4fae3d1812ee9c0d17a3350f139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414062359f838bcb24d9ae63386a189ce994a98cdc69f5668a083cc43fbe8f33`

```dockerfile
```

-	Layers:
	-	`sha256:06e04688ebe91d0536813dbc53e26f8ef0775ca460042a866ea8fa8a0ca3fa88`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 2.1 MB (2147787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38503d9dfee385b915286c453838f2d94fed6d661d99d2d083ba0ff7fe268092`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 31.2 KB (31230 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.7` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:b869809691619076c257df807eea0a48aaa51d4e429db786ea735884edc778f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73242776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe18a77bd397705e87bd4ec8268d8233aada7eb48bf2f1ef4c35f3f556be535`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:30:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 23:30:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 23:30:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 23:30:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:50:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 19:56:37 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 19:56:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 19:56:37 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 19:56:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 19:56:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:01:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:01:00 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:01:01 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:01:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:01:01 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f069fb86c015646c4497d6fa3beaf8bd3f9f04d8f77a1a865ff47fc9922c27e3`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 3.3 MB (3324720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298458c1fe168646ba7edf3e03804ff1a01f1fac6b41ef2a94ef5bf333311f2b`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71c5e072e5141e780c5bbd4c1e2a34f9248a4b4a0983717a6c98be7560b899`  
		Last Modified: Tue, 23 Jul 2024 02:00:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eb94c855017ccb6e05ed05ab6089ac13ef31b7c2c4f68ac1aa7871f5e50f05`  
		Last Modified: Fri, 30 Aug 2024 21:23:23 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7788e2267fee70d1ccfd7ae5b7bdc051ea44976ed82a8dcce577cc9b0c8d6a`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d38576090a615f5e4f5732ed6ca99ac0f1721a6ed93df8c2a86c7b7d9a2539`  
		Last Modified: Fri, 30 Aug 2024 21:23:24 GMT  
		Size: 17.9 MB (17857930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb7c168c56b49540c07601d6cab358cafc4340a5f0dae6ef942aff3d828fa14`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f44bd4d0b7f587d16c7c70ac77c4a0a8d22a607399c38b6eb5ae4d5cd7d78b3`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 19.5 KB (19488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee874a6d0bc05b34617460b975ed3786bc3fb8320c0a847a478a06d8137ad3c`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 31.2 MB (31163203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab4e408f7d446ed2ebe4e87b8fc9ac34818639a1d6bd84e5e45a06bc7106695`  
		Last Modified: Sat, 31 Aug 2024 01:35:35 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471d29effa5f2eb83b2f0a7046bbe384437b0fdb94371156ddb902fcbae0c57d`  
		Last Modified: Thu, 05 Sep 2024 22:04:55 GMT  
		Size: 4.3 MB (4283528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93f6d78874f59727226d8b0f5d434289cfddd237bf281ce65ee61cbf48aed3d`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3de2366387cc3110c6029a23f39e799fee5b9af39ca4d6fd24935000537d74e`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7` - unknown; unknown

```console
$ docker pull composer@sha256:f671ade9cf000abfebed98797ba31a95e4b9e7c9a66abd8809ee449566a48cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c03772129e8978c8d7e3bf6d6b7628e243c359bf386c62625b423c670dee84`

```dockerfile
```

-	Layers:
	-	`sha256:5b2817a406bb8bbe15f0e63d07de7c7bc61dd5a16b2fa9a5f81bd6eb82393395`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 2.1 MB (2147617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45290e8d87ce7431906c7c10fa965bc3587af107940530164650c6eb891c40a5`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 31.4 KB (31435 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.7` - linux; 386

```console
$ docker pull composer@sha256:8312b8751b142b0a015dd9590e85278dc3a744c583f26917cc298274c257f717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49192907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19f9445ebcafde08291d1740ca48717f04d634fcfcfe719397192e34b54f346`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Sep 2024 08:44:06 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Sep 2024 08:44:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Sep 2024 08:44:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_VERSION=8.3.11
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 05 Sep 2024 08:44:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Sep 2024 08:44:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17866811de1cdb9710f37a522dde62051d068230716118d22b6b987216e037ef`  
		Last Modified: Sat, 07 Sep 2024 01:49:46 GMT  
		Size: 3.3 MB (3331976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513ca5d3e6e64e8e064f1b178ad39b5d375a65559181a7f4964c9471461ba8f`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90338393c7a779c5576927d742c98b6841aa39aa84fe1b137708bd8f4d0ae68e`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20961f4e3b99e90c174a4f87f2af7f93ae78322283dde5d669a4c76c2c3cebd8`  
		Last Modified: Sat, 07 Sep 2024 01:51:38 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42171d227440b8721b3056f4e4f3a4916baf777d09c6f844c8f8056fbc70c42`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dabae8861b481fcfb1e16733b346f40d06038d6a5cd82cceb87bd8c3ee3ecd`  
		Last Modified: Sat, 07 Sep 2024 01:51:42 GMT  
		Size: 17.7 MB (17656052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d394881214b919e13be7206b61f0f6743c86558096cefb3ea4f89e68ad0c8d2`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357eacc586709ee7f5d5f8c1962caf6215d0ea35d2d9ed17c68628bfff98004d`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ceaf7eb2dca105a56d8088ae20e32e04da87d85e9f3f09128670d827655bf7`  
		Last Modified: Sat, 07 Sep 2024 02:57:36 GMT  
		Size: 11.3 MB (11281268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f027e9fbe9cf77b0fce954ce8fbd052e739b2ff93e8da28371a6d5e94a0e2cbe`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26346643aadaa9a17917fd876775e1dd782dee44797eb19fffa15a6041861dba`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 927.8 KB (927779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afa2275f20f7dd58d5cfed55223d78856a410a10571131099c93c96790fe01e`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731311864dda11557754fea1b4d013140d3888f5ae6a9ebdf49ab6817c32db2`  
		Last Modified: Sat, 07 Sep 2024 02:57:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7` - unknown; unknown

```console
$ docker pull composer@sha256:b7ead7cbc4ea95097c0765936f81f348282e2988e0a38da34af421c9e0fb9b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.2 KB (452233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15ae0e3c0095d9fc4067abeed65ebd7323312c0802e512309d7ef6a6f1f3441`

```dockerfile
```

-	Layers:
	-	`sha256:79ad4e506a516203b8ec59310d39679f1819e1ddf6e4eeaf2e829bc8e6c8f719`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 421.1 KB (421135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a25d9908a80b2d5c7108c6c649b0ce7ac73d06c70f6bc5f3f94f655c81dc34`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 31.1 KB (31098 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.7` - linux; ppc64le

```console
$ docker pull composer@sha256:bc8587a56d445402ad83ed08b4fa4547ecd680b4c018d5ef5b80cd9c71a89ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73690032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57f38462579c8ced3b7f7847a77a0dfd7b8410d48af550afb90fe24f76fe2d3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 21:55:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 21:55:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 21:55:11 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 21:55:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 21:55:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 21:55:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 21:55:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 21:55:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 22:13:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:31:39 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:31:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:31:39 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:31:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:31:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:34:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:34:17 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:34:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:34:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:34:20 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3b3ac21bbea54c953ea1f2d18929d69c201c50acbb70a6157944a16d881644`  
		Last Modified: Mon, 22 Jul 2024 23:40:54 GMT  
		Size: 3.4 MB (3400973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab89bd2c65997355b0f8d6c170e8ada77fc5d87ae04f4e525032aad1d1c519`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9ea05d06440c67793ed8359925d4dcf5e15c76e0e78b5d20fad34b553a253f`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512248dd3ed75a17d321bc96ddef6ecae12695170f3a768584fe46b6fec8b581`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f97a91111a935f934126b9b5e843f52e61ce5a0d268da80ce88a7e9637e46b`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e963895597cd82f3e2562f1193ef440f635d77e3ce7d65a2d29a5f952d1ee09`  
		Last Modified: Fri, 30 Aug 2024 21:39:34 GMT  
		Size: 18.8 MB (18776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd6fc58c5780a4980b31da9f3258387aa34ad2ae9aa0edd08d9a5b90aaea95`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb9ba050d100c1c32d4f5b3c3975a0ebb302f1b9d8fb6c9b5c21dd9b7279d50`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b5ba9d088f76b4f58ad424d166ff3328d5c7af19e83e9bf897da73af9c27e5`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 31.7 MB (31678361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980ba58d45390240ed5b943d865d41bc6ceaa59661e4c900661678594a767b3f`  
		Last Modified: Sat, 31 Aug 2024 02:19:13 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc9d7e6a424d5f21f867ce20dd0412a843bc862bbfa52a72c8fec70a91e9820`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 3.7 MB (3735823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c66371ed6bb411621f796beb53658e55775622499a2e3cb680d11aef50836b`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e195cdfe80738ab413e61c2c78199d6ce718a1cc53c0e4009150b0b9e080233e`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7` - unknown; unknown

```console
$ docker pull composer@sha256:efab4d657adc63f8f5ec446309628d53ae9c1619621d59baffac7e8848599a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c0df070a167df4c3900ea024b5889a7c16cd645bc574984ff0d023102c384e`

```dockerfile
```

-	Layers:
	-	`sha256:05f796980c4a0d5999b42b6362b266f43d3c281b065548ce493711bf6784ca18`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 2.1 MB (2146021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa61ab546b7b90ac789c29cb289298af77d133d2b3e4a9c4730de6952b1c4663`  
		Last Modified: Thu, 05 Sep 2024 23:26:45 GMT  
		Size: 31.2 KB (31175 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.7` - linux; riscv64

```console
$ docker pull composer@sha256:bf673fa5bf49303d1284204bbbaebf69ce04845f99f9e2c2306fba331c9dd5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71357432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb65159493a0c7780698a7df08edba41813cfcb4b96941d9f076a7c58890f68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:40:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:40:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:40:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:40:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:40:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:40:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:40:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:40:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 01:15:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 22:01:05 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 22:01:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 22:01:06 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 22:01:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 22:01:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 22:49:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 22:49:31 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 22:49:37 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 22:49:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 22:49:39 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2d0e03d7a4d4766a64c04a50abfb02e217be153dd68888273b46568c4cac04`  
		Last Modified: Tue, 23 Jul 2024 12:29:02 GMT  
		Size: 3.4 MB (3397181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56268c2d820d6bf5bbf0e86c5bc55e50edc209a552c0844c6a9f787a880a2c6`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d3b9188b0e4a61167b2493ce280347bad9dfe72e9ecf4c18c5572f2cb6719`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d23ac9bf2deff71588cfd4b3f47c1364b66f45e05cb5d2518adb6a0396df50`  
		Last Modified: Sat, 31 Aug 2024 02:36:17 GMT  
		Size: 12.5 MB (12502106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869116b457f2e31f8fdb3c69a1bab7e4c51f76c00076389e0239f62c730528cf`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b247cb48214eaf57917fe6fa9b468fc196954c87b0933090b00ffbacd4cb7bd`  
		Last Modified: Sat, 31 Aug 2024 02:36:29 GMT  
		Size: 17.4 MB (17440090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f94c80d7718bd1bbc656205b6b9a90ee074a66d9466f41da567a907abd70f17`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a299e457c645ef0ea5f4f77590cbf1f9bbb149ab3b6d35be1e03c232e21b4298`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb74b37352199c3a76042764443f478982d69b68687aaf3b025bbe890eb8ac3f`  
		Last Modified: Sat, 31 Aug 2024 02:59:25 GMT  
		Size: 31.1 MB (31085763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5e8f63a80e285c25bb4838990371cbc88754639c0329cd9959283425dcc5eb`  
		Last Modified: Sat, 31 Aug 2024 02:59:22 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478ce11c08f84b8b7ef024ae95064e16cbf6ca32a8a9cd7f410dc361463eca95`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 3.5 MB (3537231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ae820656a3026d75cd896ddfb8c712b63434f5e78ca547f38a87da2d57760c`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eab9f887e2c0cae13ef41f6342ed9ff724873ce2065692a1e4cebd9660f3875`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7` - unknown; unknown

```console
$ docker pull composer@sha256:8e1dca6e31e5eb0d3cdf8a537041418b35bcdadfd2b2c9a2a2647f0ef9f6359b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0580b08ef8ef61d4939757c82ce29de24638ed0fd241ed6af77bf60e5ef3b4`

```dockerfile
```

-	Layers:
	-	`sha256:31a0c112e4561f1142fe90ba25be7145131a0daa0115e16bef20cb4a5e4e596e`  
		Last Modified: Thu, 05 Sep 2024 22:07:28 GMT  
		Size: 2.1 MB (2145637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc47b1511335b2b61390c61f237078daae30b87e51e2d5bbd0c89f5d6e329459`  
		Last Modified: Thu, 05 Sep 2024 22:07:28 GMT  
		Size: 31.2 KB (31176 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.7` - linux; s390x

```console
$ docker pull composer@sha256:1df015ec24cd23ae2d860ff918845a6067da37bae3e377cc24a7308496b987d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73197813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b68d12485ac34ba23fca979b223aa60d4a14122500e410ef718ce17654bacc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:33:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:33:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:33:37 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:33:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:33:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:33:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:33:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:33:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:08:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:02:04 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:02:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:02:04 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:02:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:02:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:05:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:05:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:05:07 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:05:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:05:07 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bee85c5a5fc33ed0d0f61a077ed76c922b87c42c5cb3a4dbba408dd62a64def`  
		Last Modified: Tue, 23 Jul 2024 00:56:03 GMT  
		Size: 3.5 MB (3467756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1505ad7d669e91b715e2a1bc7ec0c52dd53433332ad45653571cbe2c3643d5`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d87c5417e12df9b44287d4f554dd37d0b5b446d100409e5c49a17ac509a5b2`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2c4b161c20f3e37aa088308da3bb1a01ec5125d77c20033c4794149cec443`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 12.5 MB (12502092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c122a67a16e90a3dfd6817a2f8845d6e6a1bc5b93a02733eed109b49ac9ac44e`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b9a37a60aa5eac97b05abfe815776138ce85dc5ba1906d5c9515c50c45b044`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 18.0 MB (17977689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c966b6ee628194de003583de4dd26ad320f0da92fbe22a571ce2a42dff75c605`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32192d5d915f2f8aabf39455fe449c2d46c8d50ae7e98d0de6c301ac1d15f45a`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7f663cd19fdb2482f23a049a2e83117b526da0ad73131e73fcfe4dc5e53635`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 31.6 MB (31612727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c1e4c810b0e1cb879cad0bec7f75826c9040aceeb755690532fc1181d9fb1`  
		Last Modified: Sat, 31 Aug 2024 01:54:05 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5bd271a220b3b436116cae2105bb3a177c48e043c4dd3fd0d6ed9ab8015848`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 4.2 MB (4152127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d7d905b04205f119efc606778b4f1d82a6e2e5d5e3655790529aae14e90ba6`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b7918b5450a89e93a44512990195960e1a4e0502cb49f82ba3a78eba9350ab`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7` - unknown; unknown

```console
$ docker pull composer@sha256:ec53877138e3fcd05768b1dc4bb3b19d3728790af26c97b2baf9bf5613b09c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8541813da59e7a04600e48f87a9ab19275d55e61cfbf734906f1bc9ebf5db813`

```dockerfile
```

-	Layers:
	-	`sha256:9e395b5be33bfe7fe5010adb29de378bdee4b6157103397beac3ac320251440a`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 2.1 MB (2145417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ee5098920bf84b8da06f1004dff77d5f0c006fb1cab68bc7718d23ffd153f8`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 31.1 KB (31134 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.7.9`

```console
$ docker pull composer@sha256:a710f61aab1ce8a99c19a4024cf965d3ec937dcc2e153937cabe001d9b4b5db4
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

### `composer:2.7.9` - linux; amd64

```console
$ docker pull composer@sha256:76a2677544ab9e928c98186b37d4327efd3e74a5b6b0e6cf1c9399624f5d2c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68243059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d70afc6bb36eacbb3d15b53b6aa3afaae51a2eaff9f01721f55c5d9b57921d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Sep 2024 08:44:06 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Sep 2024 08:44:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Sep 2024 08:44:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_VERSION=8.3.11
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 05 Sep 2024 08:44:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Sep 2024 08:44:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15916673af8229814dcc44164d4616a6141bc5b586ae9362e741d64c6e4c91`  
		Last Modified: Sat, 07 Sep 2024 02:15:12 GMT  
		Size: 3.3 MB (3282678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb3258c4c6a46b7e182fa372bfe03ff37fd0fdf7f6894ca97b564fc382d7d4`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e436918c34ed4c536bdbaeace5213a8aaeb796ec65951fe681a10758ae2677`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6c87b6d10c2d5a9226b306e7fc3370cab80f9f41fe049706de7a51f8e1cf5a`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 12.5 MB (12502103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90d2c6f0ff71e78e4e311ebe4b83b2abbe5fdda23eaa28c5711e68b23c578da`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5cf8a88be3fd539ff5a60321e916df9fa78268109a78972d9411217023bf61`  
		Last Modified: Sat, 07 Sep 2024 02:16:52 GMT  
		Size: 17.2 MB (17212749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eea6dbc4cb9e274ad2228dfea58ecabec99b9336c8d528206ce4c41f6724ad`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f889a53b48220a2103d38ac31ed15adb68d8e5de71c03c475792439675576304`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fa61b2c2dec3cde7d7b254fe7cc695f7e1fcb5f9625f6e42c07b4976c2b4bb`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 30.6 MB (30647241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc185b71db015be6ffb966d849004a9b1afd7a3d9099d9ea8d2b743a4a6affc1`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeddc56dcb85f3b58b490f826f2b8a02a323be04c7e85ee4d67c52805fa43f9b`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 949.9 KB (949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77db48088bf9fcafb03ff9e33ceb1a2be151dcd65566c5fb764c0ac5d261e5b8`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01bd6daab7e4f446ad3a64e1bca2a2425cee9a5999a854476f33bbec8ab8f27`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7.9` - unknown; unknown

```console
$ docker pull composer@sha256:380fdcb085ccb206fec4f4b50b8bcf931391fffd2debdf6b738283b3d47535bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2311f82e2f94a4859282c18dbd009a3b9cf910062b4ac4f0a35d53f631178a75`

```dockerfile
```

-	Layers:
	-	`sha256:2502d4bff665dce0aa9952c0fd0a09899110a082f8081b55c899663df32d7c53`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 2.1 MB (2147466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3de91917cccb756e8648efe06ec60e26924d4b0093965412f052790c2ec35c`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 31.1 KB (31131 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.7.9` - linux; arm variant v6

```console
$ docker pull composer@sha256:c9de0c54c9ad664ec3718bd74409988036df84f052f65ae5a844237837975b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68494557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087f2f76d1a94a9bcc3555f5f1857ae64bf69071de81794c4e05e3d2d9565d82`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:16:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:16:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:16:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:16:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:16:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:16:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:16:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:16:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 22:44:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 19:18:35 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 19:18:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 19:18:35 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 19:18:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 19:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 19:23:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 19:23:08 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 19:23:10 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 19:23:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 19:23:11 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b041a1a670328abed5fe2b73e068aba477e969ddbfe65c606c8054a4c36067b2`  
		Last Modified: Tue, 23 Jul 2024 01:00:35 GMT  
		Size: 3.3 MB (3263638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51daa6109cd19af541c6fc2600ad5a2f2382e50d3938e2b51f30d24df583fee`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b57c8706e4f06f42a10294d5c9eef985613e48298dedb390c6e6816b60a8f78`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b27cb594dc713e8223f5363b7505f762ad934cbf1c4f47ed7885c05db8e13`  
		Last Modified: Fri, 30 Aug 2024 20:20:12 GMT  
		Size: 12.5 MB (12502099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22237d0261563edb9ca222f6a36c5e175cf1d62c16f38e41755982d955f0e39c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ea243fc20547ec3f93ecbe653822d8a49a7c9c61fd5b7ad229cf6ee331209`  
		Last Modified: Fri, 30 Aug 2024 20:20:15 GMT  
		Size: 16.4 MB (16360114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a08c99e5b1cb1537070b37b1f8f3c78a107be7dd6efdd3a197aa7867d3d7a5c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68481b9e1f3b14557aa8d598c31b8ec7b735f77a5aeac9431ef7b69560d46a92`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c939352561246c630164d6835a0997969adc47f5e678a95dc31e21f57e94926d`  
		Last Modified: Fri, 30 Aug 2024 21:19:20 GMT  
		Size: 29.5 MB (29450758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f957f60156f9b6e900c9f3e132d2e377afa2f2d79dd2350288d3c3cf994fc2`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f354e7435ab3ecb4dc85feb20065dcc85c5b6bdc8e73172c0c130f2ae7cd9`  
		Last Modified: Thu, 05 Sep 2024 22:03:17 GMT  
		Size: 3.5 MB (3528377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12ece5c7e8ab6982a7044cbac04f6e5410efdba180cf3f82d3664a6a5b17b46`  
		Last Modified: Thu, 05 Sep 2024 22:03:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1259f25d9b072394ffbf557569b235c7044742bd33a81a9bfae78d674251acfe`  
		Last Modified: Thu, 05 Sep 2024 22:03:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7.9` - unknown; unknown

```console
$ docker pull composer@sha256:9e633785fdb4d8d10f84cec08db3b6f89fb96447cc0173e95e9184513e42af7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (30975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3adde16d5c6cafefdabe56b377da4b9d3bff02923e59c6e8c1b1e3adadc299`

```dockerfile
```

-	Layers:
	-	`sha256:686a058a7390a9266296d88cc6c40607dd67ef5b59d5e5281a954da2c53de8c9`  
		Last Modified: Thu, 05 Sep 2024 22:03:16 GMT  
		Size: 31.0 KB (30975 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.7.9` - linux; arm variant v7

```console
$ docker pull composer@sha256:3bbff8da1174ec04349fa78e7ff4738c90ead0b737dd94018dace167d8b85b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66402051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df778fccceef1a7ad544eaff20cdf5cba33ef4ef9612f94e6d77290d4f2e8ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:31:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:31:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:31:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:31:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:31:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:01:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:38:44 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:38:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:38:45 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:38:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:38:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:41:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:41:37 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:41:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:41:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:41:38 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57db3d4836535044109c42cf341df21ab1def6a06fecbaf98ffac833b47f15b`  
		Last Modified: Tue, 23 Jul 2024 01:14:20 GMT  
		Size: 3.1 MB (3073093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991e70be4838afae3979e2bef4b2a7682dffac44793431e072ffbc9fc1686e5`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967a6fef2cedd5f47096963a74875b542f5e4f6667543712aa16505b281dcf7`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c472efc6552ca3c22ddd3afc3423433498a05fa5b26d79a2c74d9c71a5db0515`  
		Last Modified: Fri, 30 Aug 2024 21:50:47 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227ac46a3f3d5c7590120d9f555b6439500ed7212cdfe872e2850b122dc0be1`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba069329678371ed2d3ebd6d6b31019c124d7b205dd0cbc451d0f894c48081d1`  
		Last Modified: Fri, 30 Aug 2024 21:50:49 GMT  
		Size: 15.3 MB (15303131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f1b71f79757d6cb7ae12dc0d78c803efa304cf2be041b5e150fa74c97255c4`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da1f4159b65619170a1816f8957041566fec819f4092f532a9be4fae0766e2`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590a47b24d3ac1c6d1e93d41854d378374a6915b7752990a9bee3fc8716f4c34`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 29.1 MB (29073898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a7d4062ccea4fdf5ed8de172dbc9d1db681bcd5b390a4ffcb54fead69672`  
		Last Modified: Sat, 31 Aug 2024 02:31:06 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ad76e191ec614b29590aed98f8511a696131750ba8ef90780b12d7c01e6a32`  
		Last Modified: Fri, 06 Sep 2024 05:23:13 GMT  
		Size: 3.3 MB (3330474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e96125ef27271af0631684d5f71f871a29af21f239006963b59523149e60154`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4d0f7be48b8b2a1f66d091203ba34585babec9ea0a242b20f051e2e6a4153c`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7.9` - unknown; unknown

```console
$ docker pull composer@sha256:cf965cc496769a6d89a79df4f86c9511cdcfc4fae3d1812ee9c0d17a3350f139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414062359f838bcb24d9ae63386a189ce994a98cdc69f5668a083cc43fbe8f33`

```dockerfile
```

-	Layers:
	-	`sha256:06e04688ebe91d0536813dbc53e26f8ef0775ca460042a866ea8fa8a0ca3fa88`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 2.1 MB (2147787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38503d9dfee385b915286c453838f2d94fed6d661d99d2d083ba0ff7fe268092`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 31.2 KB (31230 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.7.9` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:b869809691619076c257df807eea0a48aaa51d4e429db786ea735884edc778f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73242776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe18a77bd397705e87bd4ec8268d8233aada7eb48bf2f1ef4c35f3f556be535`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:30:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 23:30:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 23:30:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 23:30:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:50:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 19:56:37 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 19:56:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 19:56:37 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 19:56:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 19:56:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:01:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:01:00 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:01:01 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:01:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:01:01 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f069fb86c015646c4497d6fa3beaf8bd3f9f04d8f77a1a865ff47fc9922c27e3`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 3.3 MB (3324720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298458c1fe168646ba7edf3e03804ff1a01f1fac6b41ef2a94ef5bf333311f2b`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71c5e072e5141e780c5bbd4c1e2a34f9248a4b4a0983717a6c98be7560b899`  
		Last Modified: Tue, 23 Jul 2024 02:00:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eb94c855017ccb6e05ed05ab6089ac13ef31b7c2c4f68ac1aa7871f5e50f05`  
		Last Modified: Fri, 30 Aug 2024 21:23:23 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7788e2267fee70d1ccfd7ae5b7bdc051ea44976ed82a8dcce577cc9b0c8d6a`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d38576090a615f5e4f5732ed6ca99ac0f1721a6ed93df8c2a86c7b7d9a2539`  
		Last Modified: Fri, 30 Aug 2024 21:23:24 GMT  
		Size: 17.9 MB (17857930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb7c168c56b49540c07601d6cab358cafc4340a5f0dae6ef942aff3d828fa14`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f44bd4d0b7f587d16c7c70ac77c4a0a8d22a607399c38b6eb5ae4d5cd7d78b3`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 19.5 KB (19488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee874a6d0bc05b34617460b975ed3786bc3fb8320c0a847a478a06d8137ad3c`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 31.2 MB (31163203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab4e408f7d446ed2ebe4e87b8fc9ac34818639a1d6bd84e5e45a06bc7106695`  
		Last Modified: Sat, 31 Aug 2024 01:35:35 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471d29effa5f2eb83b2f0a7046bbe384437b0fdb94371156ddb902fcbae0c57d`  
		Last Modified: Thu, 05 Sep 2024 22:04:55 GMT  
		Size: 4.3 MB (4283528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93f6d78874f59727226d8b0f5d434289cfddd237bf281ce65ee61cbf48aed3d`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3de2366387cc3110c6029a23f39e799fee5b9af39ca4d6fd24935000537d74e`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7.9` - unknown; unknown

```console
$ docker pull composer@sha256:f671ade9cf000abfebed98797ba31a95e4b9e7c9a66abd8809ee449566a48cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c03772129e8978c8d7e3bf6d6b7628e243c359bf386c62625b423c670dee84`

```dockerfile
```

-	Layers:
	-	`sha256:5b2817a406bb8bbe15f0e63d07de7c7bc61dd5a16b2fa9a5f81bd6eb82393395`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 2.1 MB (2147617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45290e8d87ce7431906c7c10fa965bc3587af107940530164650c6eb891c40a5`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 31.4 KB (31435 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.7.9` - linux; 386

```console
$ docker pull composer@sha256:8312b8751b142b0a015dd9590e85278dc3a744c583f26917cc298274c257f717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49192907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19f9445ebcafde08291d1740ca48717f04d634fcfcfe719397192e34b54f346`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Sep 2024 08:44:06 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Sep 2024 08:44:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Sep 2024 08:44:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_VERSION=8.3.11
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 05 Sep 2024 08:44:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Sep 2024 08:44:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17866811de1cdb9710f37a522dde62051d068230716118d22b6b987216e037ef`  
		Last Modified: Sat, 07 Sep 2024 01:49:46 GMT  
		Size: 3.3 MB (3331976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513ca5d3e6e64e8e064f1b178ad39b5d375a65559181a7f4964c9471461ba8f`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90338393c7a779c5576927d742c98b6841aa39aa84fe1b137708bd8f4d0ae68e`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20961f4e3b99e90c174a4f87f2af7f93ae78322283dde5d669a4c76c2c3cebd8`  
		Last Modified: Sat, 07 Sep 2024 01:51:38 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42171d227440b8721b3056f4e4f3a4916baf777d09c6f844c8f8056fbc70c42`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dabae8861b481fcfb1e16733b346f40d06038d6a5cd82cceb87bd8c3ee3ecd`  
		Last Modified: Sat, 07 Sep 2024 01:51:42 GMT  
		Size: 17.7 MB (17656052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d394881214b919e13be7206b61f0f6743c86558096cefb3ea4f89e68ad0c8d2`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357eacc586709ee7f5d5f8c1962caf6215d0ea35d2d9ed17c68628bfff98004d`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ceaf7eb2dca105a56d8088ae20e32e04da87d85e9f3f09128670d827655bf7`  
		Last Modified: Sat, 07 Sep 2024 02:57:36 GMT  
		Size: 11.3 MB (11281268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f027e9fbe9cf77b0fce954ce8fbd052e739b2ff93e8da28371a6d5e94a0e2cbe`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26346643aadaa9a17917fd876775e1dd782dee44797eb19fffa15a6041861dba`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 927.8 KB (927779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afa2275f20f7dd58d5cfed55223d78856a410a10571131099c93c96790fe01e`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731311864dda11557754fea1b4d013140d3888f5ae6a9ebdf49ab6817c32db2`  
		Last Modified: Sat, 07 Sep 2024 02:57:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7.9` - unknown; unknown

```console
$ docker pull composer@sha256:b7ead7cbc4ea95097c0765936f81f348282e2988e0a38da34af421c9e0fb9b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.2 KB (452233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15ae0e3c0095d9fc4067abeed65ebd7323312c0802e512309d7ef6a6f1f3441`

```dockerfile
```

-	Layers:
	-	`sha256:79ad4e506a516203b8ec59310d39679f1819e1ddf6e4eeaf2e829bc8e6c8f719`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 421.1 KB (421135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a25d9908a80b2d5c7108c6c649b0ce7ac73d06c70f6bc5f3f94f655c81dc34`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 31.1 KB (31098 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.7.9` - linux; ppc64le

```console
$ docker pull composer@sha256:bc8587a56d445402ad83ed08b4fa4547ecd680b4c018d5ef5b80cd9c71a89ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73690032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57f38462579c8ced3b7f7847a77a0dfd7b8410d48af550afb90fe24f76fe2d3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 21:55:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 21:55:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 21:55:11 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 21:55:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 21:55:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 21:55:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 21:55:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 21:55:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 22:13:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:31:39 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:31:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:31:39 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:31:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:31:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:34:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:34:17 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:34:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:34:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:34:20 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3b3ac21bbea54c953ea1f2d18929d69c201c50acbb70a6157944a16d881644`  
		Last Modified: Mon, 22 Jul 2024 23:40:54 GMT  
		Size: 3.4 MB (3400973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab89bd2c65997355b0f8d6c170e8ada77fc5d87ae04f4e525032aad1d1c519`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9ea05d06440c67793ed8359925d4dcf5e15c76e0e78b5d20fad34b553a253f`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512248dd3ed75a17d321bc96ddef6ecae12695170f3a768584fe46b6fec8b581`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f97a91111a935f934126b9b5e843f52e61ce5a0d268da80ce88a7e9637e46b`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e963895597cd82f3e2562f1193ef440f635d77e3ce7d65a2d29a5f952d1ee09`  
		Last Modified: Fri, 30 Aug 2024 21:39:34 GMT  
		Size: 18.8 MB (18776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd6fc58c5780a4980b31da9f3258387aa34ad2ae9aa0edd08d9a5b90aaea95`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb9ba050d100c1c32d4f5b3c3975a0ebb302f1b9d8fb6c9b5c21dd9b7279d50`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b5ba9d088f76b4f58ad424d166ff3328d5c7af19e83e9bf897da73af9c27e5`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 31.7 MB (31678361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980ba58d45390240ed5b943d865d41bc6ceaa59661e4c900661678594a767b3f`  
		Last Modified: Sat, 31 Aug 2024 02:19:13 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc9d7e6a424d5f21f867ce20dd0412a843bc862bbfa52a72c8fec70a91e9820`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 3.7 MB (3735823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c66371ed6bb411621f796beb53658e55775622499a2e3cb680d11aef50836b`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e195cdfe80738ab413e61c2c78199d6ce718a1cc53c0e4009150b0b9e080233e`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7.9` - unknown; unknown

```console
$ docker pull composer@sha256:efab4d657adc63f8f5ec446309628d53ae9c1619621d59baffac7e8848599a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c0df070a167df4c3900ea024b5889a7c16cd645bc574984ff0d023102c384e`

```dockerfile
```

-	Layers:
	-	`sha256:05f796980c4a0d5999b42b6362b266f43d3c281b065548ce493711bf6784ca18`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 2.1 MB (2146021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa61ab546b7b90ac789c29cb289298af77d133d2b3e4a9c4730de6952b1c4663`  
		Last Modified: Thu, 05 Sep 2024 23:26:45 GMT  
		Size: 31.2 KB (31175 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.7.9` - linux; riscv64

```console
$ docker pull composer@sha256:bf673fa5bf49303d1284204bbbaebf69ce04845f99f9e2c2306fba331c9dd5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71357432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb65159493a0c7780698a7df08edba41813cfcb4b96941d9f076a7c58890f68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:40:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:40:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:40:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:40:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:40:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:40:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:40:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:40:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 01:15:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 22:01:05 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 22:01:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 22:01:06 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 22:01:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 22:01:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 22:49:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 22:49:31 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 22:49:37 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 22:49:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 22:49:39 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2d0e03d7a4d4766a64c04a50abfb02e217be153dd68888273b46568c4cac04`  
		Last Modified: Tue, 23 Jul 2024 12:29:02 GMT  
		Size: 3.4 MB (3397181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56268c2d820d6bf5bbf0e86c5bc55e50edc209a552c0844c6a9f787a880a2c6`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d3b9188b0e4a61167b2493ce280347bad9dfe72e9ecf4c18c5572f2cb6719`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d23ac9bf2deff71588cfd4b3f47c1364b66f45e05cb5d2518adb6a0396df50`  
		Last Modified: Sat, 31 Aug 2024 02:36:17 GMT  
		Size: 12.5 MB (12502106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869116b457f2e31f8fdb3c69a1bab7e4c51f76c00076389e0239f62c730528cf`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b247cb48214eaf57917fe6fa9b468fc196954c87b0933090b00ffbacd4cb7bd`  
		Last Modified: Sat, 31 Aug 2024 02:36:29 GMT  
		Size: 17.4 MB (17440090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f94c80d7718bd1bbc656205b6b9a90ee074a66d9466f41da567a907abd70f17`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a299e457c645ef0ea5f4f77590cbf1f9bbb149ab3b6d35be1e03c232e21b4298`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb74b37352199c3a76042764443f478982d69b68687aaf3b025bbe890eb8ac3f`  
		Last Modified: Sat, 31 Aug 2024 02:59:25 GMT  
		Size: 31.1 MB (31085763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5e8f63a80e285c25bb4838990371cbc88754639c0329cd9959283425dcc5eb`  
		Last Modified: Sat, 31 Aug 2024 02:59:22 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478ce11c08f84b8b7ef024ae95064e16cbf6ca32a8a9cd7f410dc361463eca95`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 3.5 MB (3537231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ae820656a3026d75cd896ddfb8c712b63434f5e78ca547f38a87da2d57760c`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eab9f887e2c0cae13ef41f6342ed9ff724873ce2065692a1e4cebd9660f3875`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7.9` - unknown; unknown

```console
$ docker pull composer@sha256:8e1dca6e31e5eb0d3cdf8a537041418b35bcdadfd2b2c9a2a2647f0ef9f6359b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0580b08ef8ef61d4939757c82ce29de24638ed0fd241ed6af77bf60e5ef3b4`

```dockerfile
```

-	Layers:
	-	`sha256:31a0c112e4561f1142fe90ba25be7145131a0daa0115e16bef20cb4a5e4e596e`  
		Last Modified: Thu, 05 Sep 2024 22:07:28 GMT  
		Size: 2.1 MB (2145637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc47b1511335b2b61390c61f237078daae30b87e51e2d5bbd0c89f5d6e329459`  
		Last Modified: Thu, 05 Sep 2024 22:07:28 GMT  
		Size: 31.2 KB (31176 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.7.9` - linux; s390x

```console
$ docker pull composer@sha256:1df015ec24cd23ae2d860ff918845a6067da37bae3e377cc24a7308496b987d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73197813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b68d12485ac34ba23fca979b223aa60d4a14122500e410ef718ce17654bacc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:33:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:33:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:33:37 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:33:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:33:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:33:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:33:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:33:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:08:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:02:04 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:02:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:02:04 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:02:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:02:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:05:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:05:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:05:07 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:05:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:05:07 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bee85c5a5fc33ed0d0f61a077ed76c922b87c42c5cb3a4dbba408dd62a64def`  
		Last Modified: Tue, 23 Jul 2024 00:56:03 GMT  
		Size: 3.5 MB (3467756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1505ad7d669e91b715e2a1bc7ec0c52dd53433332ad45653571cbe2c3643d5`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d87c5417e12df9b44287d4f554dd37d0b5b446d100409e5c49a17ac509a5b2`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2c4b161c20f3e37aa088308da3bb1a01ec5125d77c20033c4794149cec443`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 12.5 MB (12502092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c122a67a16e90a3dfd6817a2f8845d6e6a1bc5b93a02733eed109b49ac9ac44e`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b9a37a60aa5eac97b05abfe815776138ce85dc5ba1906d5c9515c50c45b044`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 18.0 MB (17977689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c966b6ee628194de003583de4dd26ad320f0da92fbe22a571ce2a42dff75c605`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32192d5d915f2f8aabf39455fe449c2d46c8d50ae7e98d0de6c301ac1d15f45a`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7f663cd19fdb2482f23a049a2e83117b526da0ad73131e73fcfe4dc5e53635`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 31.6 MB (31612727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c1e4c810b0e1cb879cad0bec7f75826c9040aceeb755690532fc1181d9fb1`  
		Last Modified: Sat, 31 Aug 2024 01:54:05 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5bd271a220b3b436116cae2105bb3a177c48e043c4dd3fd0d6ed9ab8015848`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 4.2 MB (4152127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d7d905b04205f119efc606778b4f1d82a6e2e5d5e3655790529aae14e90ba6`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b7918b5450a89e93a44512990195960e1a4e0502cb49f82ba3a78eba9350ab`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.7.9` - unknown; unknown

```console
$ docker pull composer@sha256:ec53877138e3fcd05768b1dc4bb3b19d3728790af26c97b2baf9bf5613b09c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8541813da59e7a04600e48f87a9ab19275d55e61cfbf734906f1bc9ebf5db813`

```dockerfile
```

-	Layers:
	-	`sha256:9e395b5be33bfe7fe5010adb29de378bdee4b6157103397beac3ac320251440a`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 2.1 MB (2145417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ee5098920bf84b8da06f1004dff77d5f0c006fb1cab68bc7718d23ffd153f8`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 31.1 KB (31134 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:a710f61aab1ce8a99c19a4024cf965d3ec937dcc2e153937cabe001d9b4b5db4
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
$ docker pull composer@sha256:76a2677544ab9e928c98186b37d4327efd3e74a5b6b0e6cf1c9399624f5d2c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68243059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d70afc6bb36eacbb3d15b53b6aa3afaae51a2eaff9f01721f55c5d9b57921d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Sep 2024 08:44:06 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Sep 2024 08:44:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Sep 2024 08:44:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_VERSION=8.3.11
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 05 Sep 2024 08:44:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Sep 2024 08:44:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15916673af8229814dcc44164d4616a6141bc5b586ae9362e741d64c6e4c91`  
		Last Modified: Sat, 07 Sep 2024 02:15:12 GMT  
		Size: 3.3 MB (3282678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb3258c4c6a46b7e182fa372bfe03ff37fd0fdf7f6894ca97b564fc382d7d4`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e436918c34ed4c536bdbaeace5213a8aaeb796ec65951fe681a10758ae2677`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6c87b6d10c2d5a9226b306e7fc3370cab80f9f41fe049706de7a51f8e1cf5a`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 12.5 MB (12502103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90d2c6f0ff71e78e4e311ebe4b83b2abbe5fdda23eaa28c5711e68b23c578da`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5cf8a88be3fd539ff5a60321e916df9fa78268109a78972d9411217023bf61`  
		Last Modified: Sat, 07 Sep 2024 02:16:52 GMT  
		Size: 17.2 MB (17212749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eea6dbc4cb9e274ad2228dfea58ecabec99b9336c8d528206ce4c41f6724ad`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f889a53b48220a2103d38ac31ed15adb68d8e5de71c03c475792439675576304`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fa61b2c2dec3cde7d7b254fe7cc695f7e1fcb5f9625f6e42c07b4976c2b4bb`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 30.6 MB (30647241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc185b71db015be6ffb966d849004a9b1afd7a3d9099d9ea8d2b743a4a6affc1`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeddc56dcb85f3b58b490f826f2b8a02a323be04c7e85ee4d67c52805fa43f9b`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 949.9 KB (949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77db48088bf9fcafb03ff9e33ceb1a2be151dcd65566c5fb764c0ac5d261e5b8`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01bd6daab7e4f446ad3a64e1bca2a2425cee9a5999a854476f33bbec8ab8f27`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:380fdcb085ccb206fec4f4b50b8bcf931391fffd2debdf6b738283b3d47535bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2311f82e2f94a4859282c18dbd009a3b9cf910062b4ac4f0a35d53f631178a75`

```dockerfile
```

-	Layers:
	-	`sha256:2502d4bff665dce0aa9952c0fd0a09899110a082f8081b55c899663df32d7c53`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 2.1 MB (2147466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3de91917cccb756e8648efe06ec60e26924d4b0093965412f052790c2ec35c`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 31.1 KB (31131 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:c9de0c54c9ad664ec3718bd74409988036df84f052f65ae5a844237837975b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68494557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087f2f76d1a94a9bcc3555f5f1857ae64bf69071de81794c4e05e3d2d9565d82`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:16:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:16:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:16:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:16:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:16:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:16:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:16:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:16:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 22:44:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 19:18:35 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 19:18:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 19:18:35 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 19:18:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 19:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 19:23:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 19:23:08 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 19:23:10 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 19:23:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 19:23:11 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b041a1a670328abed5fe2b73e068aba477e969ddbfe65c606c8054a4c36067b2`  
		Last Modified: Tue, 23 Jul 2024 01:00:35 GMT  
		Size: 3.3 MB (3263638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51daa6109cd19af541c6fc2600ad5a2f2382e50d3938e2b51f30d24df583fee`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b57c8706e4f06f42a10294d5c9eef985613e48298dedb390c6e6816b60a8f78`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b27cb594dc713e8223f5363b7505f762ad934cbf1c4f47ed7885c05db8e13`  
		Last Modified: Fri, 30 Aug 2024 20:20:12 GMT  
		Size: 12.5 MB (12502099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22237d0261563edb9ca222f6a36c5e175cf1d62c16f38e41755982d955f0e39c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ea243fc20547ec3f93ecbe653822d8a49a7c9c61fd5b7ad229cf6ee331209`  
		Last Modified: Fri, 30 Aug 2024 20:20:15 GMT  
		Size: 16.4 MB (16360114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a08c99e5b1cb1537070b37b1f8f3c78a107be7dd6efdd3a197aa7867d3d7a5c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68481b9e1f3b14557aa8d598c31b8ec7b735f77a5aeac9431ef7b69560d46a92`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c939352561246c630164d6835a0997969adc47f5e678a95dc31e21f57e94926d`  
		Last Modified: Fri, 30 Aug 2024 21:19:20 GMT  
		Size: 29.5 MB (29450758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f957f60156f9b6e900c9f3e132d2e377afa2f2d79dd2350288d3c3cf994fc2`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f354e7435ab3ecb4dc85feb20065dcc85c5b6bdc8e73172c0c130f2ae7cd9`  
		Last Modified: Thu, 05 Sep 2024 22:03:17 GMT  
		Size: 3.5 MB (3528377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12ece5c7e8ab6982a7044cbac04f6e5410efdba180cf3f82d3664a6a5b17b46`  
		Last Modified: Thu, 05 Sep 2024 22:03:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1259f25d9b072394ffbf557569b235c7044742bd33a81a9bfae78d674251acfe`  
		Last Modified: Thu, 05 Sep 2024 22:03:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:9e633785fdb4d8d10f84cec08db3b6f89fb96447cc0173e95e9184513e42af7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (30975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3adde16d5c6cafefdabe56b377da4b9d3bff02923e59c6e8c1b1e3adadc299`

```dockerfile
```

-	Layers:
	-	`sha256:686a058a7390a9266296d88cc6c40607dd67ef5b59d5e5281a954da2c53de8c9`  
		Last Modified: Thu, 05 Sep 2024 22:03:16 GMT  
		Size: 31.0 KB (30975 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:3bbff8da1174ec04349fa78e7ff4738c90ead0b737dd94018dace167d8b85b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66402051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df778fccceef1a7ad544eaff20cdf5cba33ef4ef9612f94e6d77290d4f2e8ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:31:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:31:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:31:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:31:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:31:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:31:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:01:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:38:44 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:38:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:38:45 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:38:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:38:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:41:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:41:37 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:41:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:41:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:41:38 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57db3d4836535044109c42cf341df21ab1def6a06fecbaf98ffac833b47f15b`  
		Last Modified: Tue, 23 Jul 2024 01:14:20 GMT  
		Size: 3.1 MB (3073093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991e70be4838afae3979e2bef4b2a7682dffac44793431e072ffbc9fc1686e5`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967a6fef2cedd5f47096963a74875b542f5e4f6667543712aa16505b281dcf7`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c472efc6552ca3c22ddd3afc3423433498a05fa5b26d79a2c74d9c71a5db0515`  
		Last Modified: Fri, 30 Aug 2024 21:50:47 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227ac46a3f3d5c7590120d9f555b6439500ed7212cdfe872e2850b122dc0be1`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba069329678371ed2d3ebd6d6b31019c124d7b205dd0cbc451d0f894c48081d1`  
		Last Modified: Fri, 30 Aug 2024 21:50:49 GMT  
		Size: 15.3 MB (15303131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f1b71f79757d6cb7ae12dc0d78c803efa304cf2be041b5e150fa74c97255c4`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da1f4159b65619170a1816f8957041566fec819f4092f532a9be4fae0766e2`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590a47b24d3ac1c6d1e93d41854d378374a6915b7752990a9bee3fc8716f4c34`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 29.1 MB (29073898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a7d4062ccea4fdf5ed8de172dbc9d1db681bcd5b390a4ffcb54fead69672`  
		Last Modified: Sat, 31 Aug 2024 02:31:06 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ad76e191ec614b29590aed98f8511a696131750ba8ef90780b12d7c01e6a32`  
		Last Modified: Fri, 06 Sep 2024 05:23:13 GMT  
		Size: 3.3 MB (3330474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e96125ef27271af0631684d5f71f871a29af21f239006963b59523149e60154`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4d0f7be48b8b2a1f66d091203ba34585babec9ea0a242b20f051e2e6a4153c`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:cf965cc496769a6d89a79df4f86c9511cdcfc4fae3d1812ee9c0d17a3350f139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414062359f838bcb24d9ae63386a189ce994a98cdc69f5668a083cc43fbe8f33`

```dockerfile
```

-	Layers:
	-	`sha256:06e04688ebe91d0536813dbc53e26f8ef0775ca460042a866ea8fa8a0ca3fa88`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 2.1 MB (2147787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38503d9dfee385b915286c453838f2d94fed6d661d99d2d083ba0ff7fe268092`  
		Last Modified: Fri, 06 Sep 2024 05:23:12 GMT  
		Size: 31.2 KB (31230 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:b869809691619076c257df807eea0a48aaa51d4e429db786ea735884edc778f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73242776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe18a77bd397705e87bd4ec8268d8233aada7eb48bf2f1ef4c35f3f556be535`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 23:30:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 23:30:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 23:30:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 23:30:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 23:30:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:50:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 19:56:37 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 19:56:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 19:56:37 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 19:56:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 19:56:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:01:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:01:00 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:01:01 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:01:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:01:01 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f069fb86c015646c4497d6fa3beaf8bd3f9f04d8f77a1a865ff47fc9922c27e3`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 3.3 MB (3324720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298458c1fe168646ba7edf3e03804ff1a01f1fac6b41ef2a94ef5bf333311f2b`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71c5e072e5141e780c5bbd4c1e2a34f9248a4b4a0983717a6c98be7560b899`  
		Last Modified: Tue, 23 Jul 2024 02:00:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eb94c855017ccb6e05ed05ab6089ac13ef31b7c2c4f68ac1aa7871f5e50f05`  
		Last Modified: Fri, 30 Aug 2024 21:23:23 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7788e2267fee70d1ccfd7ae5b7bdc051ea44976ed82a8dcce577cc9b0c8d6a`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d38576090a615f5e4f5732ed6ca99ac0f1721a6ed93df8c2a86c7b7d9a2539`  
		Last Modified: Fri, 30 Aug 2024 21:23:24 GMT  
		Size: 17.9 MB (17857930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb7c168c56b49540c07601d6cab358cafc4340a5f0dae6ef942aff3d828fa14`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f44bd4d0b7f587d16c7c70ac77c4a0a8d22a607399c38b6eb5ae4d5cd7d78b3`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 19.5 KB (19488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee874a6d0bc05b34617460b975ed3786bc3fb8320c0a847a478a06d8137ad3c`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 31.2 MB (31163203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab4e408f7d446ed2ebe4e87b8fc9ac34818639a1d6bd84e5e45a06bc7106695`  
		Last Modified: Sat, 31 Aug 2024 01:35:35 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471d29effa5f2eb83b2f0a7046bbe384437b0fdb94371156ddb902fcbae0c57d`  
		Last Modified: Thu, 05 Sep 2024 22:04:55 GMT  
		Size: 4.3 MB (4283528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93f6d78874f59727226d8b0f5d434289cfddd237bf281ce65ee61cbf48aed3d`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3de2366387cc3110c6029a23f39e799fee5b9af39ca4d6fd24935000537d74e`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:f671ade9cf000abfebed98797ba31a95e4b9e7c9a66abd8809ee449566a48cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c03772129e8978c8d7e3bf6d6b7628e243c359bf386c62625b423c670dee84`

```dockerfile
```

-	Layers:
	-	`sha256:5b2817a406bb8bbe15f0e63d07de7c7bc61dd5a16b2fa9a5f81bd6eb82393395`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 2.1 MB (2147617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45290e8d87ce7431906c7c10fa965bc3587af107940530164650c6eb891c40a5`  
		Last Modified: Thu, 05 Sep 2024 22:04:54 GMT  
		Size: 31.4 KB (31435 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:8312b8751b142b0a015dd9590e85278dc3a744c583f26917cc298274c257f717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49192907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19f9445ebcafde08291d1740ca48717f04d634fcfcfe719397192e34b54f346`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Sep 2024 08:44:06 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Sep 2024 08:44:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Sep 2024 08:44:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_VERSION=8.3.11
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 05 Sep 2024 08:44:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Sep 2024 08:44:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 05 Sep 2024 08:44:06 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17866811de1cdb9710f37a522dde62051d068230716118d22b6b987216e037ef`  
		Last Modified: Sat, 07 Sep 2024 01:49:46 GMT  
		Size: 3.3 MB (3331976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513ca5d3e6e64e8e064f1b178ad39b5d375a65559181a7f4964c9471461ba8f`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90338393c7a779c5576927d742c98b6841aa39aa84fe1b137708bd8f4d0ae68e`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20961f4e3b99e90c174a4f87f2af7f93ae78322283dde5d669a4c76c2c3cebd8`  
		Last Modified: Sat, 07 Sep 2024 01:51:38 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42171d227440b8721b3056f4e4f3a4916baf777d09c6f844c8f8056fbc70c42`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dabae8861b481fcfb1e16733b346f40d06038d6a5cd82cceb87bd8c3ee3ecd`  
		Last Modified: Sat, 07 Sep 2024 01:51:42 GMT  
		Size: 17.7 MB (17656052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d394881214b919e13be7206b61f0f6743c86558096cefb3ea4f89e68ad0c8d2`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357eacc586709ee7f5d5f8c1962caf6215d0ea35d2d9ed17c68628bfff98004d`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ceaf7eb2dca105a56d8088ae20e32e04da87d85e9f3f09128670d827655bf7`  
		Last Modified: Sat, 07 Sep 2024 02:57:36 GMT  
		Size: 11.3 MB (11281268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f027e9fbe9cf77b0fce954ce8fbd052e739b2ff93e8da28371a6d5e94a0e2cbe`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26346643aadaa9a17917fd876775e1dd782dee44797eb19fffa15a6041861dba`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 927.8 KB (927779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afa2275f20f7dd58d5cfed55223d78856a410a10571131099c93c96790fe01e`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731311864dda11557754fea1b4d013140d3888f5ae6a9ebdf49ab6817c32db2`  
		Last Modified: Sat, 07 Sep 2024 02:57:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:b7ead7cbc4ea95097c0765936f81f348282e2988e0a38da34af421c9e0fb9b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.2 KB (452233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15ae0e3c0095d9fc4067abeed65ebd7323312c0802e512309d7ef6a6f1f3441`

```dockerfile
```

-	Layers:
	-	`sha256:79ad4e506a516203b8ec59310d39679f1819e1ddf6e4eeaf2e829bc8e6c8f719`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 421.1 KB (421135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a25d9908a80b2d5c7108c6c649b0ce7ac73d06c70f6bc5f3f94f655c81dc34`  
		Last Modified: Sat, 07 Sep 2024 02:57:35 GMT  
		Size: 31.1 KB (31098 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:bc8587a56d445402ad83ed08b4fa4547ecd680b4c018d5ef5b80cd9c71a89ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73690032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57f38462579c8ced3b7f7847a77a0dfd7b8410d48af550afb90fe24f76fe2d3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 21:55:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 21:55:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 21:55:11 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 21:55:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 21:55:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 21:55:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 21:55:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 21:55:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 22:13:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:31:39 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:31:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:31:39 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:31:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:31:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:34:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:34:17 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:34:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:34:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:34:20 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3b3ac21bbea54c953ea1f2d18929d69c201c50acbb70a6157944a16d881644`  
		Last Modified: Mon, 22 Jul 2024 23:40:54 GMT  
		Size: 3.4 MB (3400973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab89bd2c65997355b0f8d6c170e8ada77fc5d87ae04f4e525032aad1d1c519`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9ea05d06440c67793ed8359925d4dcf5e15c76e0e78b5d20fad34b553a253f`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512248dd3ed75a17d321bc96ddef6ecae12695170f3a768584fe46b6fec8b581`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f97a91111a935f934126b9b5e843f52e61ce5a0d268da80ce88a7e9637e46b`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e963895597cd82f3e2562f1193ef440f635d77e3ce7d65a2d29a5f952d1ee09`  
		Last Modified: Fri, 30 Aug 2024 21:39:34 GMT  
		Size: 18.8 MB (18776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd6fc58c5780a4980b31da9f3258387aa34ad2ae9aa0edd08d9a5b90aaea95`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb9ba050d100c1c32d4f5b3c3975a0ebb302f1b9d8fb6c9b5c21dd9b7279d50`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b5ba9d088f76b4f58ad424d166ff3328d5c7af19e83e9bf897da73af9c27e5`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 31.7 MB (31678361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980ba58d45390240ed5b943d865d41bc6ceaa59661e4c900661678594a767b3f`  
		Last Modified: Sat, 31 Aug 2024 02:19:13 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc9d7e6a424d5f21f867ce20dd0412a843bc862bbfa52a72c8fec70a91e9820`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 3.7 MB (3735823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c66371ed6bb411621f796beb53658e55775622499a2e3cb680d11aef50836b`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e195cdfe80738ab413e61c2c78199d6ce718a1cc53c0e4009150b0b9e080233e`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:efab4d657adc63f8f5ec446309628d53ae9c1619621d59baffac7e8848599a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c0df070a167df4c3900ea024b5889a7c16cd645bc574984ff0d023102c384e`

```dockerfile
```

-	Layers:
	-	`sha256:05f796980c4a0d5999b42b6362b266f43d3c281b065548ce493711bf6784ca18`  
		Last Modified: Thu, 05 Sep 2024 23:26:46 GMT  
		Size: 2.1 MB (2146021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa61ab546b7b90ac789c29cb289298af77d133d2b3e4a9c4730de6952b1c4663`  
		Last Modified: Thu, 05 Sep 2024 23:26:45 GMT  
		Size: 31.2 KB (31175 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:bf673fa5bf49303d1284204bbbaebf69ce04845f99f9e2c2306fba331c9dd5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71357432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb65159493a0c7780698a7df08edba41813cfcb4b96941d9f076a7c58890f68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:40:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:40:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:40:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:40:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:40:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:40:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:40:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:40:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 01:15:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 22:01:05 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 22:01:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 22:01:06 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 22:01:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 22:01:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 22:49:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 22:49:31 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 22:49:37 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 22:49:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 22:49:39 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2d0e03d7a4d4766a64c04a50abfb02e217be153dd68888273b46568c4cac04`  
		Last Modified: Tue, 23 Jul 2024 12:29:02 GMT  
		Size: 3.4 MB (3397181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56268c2d820d6bf5bbf0e86c5bc55e50edc209a552c0844c6a9f787a880a2c6`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d3b9188b0e4a61167b2493ce280347bad9dfe72e9ecf4c18c5572f2cb6719`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d23ac9bf2deff71588cfd4b3f47c1364b66f45e05cb5d2518adb6a0396df50`  
		Last Modified: Sat, 31 Aug 2024 02:36:17 GMT  
		Size: 12.5 MB (12502106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869116b457f2e31f8fdb3c69a1bab7e4c51f76c00076389e0239f62c730528cf`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b247cb48214eaf57917fe6fa9b468fc196954c87b0933090b00ffbacd4cb7bd`  
		Last Modified: Sat, 31 Aug 2024 02:36:29 GMT  
		Size: 17.4 MB (17440090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f94c80d7718bd1bbc656205b6b9a90ee074a66d9466f41da567a907abd70f17`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a299e457c645ef0ea5f4f77590cbf1f9bbb149ab3b6d35be1e03c232e21b4298`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb74b37352199c3a76042764443f478982d69b68687aaf3b025bbe890eb8ac3f`  
		Last Modified: Sat, 31 Aug 2024 02:59:25 GMT  
		Size: 31.1 MB (31085763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5e8f63a80e285c25bb4838990371cbc88754639c0329cd9959283425dcc5eb`  
		Last Modified: Sat, 31 Aug 2024 02:59:22 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478ce11c08f84b8b7ef024ae95064e16cbf6ca32a8a9cd7f410dc361463eca95`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 3.5 MB (3537231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ae820656a3026d75cd896ddfb8c712b63434f5e78ca547f38a87da2d57760c`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eab9f887e2c0cae13ef41f6342ed9ff724873ce2065692a1e4cebd9660f3875`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:8e1dca6e31e5eb0d3cdf8a537041418b35bcdadfd2b2c9a2a2647f0ef9f6359b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0580b08ef8ef61d4939757c82ce29de24638ed0fd241ed6af77bf60e5ef3b4`

```dockerfile
```

-	Layers:
	-	`sha256:31a0c112e4561f1142fe90ba25be7145131a0daa0115e16bef20cb4a5e4e596e`  
		Last Modified: Thu, 05 Sep 2024 22:07:28 GMT  
		Size: 2.1 MB (2145637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc47b1511335b2b61390c61f237078daae30b87e51e2d5bbd0c89f5d6e329459`  
		Last Modified: Thu, 05 Sep 2024 22:07:28 GMT  
		Size: 31.2 KB (31176 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:1df015ec24cd23ae2d860ff918845a6067da37bae3e377cc24a7308496b987d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73197813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b68d12485ac34ba23fca979b223aa60d4a14122500e410ef718ce17654bacc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:33:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:33:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:33:37 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:33:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:33:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:33:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:33:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:33:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Jul 2024 23:08:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:02:04 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:02:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:02:04 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:02:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Aug 2024 20:02:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:05:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:05:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:05:07 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:05:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:05:07 GMT
CMD ["php" "-a"]
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 05 Sep 2024 08:44:06 GMT
ENV COMPOSER_VERSION=2.7.9
# Thu, 05 Sep 2024 08:44:06 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 08:44:06 GMT
WORKDIR /app
# Thu, 05 Sep 2024 08:44:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 08:44:06 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bee85c5a5fc33ed0d0f61a077ed76c922b87c42c5cb3a4dbba408dd62a64def`  
		Last Modified: Tue, 23 Jul 2024 00:56:03 GMT  
		Size: 3.5 MB (3467756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1505ad7d669e91b715e2a1bc7ec0c52dd53433332ad45653571cbe2c3643d5`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d87c5417e12df9b44287d4f554dd37d0b5b446d100409e5c49a17ac509a5b2`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2c4b161c20f3e37aa088308da3bb1a01ec5125d77c20033c4794149cec443`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 12.5 MB (12502092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c122a67a16e90a3dfd6817a2f8845d6e6a1bc5b93a02733eed109b49ac9ac44e`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b9a37a60aa5eac97b05abfe815776138ce85dc5ba1906d5c9515c50c45b044`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 18.0 MB (17977689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c966b6ee628194de003583de4dd26ad320f0da92fbe22a571ce2a42dff75c605`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32192d5d915f2f8aabf39455fe449c2d46c8d50ae7e98d0de6c301ac1d15f45a`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7f663cd19fdb2482f23a049a2e83117b526da0ad73131e73fcfe4dc5e53635`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 31.6 MB (31612727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c1e4c810b0e1cb879cad0bec7f75826c9040aceeb755690532fc1181d9fb1`  
		Last Modified: Sat, 31 Aug 2024 01:54:05 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5bd271a220b3b436116cae2105bb3a177c48e043c4dd3fd0d6ed9ab8015848`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 4.2 MB (4152127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d7d905b04205f119efc606778b4f1d82a6e2e5d5e3655790529aae14e90ba6`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b7918b5450a89e93a44512990195960e1a4e0502cb49f82ba3a78eba9350ab`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:ec53877138e3fcd05768b1dc4bb3b19d3728790af26c97b2baf9bf5613b09c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8541813da59e7a04600e48f87a9ab19275d55e61cfbf734906f1bc9ebf5db813`

```dockerfile
```

-	Layers:
	-	`sha256:9e395b5be33bfe7fe5010adb29de378bdee4b6157103397beac3ac320251440a`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 2.1 MB (2145417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ee5098920bf84b8da06f1004dff77d5f0c006fb1cab68bc7718d23ffd153f8`  
		Last Modified: Fri, 06 Sep 2024 03:35:25 GMT  
		Size: 31.1 KB (31134 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:lts`

```console
$ docker pull composer@sha256:85efd59b11f33fc18374fa0e5c86709f8a5fea3e9650df18053cd6d7b04d7714
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
$ docker pull composer@sha256:ef354ecde80d7fcb643c9f6f6aa2e2423078362ff7d12a323fd2c5186dd3d599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68107267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9994d5774040963d44077e2b5c3a689fac3bdfad5312bb016dd94244fbfaee49`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15916673af8229814dcc44164d4616a6141bc5b586ae9362e741d64c6e4c91`  
		Last Modified: Sat, 07 Sep 2024 02:15:12 GMT  
		Size: 3.3 MB (3282678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb3258c4c6a46b7e182fa372bfe03ff37fd0fdf7f6894ca97b564fc382d7d4`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e436918c34ed4c536bdbaeace5213a8aaeb796ec65951fe681a10758ae2677`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6c87b6d10c2d5a9226b306e7fc3370cab80f9f41fe049706de7a51f8e1cf5a`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 12.5 MB (12502103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90d2c6f0ff71e78e4e311ebe4b83b2abbe5fdda23eaa28c5711e68b23c578da`  
		Last Modified: Sat, 07 Sep 2024 02:16:49 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5cf8a88be3fd539ff5a60321e916df9fa78268109a78972d9411217023bf61`  
		Last Modified: Sat, 07 Sep 2024 02:16:52 GMT  
		Size: 17.2 MB (17212749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eea6dbc4cb9e274ad2228dfea58ecabec99b9336c8d528206ce4c41f6724ad`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f889a53b48220a2103d38ac31ed15adb68d8e5de71c03c475792439675576304`  
		Last Modified: Sat, 07 Sep 2024 02:16:48 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3080dfea9076e6b057ffd6e2fda1f2313882a16cb3b2be620d444d8716f47ed`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 30.6 MB (30647258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a21f363d6f1fab5e89d290f6716804f9b9506191d9b6c58871a9b11f8bfd2f5`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8b8ffc85688c7454f6c910028225d2b682797bd1677a0ce223545108c4c1c9`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 814.1 KB (814091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493b1985a4a796f58d1385e50c98d9872e2c9a346e575f45768ab2f6a5b0629e`  
		Last Modified: Sat, 07 Sep 2024 02:57:24 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db0479371de30561eeeb00b17d7b75c81ac293dcf11c4556cb6a71bc59ac403`  
		Last Modified: Sat, 07 Sep 2024 02:57:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:130e8b688936f3b028e396bea0208b91e0e19712fed8e3ae9a1e46b1ca32c778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2242271ab15d1a11c14d542e696cfa8cf177b197dee4d760ba5a20154f2027b8`

```dockerfile
```

-	Layers:
	-	`sha256:65ed272d5ffc6cc8ad2496a3e9b79a1ffb8c4a52ebab178e7e5f5e4eb448bf3b`  
		Last Modified: Sat, 07 Sep 2024 02:57:23 GMT  
		Size: 2.1 MB (2147172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f727a2ffde7c99d01bde1c4bf2d23563b58ba88753e9881f71538c69670a609f`  
		Last Modified: Sat, 07 Sep 2024 02:57:22 GMT  
		Size: 30.8 KB (30827 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v6

```console
$ docker pull composer@sha256:ab4df0f3dfbd1d8965fd3e2de431c1eee1f9beb71e4820a6b4c71b17b4669e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65779848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa7e3a1dedc7be2215c685d01f57637e2bf27ad51bd1e0e71a71abb97fd147f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b041a1a670328abed5fe2b73e068aba477e969ddbfe65c606c8054a4c36067b2`  
		Last Modified: Tue, 23 Jul 2024 01:00:35 GMT  
		Size: 3.3 MB (3263638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51daa6109cd19af541c6fc2600ad5a2f2382e50d3938e2b51f30d24df583fee`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b57c8706e4f06f42a10294d5c9eef985613e48298dedb390c6e6816b60a8f78`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b27cb594dc713e8223f5363b7505f762ad934cbf1c4f47ed7885c05db8e13`  
		Last Modified: Fri, 30 Aug 2024 20:20:12 GMT  
		Size: 12.5 MB (12502099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22237d0261563edb9ca222f6a36c5e175cf1d62c16f38e41755982d955f0e39c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ea243fc20547ec3f93ecbe653822d8a49a7c9c61fd5b7ad229cf6ee331209`  
		Last Modified: Fri, 30 Aug 2024 20:20:15 GMT  
		Size: 16.4 MB (16360114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a08c99e5b1cb1537070b37b1f8f3c78a107be7dd6efdd3a197aa7867d3d7a5c`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68481b9e1f3b14557aa8d598c31b8ec7b735f77a5aeac9431ef7b69560d46a92`  
		Last Modified: Fri, 30 Aug 2024 20:20:10 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c939352561246c630164d6835a0997969adc47f5e678a95dc31e21f57e94926d`  
		Last Modified: Fri, 30 Aug 2024 21:19:20 GMT  
		Size: 29.5 MB (29450758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f957f60156f9b6e900c9f3e132d2e377afa2f2d79dd2350288d3c3cf994fc2`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0024ec06ef23ce4ec077a63b60db5ffb584e27216e5be4423204ed6b3ee9d9ff`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 813.7 KB (813668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff00edb04cb0f9ff5be423ef9e64b2cc05ec099877d249544ab29d1038f5de3d`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849dafc07c8b03b2973789919523ffe9f0c9052a63652530c735314f8942657c`  
		Last Modified: Fri, 30 Aug 2024 21:19:20 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:515fe315f96216572fe9c92807daa2364060f55adb0939343f2e6f9c2ee5fab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0dde179ac6a00aee0b55cd0d47db549566a3234a33f45f2b16cfa4330eb46d`

```dockerfile
```

-	Layers:
	-	`sha256:f1dce4243535ccf2d00cbd4d3919988ef14db980db9aec68d4cdcbd5921a2ecf`  
		Last Modified: Fri, 30 Aug 2024 21:19:17 GMT  
		Size: 30.7 KB (30659 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v7

```console
$ docker pull composer@sha256:22599a3b141c242ec907a22de0a45dc607d4663fa65663ed4ce7fcae0b8e515e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63876262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30061f8b6f60071707176e9d676ae5f17ead9642086e9888c2aa65dc3176bdf8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57db3d4836535044109c42cf341df21ab1def6a06fecbaf98ffac833b47f15b`  
		Last Modified: Tue, 23 Jul 2024 01:14:20 GMT  
		Size: 3.1 MB (3073093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991e70be4838afae3979e2bef4b2a7682dffac44793431e072ffbc9fc1686e5`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967a6fef2cedd5f47096963a74875b542f5e4f6667543712aa16505b281dcf7`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c472efc6552ca3c22ddd3afc3423433498a05fa5b26d79a2c74d9c71a5db0515`  
		Last Modified: Fri, 30 Aug 2024 21:50:47 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227ac46a3f3d5c7590120d9f555b6439500ed7212cdfe872e2850b122dc0be1`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba069329678371ed2d3ebd6d6b31019c124d7b205dd0cbc451d0f894c48081d1`  
		Last Modified: Fri, 30 Aug 2024 21:50:49 GMT  
		Size: 15.3 MB (15303131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f1b71f79757d6cb7ae12dc0d78c803efa304cf2be041b5e150fa74c97255c4`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da1f4159b65619170a1816f8957041566fec819f4092f532a9be4fae0766e2`  
		Last Modified: Fri, 30 Aug 2024 21:50:46 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590a47b24d3ac1c6d1e93d41854d378374a6915b7752990a9bee3fc8716f4c34`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 29.1 MB (29073898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a7d4062ccea4fdf5ed8de172dbc9d1db681bcd5b390a4ffcb54fead69672`  
		Last Modified: Sat, 31 Aug 2024 02:31:06 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bcd20a2a658d50ec683a43833566710b84f4216194938d7af7cbf8c10210dd`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 804.7 KB (804685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c905190ed1bd03845eedb722e18ffc45b80ef025ab1c6f43997c55f1f800ceb`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944773c52e9f707928b0d29b7bf87541ac3570feff0f533ced8b01645298d971`  
		Last Modified: Sat, 31 Aug 2024 02:31:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:7fe76e5b9a9780c9cdbd9a895cc83c3b2476377536e62b87dbf161a9d0f338cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22918c5d8eba2985f99f9354a988108467181b3ec0587cfa0d276b25b148816d`

```dockerfile
```

-	Layers:
	-	`sha256:118580ec0c28ea60bb073b0529386d6410c5c3273787f1a0148d457792bdf79e`  
		Last Modified: Sat, 31 Aug 2024 02:31:05 GMT  
		Size: 2.1 MB (2147485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ac676009902101bbbc64e493d54a458bf29a597d82a7e60d159f970a30ca75d`  
		Last Modified: Sat, 31 Aug 2024 02:31:05 GMT  
		Size: 30.9 KB (30914 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:70a06924a1e1de676becb0dc74871a52c4236a11f810813c33eafacd3afed37e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69774571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d481a74ee31aad0920de6ddaad5d09e95246121f99bffee6edcd55bc4753b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f069fb86c015646c4497d6fa3beaf8bd3f9f04d8f77a1a865ff47fc9922c27e3`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 3.3 MB (3324720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298458c1fe168646ba7edf3e03804ff1a01f1fac6b41ef2a94ef5bf333311f2b`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71c5e072e5141e780c5bbd4c1e2a34f9248a4b4a0983717a6c98be7560b899`  
		Last Modified: Tue, 23 Jul 2024 02:00:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eb94c855017ccb6e05ed05ab6089ac13ef31b7c2c4f68ac1aa7871f5e50f05`  
		Last Modified: Fri, 30 Aug 2024 21:23:23 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7788e2267fee70d1ccfd7ae5b7bdc051ea44976ed82a8dcce577cc9b0c8d6a`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d38576090a615f5e4f5732ed6ca99ac0f1721a6ed93df8c2a86c7b7d9a2539`  
		Last Modified: Fri, 30 Aug 2024 21:23:24 GMT  
		Size: 17.9 MB (17857930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb7c168c56b49540c07601d6cab358cafc4340a5f0dae6ef942aff3d828fa14`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f44bd4d0b7f587d16c7c70ac77c4a0a8d22a607399c38b6eb5ae4d5cd7d78b3`  
		Last Modified: Fri, 30 Aug 2024 21:23:22 GMT  
		Size: 19.5 KB (19488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee874a6d0bc05b34617460b975ed3786bc3fb8320c0a847a478a06d8137ad3c`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 31.2 MB (31163203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab4e408f7d446ed2ebe4e87b8fc9ac34818639a1d6bd84e5e45a06bc7106695`  
		Last Modified: Sat, 31 Aug 2024 01:35:35 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf88b56f2caff98fcaa837bcf1d25e968ad076d11a4b61bfeb3c6b5cb980212`  
		Last Modified: Sat, 31 Aug 2024 01:35:35 GMT  
		Size: 815.3 KB (815324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ed584abd72db3d3f41e633a17439ea5d6bbd61a8b8665eec82007ba1f083db`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75117c9eb6ed3b4cec0958d69174c5b7e7e490066ac0b82c25e9f9aa41b51326`  
		Last Modified: Sat, 31 Aug 2024 01:35:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:680855afdfda70272d7bd80eda23b12167edb0f61bd1cbc3b94fdb0edf031025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729e6a7d8a05bb40c7ad680fb68991849ef818a43f82b8a33486f821729d49e1`

```dockerfile
```

-	Layers:
	-	`sha256:f383e20574737e2d7e47e5b7459e472aa1655e78a05434eb57222186191c3937`  
		Last Modified: Sat, 31 Aug 2024 01:35:34 GMT  
		Size: 2.1 MB (2147311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918075db4af02abd114ef74c8ef7850a61efd057308a01599c2a509e05136945`  
		Last Modified: Sat, 31 Aug 2024 01:35:33 GMT  
		Size: 31.1 KB (31116 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; 386

```console
$ docker pull composer@sha256:c285efacb3574249fdedf50f233480f6f3a622d40ce8f013d01ec36b29f87402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49056520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfce11e18c987a6a1d470dd14b899f54bed07bf2249f5cd66e473e33531f2a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17866811de1cdb9710f37a522dde62051d068230716118d22b6b987216e037ef`  
		Last Modified: Sat, 07 Sep 2024 01:49:46 GMT  
		Size: 3.3 MB (3331976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513ca5d3e6e64e8e064f1b178ad39b5d375a65559181a7f4964c9471461ba8f`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90338393c7a779c5576927d742c98b6841aa39aa84fe1b137708bd8f4d0ae68e`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20961f4e3b99e90c174a4f87f2af7f93ae78322283dde5d669a4c76c2c3cebd8`  
		Last Modified: Sat, 07 Sep 2024 01:51:38 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42171d227440b8721b3056f4e4f3a4916baf777d09c6f844c8f8056fbc70c42`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dabae8861b481fcfb1e16733b346f40d06038d6a5cd82cceb87bd8c3ee3ecd`  
		Last Modified: Sat, 07 Sep 2024 01:51:42 GMT  
		Size: 17.7 MB (17656052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d394881214b919e13be7206b61f0f6743c86558096cefb3ea4f89e68ad0c8d2`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357eacc586709ee7f5d5f8c1962caf6215d0ea35d2d9ed17c68628bfff98004d`  
		Last Modified: Sat, 07 Sep 2024 01:51:37 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c0582899ef276d3ef7782d863b75dc242b983d81f3ba38e9c2526cd4b66124`  
		Last Modified: Sat, 07 Sep 2024 02:57:38 GMT  
		Size: 11.3 MB (11281287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d9b78c504cbbb63a0444a48b1d4abf81c85399c46d67ae6bfe5b3e592c9b07`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a00cf43fce9b7a0f59f2513c440ceec89371153bcd9718ee7bf9392be0af70`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 791.4 KB (791375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002ae015b5c77256a349e1730eb8973dd000ba3b28d58f103d2ae02f5bdfd086`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370385d9ee8afe32b45f8acb99057b97b2791438daa050af3567f9b2011e5ba7`  
		Last Modified: Sat, 07 Sep 2024 02:57:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:5560243fa9b4a0bf35a669d325d6f47575b763d236dad10a588b2794f6e19fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.6 KB (451645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbf874329e4a41ef89503cb290d41ce3e36b666436c0e3aceac07aa9559dae0`

```dockerfile
```

-	Layers:
	-	`sha256:9a25c0d8e3da3517fbb36dbae00efe024ab4215f087b5a0470aac811b8e86ee7`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 420.8 KB (420846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0189d0fc46ef2c7b6d129d2de1b6c3fd667779e48e4c8fa308b37bc400b42457`  
		Last Modified: Sat, 07 Sep 2024 02:57:37 GMT  
		Size: 30.8 KB (30799 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; ppc64le

```console
$ docker pull composer@sha256:a98e733029bd8bd44adf828da681cc6c0da1b605d06cba3baf2a8b80ee1350b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70775287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfff63a4151c0efd88ae55b48123f440bcd7921a92db6c257f8a438cfb51f23`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3b3ac21bbea54c953ea1f2d18929d69c201c50acbb70a6157944a16d881644`  
		Last Modified: Mon, 22 Jul 2024 23:40:54 GMT  
		Size: 3.4 MB (3400973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab89bd2c65997355b0f8d6c170e8ada77fc5d87ae04f4e525032aad1d1c519`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9ea05d06440c67793ed8359925d4dcf5e15c76e0e78b5d20fad34b553a253f`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512248dd3ed75a17d321bc96ddef6ecae12695170f3a768584fe46b6fec8b581`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 12.5 MB (12502101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f97a91111a935f934126b9b5e843f52e61ce5a0d268da80ce88a7e9637e46b`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e963895597cd82f3e2562f1193ef440f635d77e3ce7d65a2d29a5f952d1ee09`  
		Last Modified: Fri, 30 Aug 2024 21:39:34 GMT  
		Size: 18.8 MB (18776853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd6fc58c5780a4980b31da9f3258387aa34ad2ae9aa0edd08d9a5b90aaea95`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb9ba050d100c1c32d4f5b3c3975a0ebb302f1b9d8fb6c9b5c21dd9b7279d50`  
		Last Modified: Fri, 30 Aug 2024 21:39:31 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b5ba9d088f76b4f58ad424d166ff3328d5c7af19e83e9bf897da73af9c27e5`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 31.7 MB (31678361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980ba58d45390240ed5b943d865d41bc6ceaa59661e4c900661678594a767b3f`  
		Last Modified: Sat, 31 Aug 2024 02:19:13 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07828b0dd98ae703ba1a00be52e896320b18f9b775c708e0176dd7eb96c55318`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 821.1 KB (821079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56202f9e9bddca31133a9f7d83d52de986e3ded88d49ca9325295c16ec61e825`  
		Last Modified: Sat, 31 Aug 2024 02:19:13 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5829414f07c88033c7b407bc997bf4ed280a090d6494a4ca8c5a43d9f9d507d`  
		Last Modified: Sat, 31 Aug 2024 02:19:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:c2fb27528e57fcdedc855613535ad95bb72b53d89902100e6c13347f655f3e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20ba4e929e3a856a4e26b6fa2bae28094763c8c6e038738cb3819c81f60bff0`

```dockerfile
```

-	Layers:
	-	`sha256:bf98f04c0fc52370a048dbc21243cd1217109a725f6167ca0fe28f0d161d8746`  
		Last Modified: Sat, 31 Aug 2024 02:19:12 GMT  
		Size: 2.1 MB (2145721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e647917393f3fc730762c47f394b76bd81338d62c29a6829e595ec0a11acb9b0`  
		Last Modified: Sat, 31 Aug 2024 02:19:11 GMT  
		Size: 30.9 KB (30863 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; riscv64

```console
$ docker pull composer@sha256:a4541babb1bf884f8dedb757ea86c56b94440baba3cf51eefa25d4b8ca347831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68633473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0545a0bc5ecec19f06ebf5d04b5fc85fcf2b61af79fcf2d19934a221486b28c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2d0e03d7a4d4766a64c04a50abfb02e217be153dd68888273b46568c4cac04`  
		Last Modified: Tue, 23 Jul 2024 12:29:02 GMT  
		Size: 3.4 MB (3397181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56268c2d820d6bf5bbf0e86c5bc55e50edc209a552c0844c6a9f787a880a2c6`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d3b9188b0e4a61167b2493ce280347bad9dfe72e9ecf4c18c5572f2cb6719`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d23ac9bf2deff71588cfd4b3f47c1364b66f45e05cb5d2518adb6a0396df50`  
		Last Modified: Sat, 31 Aug 2024 02:36:17 GMT  
		Size: 12.5 MB (12502106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869116b457f2e31f8fdb3c69a1bab7e4c51f76c00076389e0239f62c730528cf`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b247cb48214eaf57917fe6fa9b468fc196954c87b0933090b00ffbacd4cb7bd`  
		Last Modified: Sat, 31 Aug 2024 02:36:29 GMT  
		Size: 17.4 MB (17440090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f94c80d7718bd1bbc656205b6b9a90ee074a66d9466f41da567a907abd70f17`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a299e457c645ef0ea5f4f77590cbf1f9bbb149ab3b6d35be1e03c232e21b4298`  
		Last Modified: Sat, 31 Aug 2024 02:36:12 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb74b37352199c3a76042764443f478982d69b68687aaf3b025bbe890eb8ac3f`  
		Last Modified: Sat, 31 Aug 2024 02:59:25 GMT  
		Size: 31.1 MB (31085763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5e8f63a80e285c25bb4838990371cbc88754639c0329cd9959283425dcc5eb`  
		Last Modified: Sat, 31 Aug 2024 02:59:22 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd31bfeaed307e2701b79ab306d11ba9930bdf53c96eae5d5be586fdd1a56c6`  
		Last Modified: Sat, 31 Aug 2024 02:59:23 GMT  
		Size: 813.3 KB (813274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d571efdeb9bf54898af4e90923d32cc1c04e057a94ef91d1f753564f845bbb3b`  
		Last Modified: Sat, 31 Aug 2024 02:59:23 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2ab762566804d399ae0112a549d382e9e600b6b797048e440647dc4068be0c`  
		Last Modified: Sat, 31 Aug 2024 02:59:24 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:74044b90f011c891b06d80de02d02a56176762bbb679773a6d2446aec14584a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9783a359efa8738da17df08006fa430317809a32da56f2c37fa5ac913f69a720`

```dockerfile
```

-	Layers:
	-	`sha256:da4a7db55dc6e1522447c9d2beba40a94e5e604f7b5975095838d818e014e1b6`  
		Last Modified: Sat, 31 Aug 2024 02:59:20 GMT  
		Size: 2.1 MB (2145337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d69e59b16ea8290aa0ba5b1aff93c6f68ef6c036c9e39e175dec687d048838`  
		Last Modified: Sat, 31 Aug 2024 02:59:20 GMT  
		Size: 30.9 KB (30863 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; s390x

```console
$ docker pull composer@sha256:462905e539aedfd429d5c4c88d0a261f44f9ec753aaf9ef74a5dce9e53f78dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70350912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a560a0380c0f62794aed4a67120e26db5c383f3c4746d40a44174a1365b76e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 09:31:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 09:31:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_VERSION=8.3.11
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 09:31:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 09:31:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 09:31:03 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["php" "-a"]
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 20 Jun 2024 09:31:03 GMT
ENV COMPOSER_VERSION=2.2.24
# Thu, 20 Jun 2024 09:31:03 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 20 Jun 2024 09:31:03 GMT
WORKDIR /app
# Thu, 20 Jun 2024 09:31:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Jun 2024 09:31:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bee85c5a5fc33ed0d0f61a077ed76c922b87c42c5cb3a4dbba408dd62a64def`  
		Last Modified: Tue, 23 Jul 2024 00:56:03 GMT  
		Size: 3.5 MB (3467756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1505ad7d669e91b715e2a1bc7ec0c52dd53433332ad45653571cbe2c3643d5`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d87c5417e12df9b44287d4f554dd37d0b5b446d100409e5c49a17ac509a5b2`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2c4b161c20f3e37aa088308da3bb1a01ec5125d77c20033c4794149cec443`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 12.5 MB (12502092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c122a67a16e90a3dfd6817a2f8845d6e6a1bc5b93a02733eed109b49ac9ac44e`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b9a37a60aa5eac97b05abfe815776138ce85dc5ba1906d5c9515c50c45b044`  
		Last Modified: Fri, 30 Aug 2024 21:10:49 GMT  
		Size: 18.0 MB (17977689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c966b6ee628194de003583de4dd26ad320f0da92fbe22a571ce2a42dff75c605`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32192d5d915f2f8aabf39455fe449c2d46c8d50ae7e98d0de6c301ac1d15f45a`  
		Last Modified: Fri, 30 Aug 2024 21:10:46 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7f663cd19fdb2482f23a049a2e83117b526da0ad73131e73fcfe4dc5e53635`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 31.6 MB (31612727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c1e4c810b0e1cb879cad0bec7f75826c9040aceeb755690532fc1181d9fb1`  
		Last Modified: Sat, 31 Aug 2024 01:54:05 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d04ad993fbf3f6aa557c5ae6eab0cd4e7337a5a2ea31afe9f9655f2d2f19db`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 1.3 MB (1305226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57acd2fbfc4b9afdbc3e4bb67dc65e135d60a71d7c7cccb3c4cd632f5304c946`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e753b7b604d5e0a37393a583ddea761ff87299164502e1e51222836366efb986`  
		Last Modified: Sat, 31 Aug 2024 01:54:06 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:dbddd69d1ea80b21d5d1cf1ae9784cf243be1154a4ee3640cd18b92affeb8004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690c598e3d18036cf2a51a0c1cced0c355ddd077ad7da5e9478be8130385646b`

```dockerfile
```

-	Layers:
	-	`sha256:65eb103a793493d81a73a2c0dfb27394094894f3cea1f0821a49dff434207a0b`  
		Last Modified: Sat, 31 Aug 2024 01:54:04 GMT  
		Size: 2.1 MB (2145123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f57bc9ec7e845944ed195006c8e0df013226a85e7956944dcd7240cab5bc2e9f`  
		Last Modified: Sat, 31 Aug 2024 01:54:04 GMT  
		Size: 30.8 KB (30830 bytes)  
		MIME: application/vnd.in-toto+json
