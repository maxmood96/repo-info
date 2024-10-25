<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.27`](#composer11027)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.24`](#composer2224)
-	[`composer:2.8`](#composer28)
-	[`composer:2.8.1`](#composer281)
-	[`composer:latest`](#composerlatest)
-	[`composer:lts`](#composerlts)

## `composer:1`

```console
$ docker pull composer@sha256:e1e502d15f71e9d3ed3ccbe967eb23ad774e85d4ec8c2df7688c5f03275d6d28
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
$ docker pull composer@sha256:99fe6004b71f09329ce1b0ebd8e1428f55e5598edb63880d1238e811683afff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71176353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df455af34ba4885b50be5963a9b698dea73ceb84cba2dd01de7aae7738e7d10e`
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:41457434eddc5cb99259de159d6a2dad43029452b1ab35975a3209703b9897f4`  
		Last Modified: Fri, 25 Oct 2024 02:16:38 GMT  
		Size: 12.5 MB (12504689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328056f851cc57837c30c7c30c8c1fba0e538db1bdb0f520508b064b7771388b`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66dabf5a41275ff903a5f9ccc8ba9ba981ff4f80da78ac30a649f683542b98c`  
		Last Modified: Fri, 25 Oct 2024 02:16:40 GMT  
		Size: 20.5 MB (20518417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab768f68c87e7a556fcaf812a92acd5c8bf122cc606c956394a6ec4bc208f0f1`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b263e76cc797a1f79fdee350bf8047c4fae8cea974168046c693eec0894545`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5934ab82f142c5daa5c238676159a201fed61ea44cad05a110ebb737f10a20b5`  
		Last Modified: Fri, 25 Oct 2024 02:49:27 GMT  
		Size: 30.4 MB (30368544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319462321dc10399fdb9d53bc4553e3dcf11f5481d6d1a7ca9616cc4fc0c87fd`  
		Last Modified: Fri, 25 Oct 2024 02:49:27 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea515b73a7c21dba500dfcfa771fde86f739230f2317f21e00d984b1452f31`  
		Last Modified: Fri, 25 Oct 2024 02:49:27 GMT  
		Size: 853.6 KB (853623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06da49748e007f33887f3bdce3620ce8225a3ccb3b660504f7a87ba014b8a888`  
		Last Modified: Fri, 25 Oct 2024 02:49:27 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7fbfdca8951b496e7b0b8e3a4825f90f9411ff8818ec2c01892428d83259d1`  
		Last Modified: Fri, 25 Oct 2024 02:49:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:cd41c0f80dcde4a2943177af11d4cd746000515ca33f89ea019be436610bb8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8ea2f147e11706d5b5d7e9d005b279a18d5983fd7e65ffadb1c0c606d80db5`

```dockerfile
```

-	Layers:
	-	`sha256:687fa0178f9c2c3020f714f2a94a0bb95b5a34ddf62f3c3915cca7b58f89f1c0`  
		Last Modified: Fri, 25 Oct 2024 02:49:26 GMT  
		Size: 2.1 MB (2146303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e32cbc091d348a7f497efb9d6d11611b22be75bfd4babdc760386ae4a37e37`  
		Last Modified: Fri, 25 Oct 2024 02:49:26 GMT  
		Size: 30.9 KB (30870 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:18e9554ba5ecc71a7eafeef60738048700b7a663d269586152e36b70c55cfa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67900217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d469a3271f5a6c8472063241b117740d63271c3e4bd18fbb7dc98c6ba76a426`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78c7a9de9941e89cd785fc3ad14f52410d858d2259f5c9b2a852fd144612520`  
		Last Modified: Sat, 07 Sep 2024 00:48:55 GMT  
		Size: 3.3 MB (3269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbf8fddbe2a872480c609959838de42e95d1f5d5d3d8daadf7a1e44e5c381a2`  
		Last Modified: Sat, 07 Sep 2024 00:48:54 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d88511b2a3086248129999917d9f1e5928426fda8f08edf40ab5bafa37a9`  
		Last Modified: Sat, 07 Sep 2024 00:48:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2913caf4eeb0b47e0a269d5500be80ad644b55b830987923b9b25d7c47b779b6`  
		Last Modified: Fri, 25 Oct 2024 01:12:37 GMT  
		Size: 12.5 MB (12504684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd40e2319cfc199b8ddae2c1022299e653810d5c8fcff021ecf9e71bc732119`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8662dfadda858bf306da862403b12c0ebf0c2c06e8cc29019a10cec84a7ec93`  
		Last Modified: Fri, 25 Oct 2024 01:12:41 GMT  
		Size: 18.7 MB (18711875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0edc47bdf53f26bf4da16fdc4eec8b087534150b52237c0f603b8e571890a9`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43053646b918ed9c5822c17ca4869f057851bb96fcaabed794a5a7ec36dba34`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92515b32642bf33db09f5042274a35b3bf9dfd52f33a78bed3ddb0efab90867`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 29.2 MB (29169219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cececc96a315d5d1a226bb3d06189757c3df3f0bf808c3089f6a8c1ee57b169`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed191b05c95c8ec8e47091054ba961bb388402c18feea2659c81884ca0fa7f5`  
		Last Modified: Fri, 25 Oct 2024 02:10:40 GMT  
		Size: 853.8 KB (853787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5e376500c1dbf9e6b542bbd48cd51904faf1049e0278e1c2b18582fa895d55`  
		Last Modified: Fri, 30 Aug 2024 21:20:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5dd5a156fcf33f2f2b2c422187fca3ec4e062527208363db00209c5d247cd2`  
		Last Modified: Fri, 25 Oct 2024 02:10:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:566b52046428f961915055348dc32675f9f0a252eae9044bd8056bf344b89e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ee22fc3f09f77778664430a1e7f4a8c6a043e27dbfe289bb67071b9283f00e`

```dockerfile
```

-	Layers:
	-	`sha256:2044d2bfcf3dc71173e00b789e1fa37302fa2b612ef96744043e8c47ebfe93d5`  
		Last Modified: Fri, 25 Oct 2024 02:10:39 GMT  
		Size: 30.7 KB (30744 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:d9db427dd0ecd3160889132e21a5035797c127ed6c28fc6562dcb9a09e98ff91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65813047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2435769ea993c3e67819438fac854d4356d5615d3297d6443a89408d240ad1f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12c01d5f758f7fce28807153dec7a85ae2e307cf0d73f644d575cd875cb994a`  
		Last Modified: Fri, 06 Sep 2024 23:45:25 GMT  
		Size: 3.1 MB (3079568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c3e48f803b4ca0c1ec0b16f85f80f0a17b054845918112eb73b80eb9bd7297`  
		Last Modified: Fri, 06 Sep 2024 23:45:23 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7c21bdd57d9b7548f08c79a56f0a75d4e14a705967ae55d0450a10f0c6c43e`  
		Last Modified: Fri, 06 Sep 2024 23:45:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efe62db4f1f9f85f795e6cc1e7f8d835b0a8657d2a60143ba15d82d5863841`  
		Last Modified: Fri, 25 Oct 2024 02:37:26 GMT  
		Size: 12.5 MB (12504680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204359c9c9eb5cb76578981a5c068e3fac227ce0e7df1a86096569dc1230c85`  
		Last Modified: Fri, 25 Oct 2024 02:37:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2762620a9d567bff0020a3cda73a630f1a993bda6921efbd9554d75c9fd3377f`  
		Last Modified: Fri, 25 Oct 2024 02:37:28 GMT  
		Size: 17.5 MB (17478737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5a9688a15e4908bcd1ed18d76acd39f8678dd66decafbae483b2c884bf1c02`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66727798fd727eda6cfc82ff904b3773b442a67ae9e11967aac36d92e2e9be32`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ef898d316952fe64642bc94179ed2cc82e7c9404af0c91e8d0f5152097b5e8`  
		Last Modified: Fri, 25 Oct 2024 02:49:33 GMT  
		Size: 28.8 MB (28797969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48238d159943a0389cdf60849c19e218b8aeae434d69dfb9050fc0c71115bf9a`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4000b86640b910da67da0e0591b928b9814cab709f524c3dd116813edb020a`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 832.2 KB (832204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14448e76a87db89051e8c674c25c620592e20e601c5226e51e66ddad741a1abf`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2aded8b7a18a66a577aaca7215b0432641184fa882da02e64aa3019fb4ff43`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:a4e13b8dc804db99d2e5742cd1a7b106f85e35472e0be2f2dc36994a5293cbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbef1edcca25baa697af6ac82d649984278e4c8d5106b6732284be72a2d511d`

```dockerfile
```

-	Layers:
	-	`sha256:246718e2cc2b7267e00ae2ef31cc11a59866ee83cc1bcf8c0e568d838c185aee`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 2.1 MB (2146616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2db3fa5cb3eb40a40a6458915a921720bff3778fed84e05d2d68c0906ce947f`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 31.0 KB (30959 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:ed610a3ecc8a6641ff6f6f7140e51d4237c5a1375ce4fdbb72bb568e0e5f4364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72632568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93292c1520920760b20d22bb2b46e73891fee9345ee4739813bbb65f8986c4d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ef8ad75958cd7eb0e453d0f85e72134ef3976f8351b5742370df35bc60ed42`  
		Last Modified: Sat, 07 Sep 2024 02:23:50 GMT  
		Size: 3.3 MB (3333388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f80c1299f6c626e7df88761199f03734cced725870be7a04dd95bf11e80104`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb3615e2ca5466e128fbfbd9bfcaa4cc0a7c5935f1d980f13d765c6bfde9144`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b324dba8535eea2357b994da9864afef849388a4c8e80235090810383253f31`  
		Last Modified: Fri, 25 Oct 2024 02:19:36 GMT  
		Size: 12.5 MB (12504686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e479347c3f32eee03df523edd0f1a869f7a7636702922f9d5db1ac9024ea211`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6b8889455c447cc20eb2d9881a51c22cdac63cc440a2e647d8e5c2c7f13cfc`  
		Last Modified: Fri, 25 Oct 2024 02:19:37 GMT  
		Size: 20.9 MB (20940181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eeecc80b8f4736452eb3054bbf21ee480f6a4eb724b114b31cb94ab034f53c`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93069ffa1c1f8ac20ef6e8c62fa71d5ba3e5ae3f4ce6b97965ae1a5a0f2562bb`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98eea5daa433de13908b8daf3e98a58f41b648a198629693556299898d3050f`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 30.9 MB (30879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24933c1ee11a72c73a8c1d127f5254b2e1a343115700bfd5d40922a70347acac`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf17e219c699a2a72db781cffa3cc64fbf596fc72c55200fc286d9cdc8a4705`  
		Last Modified: Fri, 25 Oct 2024 04:24:52 GMT  
		Size: 862.6 KB (862632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce14b2b504eda344744c47bb683b1426b0fa486fabbfac2faa8105f727b08582`  
		Last Modified: Fri, 25 Oct 2024 04:24:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44f751e33221265625049db5a9c83603ddb0fb5a864f1fa1b741ae4c742bbbc`  
		Last Modified: Fri, 25 Oct 2024 04:24:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:a03c0f41e4217425cd386b0abe60fd531d6888584099ec45ba13a2cf3b0b8a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4319f087567573fd62e91b1ce51f33931f4db67de0100145586025faf5c134`

```dockerfile
```

-	Layers:
	-	`sha256:478665d61d84e761883072a907b1babb5b42cdc0c775a8d5ba85404d43e2b544`  
		Last Modified: Fri, 25 Oct 2024 04:24:51 GMT  
		Size: 2.1 MB (2146442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f598d25220811662bfae672ca57be5fde9a89c368c0a2ab0c5cb86d44dfdc22`  
		Last Modified: Fri, 25 Oct 2024 04:24:51 GMT  
		Size: 31.0 KB (30987 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:a74e7cd69fd5fdf58574ec5d7c5ba3b5ffb23be88ba39fe8c361b9f1f55a9206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52269419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecea442e97de0232c1d214efef1edbe4687f4fc157a2e1d85e26068b337d4b2f`
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:9eaf7c1d9791c6b12392f1f767948304f2c2e69cb0878ecec4d5df2be5af4dca`  
		Last Modified: Fri, 25 Oct 2024 04:22:20 GMT  
		Size: 12.5 MB (12504687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0bab9c844ca004a8fd6a7ea2a92c041012b047b66151b6d55f81e1e29009e`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609f4e456e59a3c94a5761b23648a66de98737427aa781c0b05b3296eacbef62`  
		Last Modified: Fri, 25 Oct 2024 04:22:23 GMT  
		Size: 20.8 MB (20818182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4455a0ae1ac0aca52a62943181a6673cf4e49459913cfea722ceb78acf98f28`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f23e94c0f2162ee0e26724220289d3609acb53f3117201cba2c8e6e5021efa`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 19.7 KB (19716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25461fdabdaef5271efc2bf4531ff19b94cd8934b3dfe7e2bf418bbb32d81a7`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 11.3 MB (11281334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abe68ad0ebdacbb851f9b459540ab25e692e7abc15e3721edf9cecaa068ea94`  
		Last Modified: Fri, 25 Oct 2024 04:50:04 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9246e07d5803105355a4670352210146b67c5b7d2f342f72914d58b29f471ec3`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 839.5 KB (839495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41663d1945b422f424a070ec2890346fea5b814db683465fc82753da7a2420d1`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e8579d9a88d2e6e4ad28e98f7c9af167da1e1c31511762afe8054b11d5a20`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:8fe92421f18332515e4db68490c13084c60405d2ee845b57eacf8b7c3d6f42a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 KB (450820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c9e925c5e713f40e117a305965ac065ca3f71ce1e8c2be703f4877e3500883`

```dockerfile
```

-	Layers:
	-	`sha256:09f9d01c8587517a625b0a1e78c7cf0dff1705643497fb4d296b5cd6a15f4bf0`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 420.0 KB (419977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:938747e2e36d8485f56f42361e570ac17bf8e1be1457b497896de59af4695ddb`  
		Last Modified: Fri, 25 Oct 2024 04:50:04 GMT  
		Size: 30.8 KB (30843 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:60bf2a71e3119e87187524f7e43e94e02d87237213ebd155e726e293cd5a5f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73070409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04dc7b892f59b50da40d47ba44723f21a51ff8123144cebdabcbfccc6642c416`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac727a268c34206d27f9588c3acfc276afdaf0623dfdc19b7d210a7a881ee4`  
		Last Modified: Sat, 07 Sep 2024 01:44:58 GMT  
		Size: 3.4 MB (3408322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564dcd8f1c226aa29a92bf07685b2a44ccb8ac47267a590bc34a56d25bbbcc4`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3867a87b0703f924c2a7915ce891a49d11c61af6d01613564e485431a9f78`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8622608d41f825e14aa5bd26799c3251549bceef128cf2eae2f52f1ab78913e`  
		Last Modified: Fri, 25 Oct 2024 00:57:34 GMT  
		Size: 12.5 MB (12504690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b9b2cc7fa22223c46604afd8fd56f225e535ca1e7d006d545233f411a4a3c0`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9400d92782aead1169d2e61549cc961ef18b1a2f1468fe9a486ae165d901cf6b`  
		Last Modified: Fri, 25 Oct 2024 00:57:37 GMT  
		Size: 21.3 MB (21285751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ccc474f40266b6e9c07bd2bd8edf9b2feccdf7986579f0a7bfa017cb90929`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd3a52d6da309a1907e5c8310c6411753ee8823a82029f55b265da24bb7566d`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b86ce86d7510dbd92b9dd787d737ff21b3ba726f05cb8546ccc581875d372d`  
		Last Modified: Fri, 25 Oct 2024 03:09:39 GMT  
		Size: 31.4 MB (31402604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74408fea44fbe8cb944832b386c9752e053e23539d049cfad4f03cac46f658f4`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba1f53a13e206b75025635546b42294f43407b4c0886512adca06f601c2d1c2`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 872.3 KB (872261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed73246db39a2f37864d4704852e731f1b98355a71cbfa582403452373a16a5`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7625397ca17be19f2ac1493062a678c2c27fc506926706292d9ec948080a95`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:b33917e7935b007beaa0ad8312f53fb782d5d50661a412557d64f940e0455b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a15032ba46bd6c66199f174035eeffe14fd7a9ebf8376ddab4f579ba83bc77c`

```dockerfile
```

-	Layers:
	-	`sha256:99be6629a5a89524b622be0403f011e5d36005d75ef65ce0b420f9743eb44f9c`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 2.1 MB (2144852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbadc54b255987b5a8cd0e61cb4086147d53a9f8a474693e60bf728686d39a7`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 30.9 KB (30907 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:95d42f5c8e075cb1a6d6669ea2ea22e58a1f89df5a716b820a1a124323c06872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70766351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e4f9b56f9bc2f90c3c24fa4fc25128df1540eb56e212ecaeaf7532af9c550d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160a71fe2c21fa0be03f4ecb3856d46307a8cab34f0749e89c452111c128a28e`  
		Last Modified: Sat, 07 Sep 2024 09:00:45 GMT  
		Size: 3.4 MB (3405216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99de0cdf41fffa764363801fb8a9efbd008b3689317846613f74f55be82ad4ec`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4878284381f1e57d12b980a3d3f2476a10fab26827866948f61cc0a2214a8`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d60d72a55a97ca66240c87e7bc1886bc5aa87d97579097a6d9bab88a75ae1d`  
		Last Modified: Fri, 25 Oct 2024 06:19:30 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55404ef143ec5be664bfb8b7d19253fad3452d91340eac96ad5cb7f88c34e9e`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f1fc6d05b292475d5cdd272dff683e4226cec9930f2394a99a2af5ad9a19c`  
		Last Modified: Fri, 25 Oct 2024 06:19:45 GMT  
		Size: 19.8 MB (19785919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f47a3a529d11fa207f1e96b631df8f8334701948d58152ac5419e07ef6f0b09`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5729eb71e7d125b843a7ed55653966533b980fcc3e19e4ee54ce1e25042a67`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d654c394fa744c0d5afc76db22431671980aa34529d74f487cfbb8e0857966`  
		Last Modified: Fri, 25 Oct 2024 09:50:35 GMT  
		Size: 30.8 MB (30811074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a58738e9c21fa9035cc24b974c8d99fbd269320abe6e366312beca87fb36e14`  
		Last Modified: Fri, 25 Oct 2024 09:50:31 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f99b08fe380cd3433f0a674009aeeb2859b0cdb7c42519d0c60d88c6eb2c8`  
		Last Modified: Fri, 25 Oct 2024 09:56:42 GMT  
		Size: 863.6 KB (863608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0527c2bf443290d937d302528997d29b7dec46cd4410f5cae140ffa4f5c9ce2`  
		Last Modified: Fri, 25 Oct 2024 09:56:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f0bed4782113f2e7ce0e0432be8b7bac1a2ccc30fc5131b48455511d554f5c`  
		Last Modified: Fri, 25 Oct 2024 09:56:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:ff74fefdefb013a70685728720daa95fe9965ea537761c5edfb3f1aff8edbe64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747348917de585d7f71dc6a64690f3016da998e5df6b8021758d8956431b5dc9`

```dockerfile
```

-	Layers:
	-	`sha256:9d4d21d439313124a4cdca34dcb6e825c4fa632adc4588d62d233059db6800e5`  
		Last Modified: Fri, 25 Oct 2024 09:56:42 GMT  
		Size: 2.1 MB (2144468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7831cdcc0293a4668d3f1b7fddf19ff875fed1b0de3846e082d27a232eca63ba`  
		Last Modified: Fri, 25 Oct 2024 09:56:41 GMT  
		Size: 30.9 KB (30907 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:ba0b51758570d1603c9d1a79e79d9984ea17d4ad71122de39631718e8c33b4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72096610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea189f687ac3a4235c4e5389a9b69c11e999d208d08cd08920892c75ff1926fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9208ede8519d248128a660ad6cbef1b3a33b141374be176c946b5b17b2968ab4`  
		Last Modified: Sat, 07 Sep 2024 00:42:38 GMT  
		Size: 3.5 MB (3473993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabbdadb2babb53e22b8c60bffa37b66bacdd1495093eec38748ca15dabc8287`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2431f4d7c348124f66281fa6433fdcded6e6a093aedb9cdd6fa9c7d87a1407`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8632e206b7bc36b0bfe226c5ec5e94154bc411b3677a2903f0f33e8b4d06d3`  
		Last Modified: Fri, 25 Oct 2024 02:46:23 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950b6d1374ddd91229978b32c87237f1a304df6908d46a3e6c6617379120ecb`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fac98b72a50f285d80ad08584ff62de41c8b0ea0276e5187d77f6dddb0430e4`  
		Last Modified: Fri, 25 Oct 2024 02:46:25 GMT  
		Size: 20.4 MB (20422987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17a61d0d2aae412d208b48c74e3754c9fc7b3f3d0644186eb5a952c01d1d01a`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c55de606062f9878f968213cb2af563401f158dbc5f7b5612b565d5f23a8d8`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a65e35183739b8872e800265ad579948004dd6060f487f2295911c401548795`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 31.3 MB (31338414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c5278f124e717ca16fc2677a7e92e4331ffd330679687f8429c052a4980ca6`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575557973f7add04a1a089c7862055c2c98ccda37474518502ea9a3dd722f89e`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 870.6 KB (870554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a02ba86566b001eebede2109925bcfacc44641549c7f5759627d94b6a722ae7`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09679b42c54f9c7976c72332e47ad04bf18c71e234c858f1713b6b3ff3732441`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:da66ffbdca6aa99a270caab47a9f9add1d9e6cf051e77f358ce4ab39df5efd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dca5383b013776298de61e007d592faaf498b949df992085e5f91374e3c24ec`

```dockerfile
```

-	Layers:
	-	`sha256:fca8df5fe3ba4a227fca2462dc0d8f7319acc477162c6c4fd9b659e96290e261`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 2.1 MB (2144254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa0a55e7ab0b0c78adde359808fe61c606a81b1b7e14cfcd33ff0005bec05aa5`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 30.9 KB (30871 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:e1e502d15f71e9d3ed3ccbe967eb23ad774e85d4ec8c2df7688c5f03275d6d28
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
$ docker pull composer@sha256:99fe6004b71f09329ce1b0ebd8e1428f55e5598edb63880d1238e811683afff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71176353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df455af34ba4885b50be5963a9b698dea73ceb84cba2dd01de7aae7738e7d10e`
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:41457434eddc5cb99259de159d6a2dad43029452b1ab35975a3209703b9897f4`  
		Last Modified: Fri, 25 Oct 2024 02:16:38 GMT  
		Size: 12.5 MB (12504689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328056f851cc57837c30c7c30c8c1fba0e538db1bdb0f520508b064b7771388b`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66dabf5a41275ff903a5f9ccc8ba9ba981ff4f80da78ac30a649f683542b98c`  
		Last Modified: Fri, 25 Oct 2024 02:16:40 GMT  
		Size: 20.5 MB (20518417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab768f68c87e7a556fcaf812a92acd5c8bf122cc606c956394a6ec4bc208f0f1`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b263e76cc797a1f79fdee350bf8047c4fae8cea974168046c693eec0894545`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5934ab82f142c5daa5c238676159a201fed61ea44cad05a110ebb737f10a20b5`  
		Last Modified: Fri, 25 Oct 2024 02:49:27 GMT  
		Size: 30.4 MB (30368544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319462321dc10399fdb9d53bc4553e3dcf11f5481d6d1a7ca9616cc4fc0c87fd`  
		Last Modified: Fri, 25 Oct 2024 02:49:27 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea515b73a7c21dba500dfcfa771fde86f739230f2317f21e00d984b1452f31`  
		Last Modified: Fri, 25 Oct 2024 02:49:27 GMT  
		Size: 853.6 KB (853623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06da49748e007f33887f3bdce3620ce8225a3ccb3b660504f7a87ba014b8a888`  
		Last Modified: Fri, 25 Oct 2024 02:49:27 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7fbfdca8951b496e7b0b8e3a4825f90f9411ff8818ec2c01892428d83259d1`  
		Last Modified: Fri, 25 Oct 2024 02:49:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:cd41c0f80dcde4a2943177af11d4cd746000515ca33f89ea019be436610bb8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8ea2f147e11706d5b5d7e9d005b279a18d5983fd7e65ffadb1c0c606d80db5`

```dockerfile
```

-	Layers:
	-	`sha256:687fa0178f9c2c3020f714f2a94a0bb95b5a34ddf62f3c3915cca7b58f89f1c0`  
		Last Modified: Fri, 25 Oct 2024 02:49:26 GMT  
		Size: 2.1 MB (2146303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e32cbc091d348a7f497efb9d6d11611b22be75bfd4babdc760386ae4a37e37`  
		Last Modified: Fri, 25 Oct 2024 02:49:26 GMT  
		Size: 30.9 KB (30870 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:18e9554ba5ecc71a7eafeef60738048700b7a663d269586152e36b70c55cfa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67900217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d469a3271f5a6c8472063241b117740d63271c3e4bd18fbb7dc98c6ba76a426`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78c7a9de9941e89cd785fc3ad14f52410d858d2259f5c9b2a852fd144612520`  
		Last Modified: Sat, 07 Sep 2024 00:48:55 GMT  
		Size: 3.3 MB (3269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbf8fddbe2a872480c609959838de42e95d1f5d5d3d8daadf7a1e44e5c381a2`  
		Last Modified: Sat, 07 Sep 2024 00:48:54 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d88511b2a3086248129999917d9f1e5928426fda8f08edf40ab5bafa37a9`  
		Last Modified: Sat, 07 Sep 2024 00:48:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2913caf4eeb0b47e0a269d5500be80ad644b55b830987923b9b25d7c47b779b6`  
		Last Modified: Fri, 25 Oct 2024 01:12:37 GMT  
		Size: 12.5 MB (12504684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd40e2319cfc199b8ddae2c1022299e653810d5c8fcff021ecf9e71bc732119`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8662dfadda858bf306da862403b12c0ebf0c2c06e8cc29019a10cec84a7ec93`  
		Last Modified: Fri, 25 Oct 2024 01:12:41 GMT  
		Size: 18.7 MB (18711875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0edc47bdf53f26bf4da16fdc4eec8b087534150b52237c0f603b8e571890a9`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43053646b918ed9c5822c17ca4869f057851bb96fcaabed794a5a7ec36dba34`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92515b32642bf33db09f5042274a35b3bf9dfd52f33a78bed3ddb0efab90867`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 29.2 MB (29169219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cececc96a315d5d1a226bb3d06189757c3df3f0bf808c3089f6a8c1ee57b169`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed191b05c95c8ec8e47091054ba961bb388402c18feea2659c81884ca0fa7f5`  
		Last Modified: Fri, 25 Oct 2024 02:10:40 GMT  
		Size: 853.8 KB (853787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5e376500c1dbf9e6b542bbd48cd51904faf1049e0278e1c2b18582fa895d55`  
		Last Modified: Fri, 30 Aug 2024 21:20:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5dd5a156fcf33f2f2b2c422187fca3ec4e062527208363db00209c5d247cd2`  
		Last Modified: Fri, 25 Oct 2024 02:10:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:566b52046428f961915055348dc32675f9f0a252eae9044bd8056bf344b89e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ee22fc3f09f77778664430a1e7f4a8c6a043e27dbfe289bb67071b9283f00e`

```dockerfile
```

-	Layers:
	-	`sha256:2044d2bfcf3dc71173e00b789e1fa37302fa2b612ef96744043e8c47ebfe93d5`  
		Last Modified: Fri, 25 Oct 2024 02:10:39 GMT  
		Size: 30.7 KB (30744 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:d9db427dd0ecd3160889132e21a5035797c127ed6c28fc6562dcb9a09e98ff91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65813047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2435769ea993c3e67819438fac854d4356d5615d3297d6443a89408d240ad1f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12c01d5f758f7fce28807153dec7a85ae2e307cf0d73f644d575cd875cb994a`  
		Last Modified: Fri, 06 Sep 2024 23:45:25 GMT  
		Size: 3.1 MB (3079568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c3e48f803b4ca0c1ec0b16f85f80f0a17b054845918112eb73b80eb9bd7297`  
		Last Modified: Fri, 06 Sep 2024 23:45:23 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7c21bdd57d9b7548f08c79a56f0a75d4e14a705967ae55d0450a10f0c6c43e`  
		Last Modified: Fri, 06 Sep 2024 23:45:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efe62db4f1f9f85f795e6cc1e7f8d835b0a8657d2a60143ba15d82d5863841`  
		Last Modified: Fri, 25 Oct 2024 02:37:26 GMT  
		Size: 12.5 MB (12504680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204359c9c9eb5cb76578981a5c068e3fac227ce0e7df1a86096569dc1230c85`  
		Last Modified: Fri, 25 Oct 2024 02:37:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2762620a9d567bff0020a3cda73a630f1a993bda6921efbd9554d75c9fd3377f`  
		Last Modified: Fri, 25 Oct 2024 02:37:28 GMT  
		Size: 17.5 MB (17478737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5a9688a15e4908bcd1ed18d76acd39f8678dd66decafbae483b2c884bf1c02`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66727798fd727eda6cfc82ff904b3773b442a67ae9e11967aac36d92e2e9be32`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ef898d316952fe64642bc94179ed2cc82e7c9404af0c91e8d0f5152097b5e8`  
		Last Modified: Fri, 25 Oct 2024 02:49:33 GMT  
		Size: 28.8 MB (28797969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48238d159943a0389cdf60849c19e218b8aeae434d69dfb9050fc0c71115bf9a`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4000b86640b910da67da0e0591b928b9814cab709f524c3dd116813edb020a`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 832.2 KB (832204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14448e76a87db89051e8c674c25c620592e20e601c5226e51e66ddad741a1abf`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2aded8b7a18a66a577aaca7215b0432641184fa882da02e64aa3019fb4ff43`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:a4e13b8dc804db99d2e5742cd1a7b106f85e35472e0be2f2dc36994a5293cbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbef1edcca25baa697af6ac82d649984278e4c8d5106b6732284be72a2d511d`

```dockerfile
```

-	Layers:
	-	`sha256:246718e2cc2b7267e00ae2ef31cc11a59866ee83cc1bcf8c0e568d838c185aee`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 2.1 MB (2146616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2db3fa5cb3eb40a40a6458915a921720bff3778fed84e05d2d68c0906ce947f`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 31.0 KB (30959 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:ed610a3ecc8a6641ff6f6f7140e51d4237c5a1375ce4fdbb72bb568e0e5f4364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72632568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93292c1520920760b20d22bb2b46e73891fee9345ee4739813bbb65f8986c4d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ef8ad75958cd7eb0e453d0f85e72134ef3976f8351b5742370df35bc60ed42`  
		Last Modified: Sat, 07 Sep 2024 02:23:50 GMT  
		Size: 3.3 MB (3333388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f80c1299f6c626e7df88761199f03734cced725870be7a04dd95bf11e80104`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb3615e2ca5466e128fbfbd9bfcaa4cc0a7c5935f1d980f13d765c6bfde9144`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b324dba8535eea2357b994da9864afef849388a4c8e80235090810383253f31`  
		Last Modified: Fri, 25 Oct 2024 02:19:36 GMT  
		Size: 12.5 MB (12504686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e479347c3f32eee03df523edd0f1a869f7a7636702922f9d5db1ac9024ea211`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6b8889455c447cc20eb2d9881a51c22cdac63cc440a2e647d8e5c2c7f13cfc`  
		Last Modified: Fri, 25 Oct 2024 02:19:37 GMT  
		Size: 20.9 MB (20940181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eeecc80b8f4736452eb3054bbf21ee480f6a4eb724b114b31cb94ab034f53c`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93069ffa1c1f8ac20ef6e8c62fa71d5ba3e5ae3f4ce6b97965ae1a5a0f2562bb`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98eea5daa433de13908b8daf3e98a58f41b648a198629693556299898d3050f`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 30.9 MB (30879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24933c1ee11a72c73a8c1d127f5254b2e1a343115700bfd5d40922a70347acac`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf17e219c699a2a72db781cffa3cc64fbf596fc72c55200fc286d9cdc8a4705`  
		Last Modified: Fri, 25 Oct 2024 04:24:52 GMT  
		Size: 862.6 KB (862632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce14b2b504eda344744c47bb683b1426b0fa486fabbfac2faa8105f727b08582`  
		Last Modified: Fri, 25 Oct 2024 04:24:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44f751e33221265625049db5a9c83603ddb0fb5a864f1fa1b741ae4c742bbbc`  
		Last Modified: Fri, 25 Oct 2024 04:24:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:a03c0f41e4217425cd386b0abe60fd531d6888584099ec45ba13a2cf3b0b8a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4319f087567573fd62e91b1ce51f33931f4db67de0100145586025faf5c134`

```dockerfile
```

-	Layers:
	-	`sha256:478665d61d84e761883072a907b1babb5b42cdc0c775a8d5ba85404d43e2b544`  
		Last Modified: Fri, 25 Oct 2024 04:24:51 GMT  
		Size: 2.1 MB (2146442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f598d25220811662bfae672ca57be5fde9a89c368c0a2ab0c5cb86d44dfdc22`  
		Last Modified: Fri, 25 Oct 2024 04:24:51 GMT  
		Size: 31.0 KB (30987 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:a74e7cd69fd5fdf58574ec5d7c5ba3b5ffb23be88ba39fe8c361b9f1f55a9206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52269419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecea442e97de0232c1d214efef1edbe4687f4fc157a2e1d85e26068b337d4b2f`
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:9eaf7c1d9791c6b12392f1f767948304f2c2e69cb0878ecec4d5df2be5af4dca`  
		Last Modified: Fri, 25 Oct 2024 04:22:20 GMT  
		Size: 12.5 MB (12504687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0bab9c844ca004a8fd6a7ea2a92c041012b047b66151b6d55f81e1e29009e`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609f4e456e59a3c94a5761b23648a66de98737427aa781c0b05b3296eacbef62`  
		Last Modified: Fri, 25 Oct 2024 04:22:23 GMT  
		Size: 20.8 MB (20818182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4455a0ae1ac0aca52a62943181a6673cf4e49459913cfea722ceb78acf98f28`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f23e94c0f2162ee0e26724220289d3609acb53f3117201cba2c8e6e5021efa`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 19.7 KB (19716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25461fdabdaef5271efc2bf4531ff19b94cd8934b3dfe7e2bf418bbb32d81a7`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 11.3 MB (11281334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abe68ad0ebdacbb851f9b459540ab25e692e7abc15e3721edf9cecaa068ea94`  
		Last Modified: Fri, 25 Oct 2024 04:50:04 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9246e07d5803105355a4670352210146b67c5b7d2f342f72914d58b29f471ec3`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 839.5 KB (839495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41663d1945b422f424a070ec2890346fea5b814db683465fc82753da7a2420d1`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e8579d9a88d2e6e4ad28e98f7c9af167da1e1c31511762afe8054b11d5a20`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:8fe92421f18332515e4db68490c13084c60405d2ee845b57eacf8b7c3d6f42a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 KB (450820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c9e925c5e713f40e117a305965ac065ca3f71ce1e8c2be703f4877e3500883`

```dockerfile
```

-	Layers:
	-	`sha256:09f9d01c8587517a625b0a1e78c7cf0dff1705643497fb4d296b5cd6a15f4bf0`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 420.0 KB (419977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:938747e2e36d8485f56f42361e570ac17bf8e1be1457b497896de59af4695ddb`  
		Last Modified: Fri, 25 Oct 2024 04:50:04 GMT  
		Size: 30.8 KB (30843 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:60bf2a71e3119e87187524f7e43e94e02d87237213ebd155e726e293cd5a5f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73070409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04dc7b892f59b50da40d47ba44723f21a51ff8123144cebdabcbfccc6642c416`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac727a268c34206d27f9588c3acfc276afdaf0623dfdc19b7d210a7a881ee4`  
		Last Modified: Sat, 07 Sep 2024 01:44:58 GMT  
		Size: 3.4 MB (3408322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564dcd8f1c226aa29a92bf07685b2a44ccb8ac47267a590bc34a56d25bbbcc4`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3867a87b0703f924c2a7915ce891a49d11c61af6d01613564e485431a9f78`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8622608d41f825e14aa5bd26799c3251549bceef128cf2eae2f52f1ab78913e`  
		Last Modified: Fri, 25 Oct 2024 00:57:34 GMT  
		Size: 12.5 MB (12504690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b9b2cc7fa22223c46604afd8fd56f225e535ca1e7d006d545233f411a4a3c0`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9400d92782aead1169d2e61549cc961ef18b1a2f1468fe9a486ae165d901cf6b`  
		Last Modified: Fri, 25 Oct 2024 00:57:37 GMT  
		Size: 21.3 MB (21285751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ccc474f40266b6e9c07bd2bd8edf9b2feccdf7986579f0a7bfa017cb90929`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd3a52d6da309a1907e5c8310c6411753ee8823a82029f55b265da24bb7566d`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b86ce86d7510dbd92b9dd787d737ff21b3ba726f05cb8546ccc581875d372d`  
		Last Modified: Fri, 25 Oct 2024 03:09:39 GMT  
		Size: 31.4 MB (31402604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74408fea44fbe8cb944832b386c9752e053e23539d049cfad4f03cac46f658f4`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba1f53a13e206b75025635546b42294f43407b4c0886512adca06f601c2d1c2`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 872.3 KB (872261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed73246db39a2f37864d4704852e731f1b98355a71cbfa582403452373a16a5`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7625397ca17be19f2ac1493062a678c2c27fc506926706292d9ec948080a95`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:b33917e7935b007beaa0ad8312f53fb782d5d50661a412557d64f940e0455b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a15032ba46bd6c66199f174035eeffe14fd7a9ebf8376ddab4f579ba83bc77c`

```dockerfile
```

-	Layers:
	-	`sha256:99be6629a5a89524b622be0403f011e5d36005d75ef65ce0b420f9743eb44f9c`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 2.1 MB (2144852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbadc54b255987b5a8cd0e61cb4086147d53a9f8a474693e60bf728686d39a7`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 30.9 KB (30907 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:95d42f5c8e075cb1a6d6669ea2ea22e58a1f89df5a716b820a1a124323c06872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70766351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e4f9b56f9bc2f90c3c24fa4fc25128df1540eb56e212ecaeaf7532af9c550d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160a71fe2c21fa0be03f4ecb3856d46307a8cab34f0749e89c452111c128a28e`  
		Last Modified: Sat, 07 Sep 2024 09:00:45 GMT  
		Size: 3.4 MB (3405216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99de0cdf41fffa764363801fb8a9efbd008b3689317846613f74f55be82ad4ec`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4878284381f1e57d12b980a3d3f2476a10fab26827866948f61cc0a2214a8`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d60d72a55a97ca66240c87e7bc1886bc5aa87d97579097a6d9bab88a75ae1d`  
		Last Modified: Fri, 25 Oct 2024 06:19:30 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55404ef143ec5be664bfb8b7d19253fad3452d91340eac96ad5cb7f88c34e9e`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f1fc6d05b292475d5cdd272dff683e4226cec9930f2394a99a2af5ad9a19c`  
		Last Modified: Fri, 25 Oct 2024 06:19:45 GMT  
		Size: 19.8 MB (19785919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f47a3a529d11fa207f1e96b631df8f8334701948d58152ac5419e07ef6f0b09`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5729eb71e7d125b843a7ed55653966533b980fcc3e19e4ee54ce1e25042a67`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d654c394fa744c0d5afc76db22431671980aa34529d74f487cfbb8e0857966`  
		Last Modified: Fri, 25 Oct 2024 09:50:35 GMT  
		Size: 30.8 MB (30811074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a58738e9c21fa9035cc24b974c8d99fbd269320abe6e366312beca87fb36e14`  
		Last Modified: Fri, 25 Oct 2024 09:50:31 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f99b08fe380cd3433f0a674009aeeb2859b0cdb7c42519d0c60d88c6eb2c8`  
		Last Modified: Fri, 25 Oct 2024 09:56:42 GMT  
		Size: 863.6 KB (863608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0527c2bf443290d937d302528997d29b7dec46cd4410f5cae140ffa4f5c9ce2`  
		Last Modified: Fri, 25 Oct 2024 09:56:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f0bed4782113f2e7ce0e0432be8b7bac1a2ccc30fc5131b48455511d554f5c`  
		Last Modified: Fri, 25 Oct 2024 09:56:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:ff74fefdefb013a70685728720daa95fe9965ea537761c5edfb3f1aff8edbe64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747348917de585d7f71dc6a64690f3016da998e5df6b8021758d8956431b5dc9`

```dockerfile
```

-	Layers:
	-	`sha256:9d4d21d439313124a4cdca34dcb6e825c4fa632adc4588d62d233059db6800e5`  
		Last Modified: Fri, 25 Oct 2024 09:56:42 GMT  
		Size: 2.1 MB (2144468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7831cdcc0293a4668d3f1b7fddf19ff875fed1b0de3846e082d27a232eca63ba`  
		Last Modified: Fri, 25 Oct 2024 09:56:41 GMT  
		Size: 30.9 KB (30907 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:ba0b51758570d1603c9d1a79e79d9984ea17d4ad71122de39631718e8c33b4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72096610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea189f687ac3a4235c4e5389a9b69c11e999d208d08cd08920892c75ff1926fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9208ede8519d248128a660ad6cbef1b3a33b141374be176c946b5b17b2968ab4`  
		Last Modified: Sat, 07 Sep 2024 00:42:38 GMT  
		Size: 3.5 MB (3473993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabbdadb2babb53e22b8c60bffa37b66bacdd1495093eec38748ca15dabc8287`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2431f4d7c348124f66281fa6433fdcded6e6a093aedb9cdd6fa9c7d87a1407`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8632e206b7bc36b0bfe226c5ec5e94154bc411b3677a2903f0f33e8b4d06d3`  
		Last Modified: Fri, 25 Oct 2024 02:46:23 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950b6d1374ddd91229978b32c87237f1a304df6908d46a3e6c6617379120ecb`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fac98b72a50f285d80ad08584ff62de41c8b0ea0276e5187d77f6dddb0430e4`  
		Last Modified: Fri, 25 Oct 2024 02:46:25 GMT  
		Size: 20.4 MB (20422987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17a61d0d2aae412d208b48c74e3754c9fc7b3f3d0644186eb5a952c01d1d01a`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c55de606062f9878f968213cb2af563401f158dbc5f7b5612b565d5f23a8d8`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a65e35183739b8872e800265ad579948004dd6060f487f2295911c401548795`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 31.3 MB (31338414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c5278f124e717ca16fc2677a7e92e4331ffd330679687f8429c052a4980ca6`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575557973f7add04a1a089c7862055c2c98ccda37474518502ea9a3dd722f89e`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 870.6 KB (870554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a02ba86566b001eebede2109925bcfacc44641549c7f5759627d94b6a722ae7`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09679b42c54f9c7976c72332e47ad04bf18c71e234c858f1713b6b3ff3732441`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:da66ffbdca6aa99a270caab47a9f9add1d9e6cf051e77f358ce4ab39df5efd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dca5383b013776298de61e007d592faaf498b949df992085e5f91374e3c24ec`

```dockerfile
```

-	Layers:
	-	`sha256:fca8df5fe3ba4a227fca2462dc0d8f7319acc477162c6c4fd9b659e96290e261`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 2.1 MB (2144254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa0a55e7ab0b0c78adde359808fe61c606a81b1b7e14cfcd33ff0005bec05aa5`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 30.9 KB (30871 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:e1e502d15f71e9d3ed3ccbe967eb23ad774e85d4ec8c2df7688c5f03275d6d28
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
$ docker pull composer@sha256:99fe6004b71f09329ce1b0ebd8e1428f55e5598edb63880d1238e811683afff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71176353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df455af34ba4885b50be5963a9b698dea73ceb84cba2dd01de7aae7738e7d10e`
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:41457434eddc5cb99259de159d6a2dad43029452b1ab35975a3209703b9897f4`  
		Last Modified: Fri, 25 Oct 2024 02:16:38 GMT  
		Size: 12.5 MB (12504689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328056f851cc57837c30c7c30c8c1fba0e538db1bdb0f520508b064b7771388b`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66dabf5a41275ff903a5f9ccc8ba9ba981ff4f80da78ac30a649f683542b98c`  
		Last Modified: Fri, 25 Oct 2024 02:16:40 GMT  
		Size: 20.5 MB (20518417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab768f68c87e7a556fcaf812a92acd5c8bf122cc606c956394a6ec4bc208f0f1`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b263e76cc797a1f79fdee350bf8047c4fae8cea974168046c693eec0894545`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5934ab82f142c5daa5c238676159a201fed61ea44cad05a110ebb737f10a20b5`  
		Last Modified: Fri, 25 Oct 2024 02:49:27 GMT  
		Size: 30.4 MB (30368544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319462321dc10399fdb9d53bc4553e3dcf11f5481d6d1a7ca9616cc4fc0c87fd`  
		Last Modified: Fri, 25 Oct 2024 02:49:27 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea515b73a7c21dba500dfcfa771fde86f739230f2317f21e00d984b1452f31`  
		Last Modified: Fri, 25 Oct 2024 02:49:27 GMT  
		Size: 853.6 KB (853623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06da49748e007f33887f3bdce3620ce8225a3ccb3b660504f7a87ba014b8a888`  
		Last Modified: Fri, 25 Oct 2024 02:49:27 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7fbfdca8951b496e7b0b8e3a4825f90f9411ff8818ec2c01892428d83259d1`  
		Last Modified: Fri, 25 Oct 2024 02:49:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:cd41c0f80dcde4a2943177af11d4cd746000515ca33f89ea019be436610bb8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8ea2f147e11706d5b5d7e9d005b279a18d5983fd7e65ffadb1c0c606d80db5`

```dockerfile
```

-	Layers:
	-	`sha256:687fa0178f9c2c3020f714f2a94a0bb95b5a34ddf62f3c3915cca7b58f89f1c0`  
		Last Modified: Fri, 25 Oct 2024 02:49:26 GMT  
		Size: 2.1 MB (2146303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e32cbc091d348a7f497efb9d6d11611b22be75bfd4babdc760386ae4a37e37`  
		Last Modified: Fri, 25 Oct 2024 02:49:26 GMT  
		Size: 30.9 KB (30870 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v6

```console
$ docker pull composer@sha256:18e9554ba5ecc71a7eafeef60738048700b7a663d269586152e36b70c55cfa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67900217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d469a3271f5a6c8472063241b117740d63271c3e4bd18fbb7dc98c6ba76a426`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78c7a9de9941e89cd785fc3ad14f52410d858d2259f5c9b2a852fd144612520`  
		Last Modified: Sat, 07 Sep 2024 00:48:55 GMT  
		Size: 3.3 MB (3269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbf8fddbe2a872480c609959838de42e95d1f5d5d3d8daadf7a1e44e5c381a2`  
		Last Modified: Sat, 07 Sep 2024 00:48:54 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d88511b2a3086248129999917d9f1e5928426fda8f08edf40ab5bafa37a9`  
		Last Modified: Sat, 07 Sep 2024 00:48:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2913caf4eeb0b47e0a269d5500be80ad644b55b830987923b9b25d7c47b779b6`  
		Last Modified: Fri, 25 Oct 2024 01:12:37 GMT  
		Size: 12.5 MB (12504684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd40e2319cfc199b8ddae2c1022299e653810d5c8fcff021ecf9e71bc732119`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8662dfadda858bf306da862403b12c0ebf0c2c06e8cc29019a10cec84a7ec93`  
		Last Modified: Fri, 25 Oct 2024 01:12:41 GMT  
		Size: 18.7 MB (18711875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0edc47bdf53f26bf4da16fdc4eec8b087534150b52237c0f603b8e571890a9`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43053646b918ed9c5822c17ca4869f057851bb96fcaabed794a5a7ec36dba34`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92515b32642bf33db09f5042274a35b3bf9dfd52f33a78bed3ddb0efab90867`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 29.2 MB (29169219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cececc96a315d5d1a226bb3d06189757c3df3f0bf808c3089f6a8c1ee57b169`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed191b05c95c8ec8e47091054ba961bb388402c18feea2659c81884ca0fa7f5`  
		Last Modified: Fri, 25 Oct 2024 02:10:40 GMT  
		Size: 853.8 KB (853787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5e376500c1dbf9e6b542bbd48cd51904faf1049e0278e1c2b18582fa895d55`  
		Last Modified: Fri, 30 Aug 2024 21:20:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5dd5a156fcf33f2f2b2c422187fca3ec4e062527208363db00209c5d247cd2`  
		Last Modified: Fri, 25 Oct 2024 02:10:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:566b52046428f961915055348dc32675f9f0a252eae9044bd8056bf344b89e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ee22fc3f09f77778664430a1e7f4a8c6a043e27dbfe289bb67071b9283f00e`

```dockerfile
```

-	Layers:
	-	`sha256:2044d2bfcf3dc71173e00b789e1fa37302fa2b612ef96744043e8c47ebfe93d5`  
		Last Modified: Fri, 25 Oct 2024 02:10:39 GMT  
		Size: 30.7 KB (30744 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v7

```console
$ docker pull composer@sha256:d9db427dd0ecd3160889132e21a5035797c127ed6c28fc6562dcb9a09e98ff91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65813047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2435769ea993c3e67819438fac854d4356d5615d3297d6443a89408d240ad1f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12c01d5f758f7fce28807153dec7a85ae2e307cf0d73f644d575cd875cb994a`  
		Last Modified: Fri, 06 Sep 2024 23:45:25 GMT  
		Size: 3.1 MB (3079568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c3e48f803b4ca0c1ec0b16f85f80f0a17b054845918112eb73b80eb9bd7297`  
		Last Modified: Fri, 06 Sep 2024 23:45:23 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7c21bdd57d9b7548f08c79a56f0a75d4e14a705967ae55d0450a10f0c6c43e`  
		Last Modified: Fri, 06 Sep 2024 23:45:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efe62db4f1f9f85f795e6cc1e7f8d835b0a8657d2a60143ba15d82d5863841`  
		Last Modified: Fri, 25 Oct 2024 02:37:26 GMT  
		Size: 12.5 MB (12504680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204359c9c9eb5cb76578981a5c068e3fac227ce0e7df1a86096569dc1230c85`  
		Last Modified: Fri, 25 Oct 2024 02:37:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2762620a9d567bff0020a3cda73a630f1a993bda6921efbd9554d75c9fd3377f`  
		Last Modified: Fri, 25 Oct 2024 02:37:28 GMT  
		Size: 17.5 MB (17478737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5a9688a15e4908bcd1ed18d76acd39f8678dd66decafbae483b2c884bf1c02`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66727798fd727eda6cfc82ff904b3773b442a67ae9e11967aac36d92e2e9be32`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ef898d316952fe64642bc94179ed2cc82e7c9404af0c91e8d0f5152097b5e8`  
		Last Modified: Fri, 25 Oct 2024 02:49:33 GMT  
		Size: 28.8 MB (28797969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48238d159943a0389cdf60849c19e218b8aeae434d69dfb9050fc0c71115bf9a`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4000b86640b910da67da0e0591b928b9814cab709f524c3dd116813edb020a`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 832.2 KB (832204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14448e76a87db89051e8c674c25c620592e20e601c5226e51e66ddad741a1abf`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2aded8b7a18a66a577aaca7215b0432641184fa882da02e64aa3019fb4ff43`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:a4e13b8dc804db99d2e5742cd1a7b106f85e35472e0be2f2dc36994a5293cbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbef1edcca25baa697af6ac82d649984278e4c8d5106b6732284be72a2d511d`

```dockerfile
```

-	Layers:
	-	`sha256:246718e2cc2b7267e00ae2ef31cc11a59866ee83cc1bcf8c0e568d838c185aee`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 2.1 MB (2146616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2db3fa5cb3eb40a40a6458915a921720bff3778fed84e05d2d68c0906ce947f`  
		Last Modified: Fri, 25 Oct 2024 02:50:25 GMT  
		Size: 31.0 KB (30959 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:ed610a3ecc8a6641ff6f6f7140e51d4237c5a1375ce4fdbb72bb568e0e5f4364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72632568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93292c1520920760b20d22bb2b46e73891fee9345ee4739813bbb65f8986c4d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ef8ad75958cd7eb0e453d0f85e72134ef3976f8351b5742370df35bc60ed42`  
		Last Modified: Sat, 07 Sep 2024 02:23:50 GMT  
		Size: 3.3 MB (3333388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f80c1299f6c626e7df88761199f03734cced725870be7a04dd95bf11e80104`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb3615e2ca5466e128fbfbd9bfcaa4cc0a7c5935f1d980f13d765c6bfde9144`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b324dba8535eea2357b994da9864afef849388a4c8e80235090810383253f31`  
		Last Modified: Fri, 25 Oct 2024 02:19:36 GMT  
		Size: 12.5 MB (12504686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e479347c3f32eee03df523edd0f1a869f7a7636702922f9d5db1ac9024ea211`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6b8889455c447cc20eb2d9881a51c22cdac63cc440a2e647d8e5c2c7f13cfc`  
		Last Modified: Fri, 25 Oct 2024 02:19:37 GMT  
		Size: 20.9 MB (20940181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eeecc80b8f4736452eb3054bbf21ee480f6a4eb724b114b31cb94ab034f53c`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93069ffa1c1f8ac20ef6e8c62fa71d5ba3e5ae3f4ce6b97965ae1a5a0f2562bb`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98eea5daa433de13908b8daf3e98a58f41b648a198629693556299898d3050f`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 30.9 MB (30879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24933c1ee11a72c73a8c1d127f5254b2e1a343115700bfd5d40922a70347acac`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf17e219c699a2a72db781cffa3cc64fbf596fc72c55200fc286d9cdc8a4705`  
		Last Modified: Fri, 25 Oct 2024 04:24:52 GMT  
		Size: 862.6 KB (862632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce14b2b504eda344744c47bb683b1426b0fa486fabbfac2faa8105f727b08582`  
		Last Modified: Fri, 25 Oct 2024 04:24:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44f751e33221265625049db5a9c83603ddb0fb5a864f1fa1b741ae4c742bbbc`  
		Last Modified: Fri, 25 Oct 2024 04:24:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:a03c0f41e4217425cd386b0abe60fd531d6888584099ec45ba13a2cf3b0b8a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4319f087567573fd62e91b1ce51f33931f4db67de0100145586025faf5c134`

```dockerfile
```

-	Layers:
	-	`sha256:478665d61d84e761883072a907b1babb5b42cdc0c775a8d5ba85404d43e2b544`  
		Last Modified: Fri, 25 Oct 2024 04:24:51 GMT  
		Size: 2.1 MB (2146442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f598d25220811662bfae672ca57be5fde9a89c368c0a2ab0c5cb86d44dfdc22`  
		Last Modified: Fri, 25 Oct 2024 04:24:51 GMT  
		Size: 31.0 KB (30987 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; 386

```console
$ docker pull composer@sha256:a74e7cd69fd5fdf58574ec5d7c5ba3b5ffb23be88ba39fe8c361b9f1f55a9206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52269419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecea442e97de0232c1d214efef1edbe4687f4fc157a2e1d85e26068b337d4b2f`
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:9eaf7c1d9791c6b12392f1f767948304f2c2e69cb0878ecec4d5df2be5af4dca`  
		Last Modified: Fri, 25 Oct 2024 04:22:20 GMT  
		Size: 12.5 MB (12504687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0bab9c844ca004a8fd6a7ea2a92c041012b047b66151b6d55f81e1e29009e`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609f4e456e59a3c94a5761b23648a66de98737427aa781c0b05b3296eacbef62`  
		Last Modified: Fri, 25 Oct 2024 04:22:23 GMT  
		Size: 20.8 MB (20818182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4455a0ae1ac0aca52a62943181a6673cf4e49459913cfea722ceb78acf98f28`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f23e94c0f2162ee0e26724220289d3609acb53f3117201cba2c8e6e5021efa`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 19.7 KB (19716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25461fdabdaef5271efc2bf4531ff19b94cd8934b3dfe7e2bf418bbb32d81a7`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 11.3 MB (11281334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abe68ad0ebdacbb851f9b459540ab25e692e7abc15e3721edf9cecaa068ea94`  
		Last Modified: Fri, 25 Oct 2024 04:50:04 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9246e07d5803105355a4670352210146b67c5b7d2f342f72914d58b29f471ec3`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 839.5 KB (839495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41663d1945b422f424a070ec2890346fea5b814db683465fc82753da7a2420d1`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093e8579d9a88d2e6e4ad28e98f7c9af167da1e1c31511762afe8054b11d5a20`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:8fe92421f18332515e4db68490c13084c60405d2ee845b57eacf8b7c3d6f42a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.8 KB (450820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c9e925c5e713f40e117a305965ac065ca3f71ce1e8c2be703f4877e3500883`

```dockerfile
```

-	Layers:
	-	`sha256:09f9d01c8587517a625b0a1e78c7cf0dff1705643497fb4d296b5cd6a15f4bf0`  
		Last Modified: Fri, 25 Oct 2024 04:50:05 GMT  
		Size: 420.0 KB (419977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:938747e2e36d8485f56f42361e570ac17bf8e1be1457b497896de59af4695ddb`  
		Last Modified: Fri, 25 Oct 2024 04:50:04 GMT  
		Size: 30.8 KB (30843 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; ppc64le

```console
$ docker pull composer@sha256:60bf2a71e3119e87187524f7e43e94e02d87237213ebd155e726e293cd5a5f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73070409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04dc7b892f59b50da40d47ba44723f21a51ff8123144cebdabcbfccc6642c416`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac727a268c34206d27f9588c3acfc276afdaf0623dfdc19b7d210a7a881ee4`  
		Last Modified: Sat, 07 Sep 2024 01:44:58 GMT  
		Size: 3.4 MB (3408322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564dcd8f1c226aa29a92bf07685b2a44ccb8ac47267a590bc34a56d25bbbcc4`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3867a87b0703f924c2a7915ce891a49d11c61af6d01613564e485431a9f78`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8622608d41f825e14aa5bd26799c3251549bceef128cf2eae2f52f1ab78913e`  
		Last Modified: Fri, 25 Oct 2024 00:57:34 GMT  
		Size: 12.5 MB (12504690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b9b2cc7fa22223c46604afd8fd56f225e535ca1e7d006d545233f411a4a3c0`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9400d92782aead1169d2e61549cc961ef18b1a2f1468fe9a486ae165d901cf6b`  
		Last Modified: Fri, 25 Oct 2024 00:57:37 GMT  
		Size: 21.3 MB (21285751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ccc474f40266b6e9c07bd2bd8edf9b2feccdf7986579f0a7bfa017cb90929`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd3a52d6da309a1907e5c8310c6411753ee8823a82029f55b265da24bb7566d`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b86ce86d7510dbd92b9dd787d737ff21b3ba726f05cb8546ccc581875d372d`  
		Last Modified: Fri, 25 Oct 2024 03:09:39 GMT  
		Size: 31.4 MB (31402604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74408fea44fbe8cb944832b386c9752e053e23539d049cfad4f03cac46f658f4`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba1f53a13e206b75025635546b42294f43407b4c0886512adca06f601c2d1c2`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 872.3 KB (872261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed73246db39a2f37864d4704852e731f1b98355a71cbfa582403452373a16a5`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7625397ca17be19f2ac1493062a678c2c27fc506926706292d9ec948080a95`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:b33917e7935b007beaa0ad8312f53fb782d5d50661a412557d64f940e0455b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a15032ba46bd6c66199f174035eeffe14fd7a9ebf8376ddab4f579ba83bc77c`

```dockerfile
```

-	Layers:
	-	`sha256:99be6629a5a89524b622be0403f011e5d36005d75ef65ce0b420f9743eb44f9c`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 2.1 MB (2144852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbadc54b255987b5a8cd0e61cb4086147d53a9f8a474693e60bf728686d39a7`  
		Last Modified: Fri, 25 Oct 2024 03:11:31 GMT  
		Size: 30.9 KB (30907 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; riscv64

```console
$ docker pull composer@sha256:95d42f5c8e075cb1a6d6669ea2ea22e58a1f89df5a716b820a1a124323c06872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70766351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e4f9b56f9bc2f90c3c24fa4fc25128df1540eb56e212ecaeaf7532af9c550d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160a71fe2c21fa0be03f4ecb3856d46307a8cab34f0749e89c452111c128a28e`  
		Last Modified: Sat, 07 Sep 2024 09:00:45 GMT  
		Size: 3.4 MB (3405216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99de0cdf41fffa764363801fb8a9efbd008b3689317846613f74f55be82ad4ec`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4878284381f1e57d12b980a3d3f2476a10fab26827866948f61cc0a2214a8`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d60d72a55a97ca66240c87e7bc1886bc5aa87d97579097a6d9bab88a75ae1d`  
		Last Modified: Fri, 25 Oct 2024 06:19:30 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55404ef143ec5be664bfb8b7d19253fad3452d91340eac96ad5cb7f88c34e9e`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f1fc6d05b292475d5cdd272dff683e4226cec9930f2394a99a2af5ad9a19c`  
		Last Modified: Fri, 25 Oct 2024 06:19:45 GMT  
		Size: 19.8 MB (19785919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f47a3a529d11fa207f1e96b631df8f8334701948d58152ac5419e07ef6f0b09`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5729eb71e7d125b843a7ed55653966533b980fcc3e19e4ee54ce1e25042a67`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d654c394fa744c0d5afc76db22431671980aa34529d74f487cfbb8e0857966`  
		Last Modified: Fri, 25 Oct 2024 09:50:35 GMT  
		Size: 30.8 MB (30811074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a58738e9c21fa9035cc24b974c8d99fbd269320abe6e366312beca87fb36e14`  
		Last Modified: Fri, 25 Oct 2024 09:50:31 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f99b08fe380cd3433f0a674009aeeb2859b0cdb7c42519d0c60d88c6eb2c8`  
		Last Modified: Fri, 25 Oct 2024 09:56:42 GMT  
		Size: 863.6 KB (863608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0527c2bf443290d937d302528997d29b7dec46cd4410f5cae140ffa4f5c9ce2`  
		Last Modified: Fri, 25 Oct 2024 09:56:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f0bed4782113f2e7ce0e0432be8b7bac1a2ccc30fc5131b48455511d554f5c`  
		Last Modified: Fri, 25 Oct 2024 09:56:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:ff74fefdefb013a70685728720daa95fe9965ea537761c5edfb3f1aff8edbe64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747348917de585d7f71dc6a64690f3016da998e5df6b8021758d8956431b5dc9`

```dockerfile
```

-	Layers:
	-	`sha256:9d4d21d439313124a4cdca34dcb6e825c4fa632adc4588d62d233059db6800e5`  
		Last Modified: Fri, 25 Oct 2024 09:56:42 GMT  
		Size: 2.1 MB (2144468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7831cdcc0293a4668d3f1b7fddf19ff875fed1b0de3846e082d27a232eca63ba`  
		Last Modified: Fri, 25 Oct 2024 09:56:41 GMT  
		Size: 30.9 KB (30907 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; s390x

```console
$ docker pull composer@sha256:ba0b51758570d1603c9d1a79e79d9984ea17d4ad71122de39631718e8c33b4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72096610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea189f687ac3a4235c4e5389a9b69c11e999d208d08cd08920892c75ff1926fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9208ede8519d248128a660ad6cbef1b3a33b141374be176c946b5b17b2968ab4`  
		Last Modified: Sat, 07 Sep 2024 00:42:38 GMT  
		Size: 3.5 MB (3473993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabbdadb2babb53e22b8c60bffa37b66bacdd1495093eec38748ca15dabc8287`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2431f4d7c348124f66281fa6433fdcded6e6a093aedb9cdd6fa9c7d87a1407`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8632e206b7bc36b0bfe226c5ec5e94154bc411b3677a2903f0f33e8b4d06d3`  
		Last Modified: Fri, 25 Oct 2024 02:46:23 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950b6d1374ddd91229978b32c87237f1a304df6908d46a3e6c6617379120ecb`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fac98b72a50f285d80ad08584ff62de41c8b0ea0276e5187d77f6dddb0430e4`  
		Last Modified: Fri, 25 Oct 2024 02:46:25 GMT  
		Size: 20.4 MB (20422987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17a61d0d2aae412d208b48c74e3754c9fc7b3f3d0644186eb5a952c01d1d01a`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c55de606062f9878f968213cb2af563401f158dbc5f7b5612b565d5f23a8d8`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a65e35183739b8872e800265ad579948004dd6060f487f2295911c401548795`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 31.3 MB (31338414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c5278f124e717ca16fc2677a7e92e4331ffd330679687f8429c052a4980ca6`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575557973f7add04a1a089c7862055c2c98ccda37474518502ea9a3dd722f89e`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 870.6 KB (870554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a02ba86566b001eebede2109925bcfacc44641549c7f5759627d94b6a722ae7`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09679b42c54f9c7976c72332e47ad04bf18c71e234c858f1713b6b3ff3732441`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:da66ffbdca6aa99a270caab47a9f9add1d9e6cf051e77f358ce4ab39df5efd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dca5383b013776298de61e007d592faaf498b949df992085e5f91374e3c24ec`

```dockerfile
```

-	Layers:
	-	`sha256:fca8df5fe3ba4a227fca2462dc0d8f7319acc477162c6c4fd9b659e96290e261`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 2.1 MB (2144254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa0a55e7ab0b0c78adde359808fe61c606a81b1b7e14cfcd33ff0005bec05aa5`  
		Last Modified: Fri, 25 Oct 2024 06:39:32 GMT  
		Size: 30.9 KB (30871 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:0d9ed84312bc8f0094c372b5074ddf89abffddd6e8b91d46f9d39f98cbd512b4
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
$ docker pull composer@sha256:a92e127cbf279c3b76b3f7a20bc4185c20d8d9b2124ed9e14ce2864d5732541b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71404941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8beffceb940b8587644cf8b44117807db3310b81a15145274e979407fdf7789c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 00:32:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Sep 2024 00:32:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 07 Sep 2024 00:32:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 07 Sep 2024 00:32:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Sep 2024 00:32:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 00:58:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
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
	-	`sha256:41457434eddc5cb99259de159d6a2dad43029452b1ab35975a3209703b9897f4`  
		Last Modified: Fri, 25 Oct 2024 02:16:38 GMT  
		Size: 12.5 MB (12504689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328056f851cc57837c30c7c30c8c1fba0e538db1bdb0f520508b064b7771388b`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66dabf5a41275ff903a5f9ccc8ba9ba981ff4f80da78ac30a649f683542b98c`  
		Last Modified: Fri, 25 Oct 2024 02:16:40 GMT  
		Size: 20.5 MB (20518417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab768f68c87e7a556fcaf812a92acd5c8bf122cc606c956394a6ec4bc208f0f1`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b263e76cc797a1f79fdee350bf8047c4fae8cea974168046c693eec0894545`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8c6e46e9e203f16f774d50fa9cee35406c7828c4fb2f3fe24a868e8cdbe576`  
		Last Modified: Fri, 25 Oct 2024 02:49:45 GMT  
		Size: 30.4 MB (30368357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b27fd7d7d1f5948b1fbe2965594f3bcce94435155a4c35a60b2d608d5ea2fd`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e9f4aa8790c6e63ad881b3900ab9120ea46bad338a9f9dc641af2fb1545dc8`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 1.1 MB (1082386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0fd2babfe1056ad805d84256fb3ec3d62cbaa0be56261a2c2c79a55c100052`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844c7c8ba204421ae47d0e4129dad01122cef45bef67ab49236fe225f2414e48`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:07e9c44c65d288981528af88e5f1ea62f7a8c5f6c4b047fb70b5ced53a2e17d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea337cfabf9cc40ac248aa582e15c6274d46217f1dd85555f1e5d03dd0cf1a8c`

```dockerfile
```

-	Layers:
	-	`sha256:2c8925f43dd72726464493496debe8d9254a2f386420933c92b82b7e17328db8`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 2.1 MB (2147788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac23cb17204e28cf366d9ea488f6d59fad0bc9ebb7c72a01b9f405bcc7ad7f9`  
		Last Modified: Fri, 25 Oct 2024 02:49:43 GMT  
		Size: 31.2 KB (31168 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:0731814f66fc6c48bd0c0807e80c89dc2e55e00fbb2f0f313bb22c127f7dd22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68128183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a45cc575b5b053051af22c57e1635b28ace0c5da57cd7994fc69278fc802ca0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:30:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:30:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:30:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:30:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:30:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:51:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78c7a9de9941e89cd785fc3ad14f52410d858d2259f5c9b2a852fd144612520`  
		Last Modified: Sat, 07 Sep 2024 00:48:55 GMT  
		Size: 3.3 MB (3269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbf8fddbe2a872480c609959838de42e95d1f5d5d3d8daadf7a1e44e5c381a2`  
		Last Modified: Sat, 07 Sep 2024 00:48:54 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d88511b2a3086248129999917d9f1e5928426fda8f08edf40ab5bafa37a9`  
		Last Modified: Sat, 07 Sep 2024 00:48:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2913caf4eeb0b47e0a269d5500be80ad644b55b830987923b9b25d7c47b779b6`  
		Last Modified: Fri, 25 Oct 2024 01:12:37 GMT  
		Size: 12.5 MB (12504684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd40e2319cfc199b8ddae2c1022299e653810d5c8fcff021ecf9e71bc732119`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8662dfadda858bf306da862403b12c0ebf0c2c06e8cc29019a10cec84a7ec93`  
		Last Modified: Fri, 25 Oct 2024 01:12:41 GMT  
		Size: 18.7 MB (18711875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0edc47bdf53f26bf4da16fdc4eec8b087534150b52237c0f603b8e571890a9`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43053646b918ed9c5822c17ca4869f057851bb96fcaabed794a5a7ec36dba34`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92515b32642bf33db09f5042274a35b3bf9dfd52f33a78bed3ddb0efab90867`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 29.2 MB (29169219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cececc96a315d5d1a226bb3d06189757c3df3f0bf808c3089f6a8c1ee57b169`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84dd6a8db95fd1cfab72745b588a6020c64ae5fa5e8e7eaf34da667e8998ebca`  
		Last Modified: Fri, 25 Oct 2024 02:11:27 GMT  
		Size: 1.1 MB (1081742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc448f86c117926316d64dc1703afc82d359157f79799cf045e2b86d86c667f6`  
		Last Modified: Mon, 07 Oct 2024 19:58:17 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53acd091d4bf5494fdd8f48f0cbdf90b0375e550a50197d0537f794786e4f735`  
		Last Modified: Fri, 25 Oct 2024 02:11:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:c70376116be9359f8d20e30b55fa4d81f4c5be21b3c1a64c07bb4141515b2ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56b4a57a86ddb1abdf163141d4bd42e27c5f5a4625178f8ea5a460ebe63b6a7`

```dockerfile
```

-	Layers:
	-	`sha256:f8dc929d2da75915ab1de51553bc89259f0f9e61645d119453a123ede1024cbc`  
		Last Modified: Fri, 25 Oct 2024 02:11:26 GMT  
		Size: 31.0 KB (31049 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:ff5c72f99787e7cd316fcc4395d97f53f714b04e6a96670c7af40a72e6f4be4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66041602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9624095698de01d4e75e21a48773fbb0d30e5fdca551bad82d4a57860f49e51`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:29:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 22:29:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 22:29:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 22:29:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 22:29:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 22:29:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:29:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:29:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 22:47:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12c01d5f758f7fce28807153dec7a85ae2e307cf0d73f644d575cd875cb994a`  
		Last Modified: Fri, 06 Sep 2024 23:45:25 GMT  
		Size: 3.1 MB (3079568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c3e48f803b4ca0c1ec0b16f85f80f0a17b054845918112eb73b80eb9bd7297`  
		Last Modified: Fri, 06 Sep 2024 23:45:23 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7c21bdd57d9b7548f08c79a56f0a75d4e14a705967ae55d0450a10f0c6c43e`  
		Last Modified: Fri, 06 Sep 2024 23:45:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efe62db4f1f9f85f795e6cc1e7f8d835b0a8657d2a60143ba15d82d5863841`  
		Last Modified: Fri, 25 Oct 2024 02:37:26 GMT  
		Size: 12.5 MB (12504680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204359c9c9eb5cb76578981a5c068e3fac227ce0e7df1a86096569dc1230c85`  
		Last Modified: Fri, 25 Oct 2024 02:37:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2762620a9d567bff0020a3cda73a630f1a993bda6921efbd9554d75c9fd3377f`  
		Last Modified: Fri, 25 Oct 2024 02:37:28 GMT  
		Size: 17.5 MB (17478737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5a9688a15e4908bcd1ed18d76acd39f8678dd66decafbae483b2c884bf1c02`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66727798fd727eda6cfc82ff904b3773b442a67ae9e11967aac36d92e2e9be32`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ef898d316952fe64642bc94179ed2cc82e7c9404af0c91e8d0f5152097b5e8`  
		Last Modified: Fri, 25 Oct 2024 02:49:33 GMT  
		Size: 28.8 MB (28797969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48238d159943a0389cdf60849c19e218b8aeae434d69dfb9050fc0c71115bf9a`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b58a4408498db5e9ab01414bd6385d998cb8f21dabb6be95a750906ae5b1f3c`  
		Last Modified: Fri, 25 Oct 2024 02:51:11 GMT  
		Size: 1.1 MB (1060749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6503f2fca1c6898aa87f48db0cd634630c52a3268995b25f8caffb8bee8475a`  
		Last Modified: Fri, 25 Oct 2024 02:51:10 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fabf1a07b3bdac00b08274fdd1b79967aabe3c4f6526c99bd7c80255a9c5c07`  
		Last Modified: Fri, 25 Oct 2024 02:51:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:29a9862fa241870ee9e9744c1234cb68935ff206aa43236d0f21de7a297aa903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38703114d6a9c5f9de4eeae5759012126d06ad4b07f8ce0d8348157c7a9c8ff`

```dockerfile
```

-	Layers:
	-	`sha256:d1bb5967213b8eacf025fbae03caf581e6326e1e330d4c01ebb58cbb27eac34e`  
		Last Modified: Fri, 25 Oct 2024 02:51:10 GMT  
		Size: 2.1 MB (2148109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b80953e51404205596c003a9bf2f30426361239bd88f3d5879f028987ab723e`  
		Last Modified: Fri, 25 Oct 2024 02:51:10 GMT  
		Size: 31.3 KB (31264 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:4575910a0d4a9df7ffd9da094b4d4e73f4a2be32d36246e7329d623454ae6329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72860831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3c631a63beae9b8ee7bcc06a3f14113fb4fc0765bc591470a50ddcb080bde6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 00:43:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Sep 2024 00:43:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 07 Sep 2024 00:43:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 07 Sep 2024 00:43:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Sep 2024 00:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 01:04:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ef8ad75958cd7eb0e453d0f85e72134ef3976f8351b5742370df35bc60ed42`  
		Last Modified: Sat, 07 Sep 2024 02:23:50 GMT  
		Size: 3.3 MB (3333388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f80c1299f6c626e7df88761199f03734cced725870be7a04dd95bf11e80104`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb3615e2ca5466e128fbfbd9bfcaa4cc0a7c5935f1d980f13d765c6bfde9144`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b324dba8535eea2357b994da9864afef849388a4c8e80235090810383253f31`  
		Last Modified: Fri, 25 Oct 2024 02:19:36 GMT  
		Size: 12.5 MB (12504686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e479347c3f32eee03df523edd0f1a869f7a7636702922f9d5db1ac9024ea211`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6b8889455c447cc20eb2d9881a51c22cdac63cc440a2e647d8e5c2c7f13cfc`  
		Last Modified: Fri, 25 Oct 2024 02:19:37 GMT  
		Size: 20.9 MB (20940181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eeecc80b8f4736452eb3054bbf21ee480f6a4eb724b114b31cb94ab034f53c`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93069ffa1c1f8ac20ef6e8c62fa71d5ba3e5ae3f4ce6b97965ae1a5a0f2562bb`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98eea5daa433de13908b8daf3e98a58f41b648a198629693556299898d3050f`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 30.9 MB (30879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24933c1ee11a72c73a8c1d127f5254b2e1a343115700bfd5d40922a70347acac`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b210b09c1b5dce1b5094e57caea0452e5776bb3f43f7c8d5e388cb69ced01d44`  
		Last Modified: Fri, 25 Oct 2024 04:26:34 GMT  
		Size: 1.1 MB (1090886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b5d0e63e39d147a5ff8487e68431854584ec90cd07275ae0a841e77cd539f9`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec155f53f4ab45bdf10f33bb071a35ac7b7777b50897579201c20b6fc9223dec`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:f165a4ca8adb8f345a4fbbd2d0e6ce7423ff3cccbe80bc6b4f74cd433103cc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732da8b9d36aadf2652af89a530a393a085bba4c677c1b4310dd4bb506d19e83`

```dockerfile
```

-	Layers:
	-	`sha256:84135c99834ab363c853372259a9196b615745b6251e3f49a3b9ae0f2786b92a`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 2.1 MB (2147939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9042f9e0e6a93e08e64a8eb7f1f3caba691460c8068e0cafe27485b1de12b43`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 31.3 KB (31296 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:62aac98b8ddd75628e726dfa617ad4cb8999c542b5694731ad2a759ce8db7f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52499599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3c0137caf6333752ae7e9a4c6dab56a54051e5561cd9e4eb1bf546ff340517`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:57:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 22:57:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 22:57:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 22:57:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 22:57:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 22:57:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:57:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:57:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:42:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
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
	-	`sha256:9eaf7c1d9791c6b12392f1f767948304f2c2e69cb0878ecec4d5df2be5af4dca`  
		Last Modified: Fri, 25 Oct 2024 04:22:20 GMT  
		Size: 12.5 MB (12504687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0bab9c844ca004a8fd6a7ea2a92c041012b047b66151b6d55f81e1e29009e`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609f4e456e59a3c94a5761b23648a66de98737427aa781c0b05b3296eacbef62`  
		Last Modified: Fri, 25 Oct 2024 04:22:23 GMT  
		Size: 20.8 MB (20818182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4455a0ae1ac0aca52a62943181a6673cf4e49459913cfea722ceb78acf98f28`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f23e94c0f2162ee0e26724220289d3609acb53f3117201cba2c8e6e5021efa`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 19.7 KB (19716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119b4f99527dc6b667937203167ecff4617fc1078093fefa09df11b56496bf86`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 11.3 MB (11281335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbd8ee9662704273444a11a2628a08c55058235539da3ea7e96f3be43027311`  
		Last Modified: Fri, 25 Oct 2024 04:49:54 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982fbbf47d3c6ccff37f0a09b37729d82c7be79b8418a3f9890760f66666dc11`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 1.1 MB (1069665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b690f8f3106cb91a4c9197600b5e08e921bd5e48167d98cc698e9b0a085932a`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba53d57ff746cd2ddd87d6ced854a49c95ff92a78a41be2558d7a03fc458d45`  
		Last Modified: Fri, 25 Oct 2024 04:49:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:b05663c6150f09f5c8cc8b3e66d66d5f7decf8d4a8e6501c5fc07ac0bbf1cf02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.6 KB (452592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767141b0e93d0dd0919fa135fc78c8810e5b45b3fd3a831748335d78739fdc15`

```dockerfile
```

-	Layers:
	-	`sha256:bdce856b61660e66f0a1aed4d46ce39f3daa23773798f7a159f6f932a8c99052`  
		Last Modified: Fri, 25 Oct 2024 04:49:52 GMT  
		Size: 421.5 KB (421457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:172b30ef88591f77f9105b14ce9ad0ecf845d37ba979e1a51d7522746131a64f`  
		Last Modified: Fri, 25 Oct 2024 04:49:52 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:514d02ab64c17c9661db088c7bd01663e131e812fe045faa21c2bc31fe3d14e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73298747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615d60ab2fbdfd79a1d5e5a420e377c65cf49849451d90d947acbabc776ecf0c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:15:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:15:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:15:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:15:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:15:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:15:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:15:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:15:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:59:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac727a268c34206d27f9588c3acfc276afdaf0623dfdc19b7d210a7a881ee4`  
		Last Modified: Sat, 07 Sep 2024 01:44:58 GMT  
		Size: 3.4 MB (3408322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564dcd8f1c226aa29a92bf07685b2a44ccb8ac47267a590bc34a56d25bbbcc4`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3867a87b0703f924c2a7915ce891a49d11c61af6d01613564e485431a9f78`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8622608d41f825e14aa5bd26799c3251549bceef128cf2eae2f52f1ab78913e`  
		Last Modified: Fri, 25 Oct 2024 00:57:34 GMT  
		Size: 12.5 MB (12504690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b9b2cc7fa22223c46604afd8fd56f225e535ca1e7d006d545233f411a4a3c0`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9400d92782aead1169d2e61549cc961ef18b1a2f1468fe9a486ae165d901cf6b`  
		Last Modified: Fri, 25 Oct 2024 00:57:37 GMT  
		Size: 21.3 MB (21285751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ccc474f40266b6e9c07bd2bd8edf9b2feccdf7986579f0a7bfa017cb90929`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd3a52d6da309a1907e5c8310c6411753ee8823a82029f55b265da24bb7566d`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b86ce86d7510dbd92b9dd787d737ff21b3ba726f05cb8546ccc581875d372d`  
		Last Modified: Fri, 25 Oct 2024 03:09:39 GMT  
		Size: 31.4 MB (31402604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74408fea44fbe8cb944832b386c9752e053e23539d049cfad4f03cac46f658f4`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a2527a077a4616f721fa663d0ca3489ff9339802683a454f33b02dc6f3a5ef`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 1.1 MB (1100590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5c0b62db8c3bc2c36a0f17863b36a9da96fecd16d1a11bb1c7bf4a3b8d0cd7`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7567addbbdfe6e8636a200946db7a20e451b5dc0b427ed4c7f7e94676d4512`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:69aa48fe58658360cfb45c08a2c949bc3df95a17f5976a9a53ad335c4975e49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be82f43a76d2877c96c039cebe054f9492a94289537f65c05cee1723c18f2f90`

```dockerfile
```

-	Layers:
	-	`sha256:b8018d8ff9cfcaa1e7981ccd02fbd578df967e6fe88a67a69cb534170a840689`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 2.1 MB (2146343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d004ece9537d1fca87b30c996e372e9be5d9d107c20b6330d54bdfcedd4b43`  
		Last Modified: Fri, 25 Oct 2024 03:13:24 GMT  
		Size: 31.2 KB (31210 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:b85847218fed0f16adfe08f5033a1bb3af32a56c8c5673e6d02addb24b5a0e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70994586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f832367514159c2134fdd37035ec3e2cca2a3910dac92396623338265832020`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:47:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:48:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:48:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:48:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:48:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:48:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 02:23:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160a71fe2c21fa0be03f4ecb3856d46307a8cab34f0749e89c452111c128a28e`  
		Last Modified: Sat, 07 Sep 2024 09:00:45 GMT  
		Size: 3.4 MB (3405216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99de0cdf41fffa764363801fb8a9efbd008b3689317846613f74f55be82ad4ec`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4878284381f1e57d12b980a3d3f2476a10fab26827866948f61cc0a2214a8`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d60d72a55a97ca66240c87e7bc1886bc5aa87d97579097a6d9bab88a75ae1d`  
		Last Modified: Fri, 25 Oct 2024 06:19:30 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55404ef143ec5be664bfb8b7d19253fad3452d91340eac96ad5cb7f88c34e9e`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f1fc6d05b292475d5cdd272dff683e4226cec9930f2394a99a2af5ad9a19c`  
		Last Modified: Fri, 25 Oct 2024 06:19:45 GMT  
		Size: 19.8 MB (19785919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f47a3a529d11fa207f1e96b631df8f8334701948d58152ac5419e07ef6f0b09`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5729eb71e7d125b843a7ed55653966533b980fcc3e19e4ee54ce1e25042a67`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d654c394fa744c0d5afc76db22431671980aa34529d74f487cfbb8e0857966`  
		Last Modified: Fri, 25 Oct 2024 09:50:35 GMT  
		Size: 30.8 MB (30811074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a58738e9c21fa9035cc24b974c8d99fbd269320abe6e366312beca87fb36e14`  
		Last Modified: Fri, 25 Oct 2024 09:50:31 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a9a1e4fd8e3bf5b73e9bba70b3e759e3a9d62b4f8080b8e7b7736c9f348d7`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 1.1 MB (1091833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c042c1d89021264e3a0e83d52ac888997c99220d598ac2eab13ab9c70a716d`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d024f2c5a6071b7c47d8215d6863b5debb180ccf8cb3fabcdd49f7f4e356275`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:ed96702ad5984311f8f58c099ddca3ecd95815043cd65fff7932e96466d3bdad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695236301c163da8ea46b617897966c76d78801c85a766096edea8496bc2ca88`

```dockerfile
```

-	Layers:
	-	`sha256:f8c3581250db3b3d15f4ff5f70365568b7dc495a10d276d3ba4c65caaa52a8b4`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 2.1 MB (2145959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b41aa3f4db744694fac0b293d66cc0a5f4065b53d8145d57fe3db9f9dda1515`  
		Last Modified: Fri, 25 Oct 2024 10:02:49 GMT  
		Size: 31.2 KB (31210 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:ea9eaad310b7a1eb6e71a04d999fff99df034c4e6e3cab0143fd27bfe4b485ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72324825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6321a175cb81ff121817f97d578326ba1fd54ea787a0beaa2cb91695fc662418`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:21:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:21:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:21:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:21:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:21:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:42:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9208ede8519d248128a660ad6cbef1b3a33b141374be176c946b5b17b2968ab4`  
		Last Modified: Sat, 07 Sep 2024 00:42:38 GMT  
		Size: 3.5 MB (3473993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabbdadb2babb53e22b8c60bffa37b66bacdd1495093eec38748ca15dabc8287`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2431f4d7c348124f66281fa6433fdcded6e6a093aedb9cdd6fa9c7d87a1407`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8632e206b7bc36b0bfe226c5ec5e94154bc411b3677a2903f0f33e8b4d06d3`  
		Last Modified: Fri, 25 Oct 2024 02:46:23 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950b6d1374ddd91229978b32c87237f1a304df6908d46a3e6c6617379120ecb`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fac98b72a50f285d80ad08584ff62de41c8b0ea0276e5187d77f6dddb0430e4`  
		Last Modified: Fri, 25 Oct 2024 02:46:25 GMT  
		Size: 20.4 MB (20422987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17a61d0d2aae412d208b48c74e3754c9fc7b3f3d0644186eb5a952c01d1d01a`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c55de606062f9878f968213cb2af563401f158dbc5f7b5612b565d5f23a8d8`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a65e35183739b8872e800265ad579948004dd6060f487f2295911c401548795`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 31.3 MB (31338414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c5278f124e717ca16fc2677a7e92e4331ffd330679687f8429c052a4980ca6`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac84ea67d37f2f607682a88ba709d3ca1d7ec45ffa78bf119c0d99f10f2b8d`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 1.1 MB (1098760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a848938d0078bf52df4fa2a8e8aa39affeeeda8eec7e20a5223789502a279b3c`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720a49fb844cd885e2f5780d44f0f9463fa2ebf0019ec117c14b3db14a6df2d3`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:25870622ae7e5ca41223a45c6b4697934b29ca8accf161069a09ea9ce2462cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b49fa50dd59377e3482258ce9585d6abc69ea39fb8ffb16cf1bdc4844fd8505`

```dockerfile
```

-	Layers:
	-	`sha256:33f7b202cdb48083456840312ed4b34234ccd718584600e47a3ae6e88fda4091`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 2.1 MB (2145739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d35b36e0e9d0af4df173a651dd2132192a1fac59fa923225d506c76e3c067`  
		Last Modified: Fri, 25 Oct 2024 06:41:07 GMT  
		Size: 31.2 KB (31168 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:46531d95ae84b4d0f44b109d365db86fca10d96d1cfb68999d9541426d89a43e
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
$ docker pull composer@sha256:1b8c7b7803441706a9e04bcb7c23d6c7d5935a6d27d7ab797183700fc4d3cda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71258353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d94b12f6cbd009a3fc780b7b1aa509b42f3a678572dc657b92d63c98ca8db49`
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:41457434eddc5cb99259de159d6a2dad43029452b1ab35975a3209703b9897f4`  
		Last Modified: Fri, 25 Oct 2024 02:16:38 GMT  
		Size: 12.5 MB (12504689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328056f851cc57837c30c7c30c8c1fba0e538db1bdb0f520508b064b7771388b`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66dabf5a41275ff903a5f9ccc8ba9ba981ff4f80da78ac30a649f683542b98c`  
		Last Modified: Fri, 25 Oct 2024 02:16:40 GMT  
		Size: 20.5 MB (20518417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab768f68c87e7a556fcaf812a92acd5c8bf122cc606c956394a6ec4bc208f0f1`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b263e76cc797a1f79fdee350bf8047c4fae8cea974168046c693eec0894545`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8e721d4ec60c167e217985a6634def0773d7c209c854c6cff384ae95d609e0`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 30.4 MB (30368247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482b3b3d18b4f075b12c4319e5dc322215e9ac691e238f09bbf7858afdc525cd`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9323b09d4891470d8d5dbad780102f127ee113898ab714b3cea5a8e051ef7ab5`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 935.9 KB (935910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ede80ac42873d95db4f1e1dc746ab53be2071011ecc8e0df9a2a05d6ff83f0`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9ebd623a6cd55899fbfa1cdbd8ed0b505385fc70414307c27b06e6306c2a50`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:85d2f659fdf26193b06cb76d853c0d73e75ba826c2b5b3d9e44f53aa15da98b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb3aef60fab8f0110068b8032e3b12e726d2978eb062c434b806dcbd8e0fb84`

```dockerfile
```

-	Layers:
	-	`sha256:b704440e485eec60929d9914b7388f77adb483eebc2626931665c90c8ea22b89`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 2.1 MB (2147494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f51685b55e387f4a3da1dc24d977b000fb70421efa45bf9f76f43d84f9c86bb`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 30.9 KB (30861 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:30730658678c13b3fa13492b42fff3265b536c0a21aaa129acc0865633af891b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67981937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa096441dfd2778abfc7be3ff0a8e578eed66f710e8b6b8c94e3812a9c7c87b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78c7a9de9941e89cd785fc3ad14f52410d858d2259f5c9b2a852fd144612520`  
		Last Modified: Sat, 07 Sep 2024 00:48:55 GMT  
		Size: 3.3 MB (3269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbf8fddbe2a872480c609959838de42e95d1f5d5d3d8daadf7a1e44e5c381a2`  
		Last Modified: Sat, 07 Sep 2024 00:48:54 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d88511b2a3086248129999917d9f1e5928426fda8f08edf40ab5bafa37a9`  
		Last Modified: Sat, 07 Sep 2024 00:48:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2913caf4eeb0b47e0a269d5500be80ad644b55b830987923b9b25d7c47b779b6`  
		Last Modified: Fri, 25 Oct 2024 01:12:37 GMT  
		Size: 12.5 MB (12504684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd40e2319cfc199b8ddae2c1022299e653810d5c8fcff021ecf9e71bc732119`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8662dfadda858bf306da862403b12c0ebf0c2c06e8cc29019a10cec84a7ec93`  
		Last Modified: Fri, 25 Oct 2024 01:12:41 GMT  
		Size: 18.7 MB (18711875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0edc47bdf53f26bf4da16fdc4eec8b087534150b52237c0f603b8e571890a9`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43053646b918ed9c5822c17ca4869f057851bb96fcaabed794a5a7ec36dba34`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92515b32642bf33db09f5042274a35b3bf9dfd52f33a78bed3ddb0efab90867`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 29.2 MB (29169219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cececc96a315d5d1a226bb3d06189757c3df3f0bf808c3089f6a8c1ee57b169`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c2e6b61270c266b53490ff499b93ef054fbec927512a281cc7a6b24701805`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 935.5 KB (935497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff00edb04cb0f9ff5be423ef9e64b2cc05ec099877d249544ab29d1038f5de3d`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c6ab539bccdbdb0fcf7fafd68ce2bd97284eab5f8d8abf785cabec35588b7b`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:e4a9826fe50da350c6777297621c260458faba92b526041a376ce79aab8b81b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57b36f19d8ad3b6a6132c9b81dbfc98306a2cd534a3294c6f488017985d24eb`

```dockerfile
```

-	Layers:
	-	`sha256:37078fd6622f6a210d26c2f3f60d602e03823611193b605e55caca850fea26d2`  
		Last Modified: Fri, 25 Oct 2024 02:09:51 GMT  
		Size: 30.7 KB (30734 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:c91cd5ffa3dbabd16ca1a5236effe469f34a169c118f5e08a70364c4028ba35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65895087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5708873007b11d781ab952dd94413afc61e3fb305d253bd5f588a1aa1c3b233`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12c01d5f758f7fce28807153dec7a85ae2e307cf0d73f644d575cd875cb994a`  
		Last Modified: Fri, 06 Sep 2024 23:45:25 GMT  
		Size: 3.1 MB (3079568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c3e48f803b4ca0c1ec0b16f85f80f0a17b054845918112eb73b80eb9bd7297`  
		Last Modified: Fri, 06 Sep 2024 23:45:23 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7c21bdd57d9b7548f08c79a56f0a75d4e14a705967ae55d0450a10f0c6c43e`  
		Last Modified: Fri, 06 Sep 2024 23:45:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efe62db4f1f9f85f795e6cc1e7f8d835b0a8657d2a60143ba15d82d5863841`  
		Last Modified: Fri, 25 Oct 2024 02:37:26 GMT  
		Size: 12.5 MB (12504680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204359c9c9eb5cb76578981a5c068e3fac227ce0e7df1a86096569dc1230c85`  
		Last Modified: Fri, 25 Oct 2024 02:37:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2762620a9d567bff0020a3cda73a630f1a993bda6921efbd9554d75c9fd3377f`  
		Last Modified: Fri, 25 Oct 2024 02:37:28 GMT  
		Size: 17.5 MB (17478737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5a9688a15e4908bcd1ed18d76acd39f8678dd66decafbae483b2c884bf1c02`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66727798fd727eda6cfc82ff904b3773b442a67ae9e11967aac36d92e2e9be32`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ef898d316952fe64642bc94179ed2cc82e7c9404af0c91e8d0f5152097b5e8`  
		Last Modified: Fri, 25 Oct 2024 02:49:33 GMT  
		Size: 28.8 MB (28797969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48238d159943a0389cdf60849c19e218b8aeae434d69dfb9050fc0c71115bf9a`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac4b3d7e0e3d6c59f9af60415c3648615e5a2c56d6abd230155f2bb2576aee4`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 914.2 KB (914234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2f49471a8a3f6b47253e4796bc3559f6c7b389ce4b004d70ab0c04c933454`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d42470aa4461eb263340b714cf91223e64989da0efd82729652db07eec42cc`  
		Last Modified: Fri, 25 Oct 2024 02:49:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:78e4ea723042b217fb38f38c02ed1c4383b09141d7f0a2696ee5b72187989bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61c1b78d61c0e364b21a45b2caaf961a9f800a8657f779ca621199534929719`

```dockerfile
```

-	Layers:
	-	`sha256:8ded441250b18ed96be4decb09068cbebb97cc0c5b5a78a72c2398c31f6e2b31`  
		Last Modified: Fri, 25 Oct 2024 02:49:31 GMT  
		Size: 2.1 MB (2147807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f242ffe1dc15e1632f169cb0fdb9c52eff4f1cfa160aa2efe395c83193b8ea`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 30.9 KB (30949 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:b4735380fef3b40db741edcda06590075faaf8ce6788f71900223d5ee9681954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72716362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9f0e692053a7b858d9e4e322e492896e71d19567dc746f0c59e0ff768d0c67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ef8ad75958cd7eb0e453d0f85e72134ef3976f8351b5742370df35bc60ed42`  
		Last Modified: Sat, 07 Sep 2024 02:23:50 GMT  
		Size: 3.3 MB (3333388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f80c1299f6c626e7df88761199f03734cced725870be7a04dd95bf11e80104`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb3615e2ca5466e128fbfbd9bfcaa4cc0a7c5935f1d980f13d765c6bfde9144`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b324dba8535eea2357b994da9864afef849388a4c8e80235090810383253f31`  
		Last Modified: Fri, 25 Oct 2024 02:19:36 GMT  
		Size: 12.5 MB (12504686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e479347c3f32eee03df523edd0f1a869f7a7636702922f9d5db1ac9024ea211`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6b8889455c447cc20eb2d9881a51c22cdac63cc440a2e647d8e5c2c7f13cfc`  
		Last Modified: Fri, 25 Oct 2024 02:19:37 GMT  
		Size: 20.9 MB (20940181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eeecc80b8f4736452eb3054bbf21ee480f6a4eb724b114b31cb94ab034f53c`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93069ffa1c1f8ac20ef6e8c62fa71d5ba3e5ae3f4ce6b97965ae1a5a0f2562bb`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98eea5daa433de13908b8daf3e98a58f41b648a198629693556299898d3050f`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 30.9 MB (30879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24933c1ee11a72c73a8c1d127f5254b2e1a343115700bfd5d40922a70347acac`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557a745b32b20029beab65e3acdc0450cd4f061eb272e090e823072c4b8b8277`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 946.4 KB (946416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fbb3c72980ba7988a2db7b9613cdb24de6cd53d9f1c55a9bf587fa83e91bbf`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763a639df17e35391453ee7f589bafca0c377a16c7d0732f158ee93511e5f769`  
		Last Modified: Fri, 25 Oct 2024 04:22:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:caf94f6b789abd452f00a7c66c15651306dd21f55bbfbf41e9de10d2b6a43b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771e5d72f8d7aa1932d6904471851b84f38a74209160af344871cbe9a301a80d`

```dockerfile
```

-	Layers:
	-	`sha256:cd6c902d764be73511e42400a26661ea999092ccabef1d81e121b13769456d85`  
		Last Modified: Fri, 25 Oct 2024 04:22:33 GMT  
		Size: 2.1 MB (2147633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1effed70f7bcdf54c50bdaa8c95188f65bdc7c9791e0022cf05680e79ce5e10e`  
		Last Modified: Fri, 25 Oct 2024 04:22:33 GMT  
		Size: 31.0 KB (30977 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:e33d8a8adc22b99db3cbddf647ea3ba3832f8c5d1d58bb90e42596ef8c94ad74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52353571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f2a1e5ee2c294d7c24728d23e74e9df91cf6999fa2a05097d4595fc8a11b68`
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:9eaf7c1d9791c6b12392f1f767948304f2c2e69cb0878ecec4d5df2be5af4dca`  
		Last Modified: Fri, 25 Oct 2024 04:22:20 GMT  
		Size: 12.5 MB (12504687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0bab9c844ca004a8fd6a7ea2a92c041012b047b66151b6d55f81e1e29009e`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609f4e456e59a3c94a5761b23648a66de98737427aa781c0b05b3296eacbef62`  
		Last Modified: Fri, 25 Oct 2024 04:22:23 GMT  
		Size: 20.8 MB (20818182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4455a0ae1ac0aca52a62943181a6673cf4e49459913cfea722ceb78acf98f28`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f23e94c0f2162ee0e26724220289d3609acb53f3117201cba2c8e6e5021efa`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 19.7 KB (19716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0d35444bc5e8c85dfb6fca26a91f8f71cbdaf010077d220932f53bc33453a`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 11.3 MB (11281319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbd8ee9662704273444a11a2628a08c55058235539da3ea7e96f3be43027311`  
		Last Modified: Fri, 25 Oct 2024 04:49:54 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd495a69bd985f7c58cbdc3bfb7fb84be69f050722b1426bfc91550c4ed7b967`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 923.7 KB (923654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffd79d5011bba75faf5b0334876e22a52625a56727cc43ceed2de7674d04399`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba53d57ff746cd2ddd87d6ced854a49c95ff92a78a41be2558d7a03fc458d45`  
		Last Modified: Fri, 25 Oct 2024 04:49:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:d503fa86a799da1a63e5ae8d28399ca6a0ff53d7c048f122664c7a3034c23420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.0 KB (452000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498f99d0fa1404bc185ba6674ca97861f0b724fe4a9d7f7f6f1ee3f18f329288`

```dockerfile
```

-	Layers:
	-	`sha256:05d26777b19bcefc825c58a638d76199a5f0c83020a0ecfcaa3e6bfb0dfb20f2`  
		Last Modified: Fri, 25 Oct 2024 04:49:52 GMT  
		Size: 421.2 KB (421168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6637a35e080632eed43344b1ae9739a1bfa92b13c73c5c1de56f4a96bb8d3dc4`  
		Last Modified: Fri, 25 Oct 2024 04:49:52 GMT  
		Size: 30.8 KB (30832 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:bb8414850435f77da1b614134245f5011e7056e4701a30ad8eadc93c5746ea88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73154547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e6e2487a5d491f3ab1e6ae7f9df85aab9b33def2334634655955afa8bd2544`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac727a268c34206d27f9588c3acfc276afdaf0623dfdc19b7d210a7a881ee4`  
		Last Modified: Sat, 07 Sep 2024 01:44:58 GMT  
		Size: 3.4 MB (3408322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564dcd8f1c226aa29a92bf07685b2a44ccb8ac47267a590bc34a56d25bbbcc4`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3867a87b0703f924c2a7915ce891a49d11c61af6d01613564e485431a9f78`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8622608d41f825e14aa5bd26799c3251549bceef128cf2eae2f52f1ab78913e`  
		Last Modified: Fri, 25 Oct 2024 00:57:34 GMT  
		Size: 12.5 MB (12504690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b9b2cc7fa22223c46604afd8fd56f225e535ca1e7d006d545233f411a4a3c0`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9400d92782aead1169d2e61549cc961ef18b1a2f1468fe9a486ae165d901cf6b`  
		Last Modified: Fri, 25 Oct 2024 00:57:37 GMT  
		Size: 21.3 MB (21285751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ccc474f40266b6e9c07bd2bd8edf9b2feccdf7986579f0a7bfa017cb90929`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd3a52d6da309a1907e5c8310c6411753ee8823a82029f55b265da24bb7566d`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b86ce86d7510dbd92b9dd787d737ff21b3ba726f05cb8546ccc581875d372d`  
		Last Modified: Fri, 25 Oct 2024 03:09:39 GMT  
		Size: 31.4 MB (31402604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74408fea44fbe8cb944832b386c9752e053e23539d049cfad4f03cac46f658f4`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd275ee85ecbdd427da2151dde955458d6d1a75fde608151c2b458a299b5391`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 956.4 KB (956388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bcb717846c44afd18a6d65ecdb638100cda39ee224ab008e8ded724a526776`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7923799a776ec1502c18e4dd0b30afce84fb4ee98781a0ae21133ff02f527fea`  
		Last Modified: Fri, 25 Oct 2024 03:09:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:6c2cfe0bf3738dc08b980f54b00584a8aa061bd4b0c109dd7251fb983b0bb7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badc90556f39fbf10a2dc27c3b81c4f9243f8d46c8acc221ee4c6065b29a8020`

```dockerfile
```

-	Layers:
	-	`sha256:1e9a706865fea7597dadf4e06cddf10f4b67c21ee03790d8fe9f2e67ad69caee`  
		Last Modified: Fri, 25 Oct 2024 03:09:37 GMT  
		Size: 2.1 MB (2146043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbdd29b7434ab64926ee6535422d4b73de69aa7d5e5a2965da2d7037207cf3c4`  
		Last Modified: Fri, 25 Oct 2024 03:09:36 GMT  
		Size: 30.9 KB (30895 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:1483db658441f9702ced09239b2970ade1f86231ff6df798df9986c760d535a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70847593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20f8993a43ef737a0eacb62c27cc4583c5be4796f1ea8178efc3044f496123d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160a71fe2c21fa0be03f4ecb3856d46307a8cab34f0749e89c452111c128a28e`  
		Last Modified: Sat, 07 Sep 2024 09:00:45 GMT  
		Size: 3.4 MB (3405216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99de0cdf41fffa764363801fb8a9efbd008b3689317846613f74f55be82ad4ec`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4878284381f1e57d12b980a3d3f2476a10fab26827866948f61cc0a2214a8`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d60d72a55a97ca66240c87e7bc1886bc5aa87d97579097a6d9bab88a75ae1d`  
		Last Modified: Fri, 25 Oct 2024 06:19:30 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55404ef143ec5be664bfb8b7d19253fad3452d91340eac96ad5cb7f88c34e9e`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f1fc6d05b292475d5cdd272dff683e4226cec9930f2394a99a2af5ad9a19c`  
		Last Modified: Fri, 25 Oct 2024 06:19:45 GMT  
		Size: 19.8 MB (19785919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f47a3a529d11fa207f1e96b631df8f8334701948d58152ac5419e07ef6f0b09`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5729eb71e7d125b843a7ed55653966533b980fcc3e19e4ee54ce1e25042a67`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d654c394fa744c0d5afc76db22431671980aa34529d74f487cfbb8e0857966`  
		Last Modified: Fri, 25 Oct 2024 09:50:35 GMT  
		Size: 30.8 MB (30811074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a58738e9c21fa9035cc24b974c8d99fbd269320abe6e366312beca87fb36e14`  
		Last Modified: Fri, 25 Oct 2024 09:50:31 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8406617ce7b268f103442ebf9014ebb6d00d67423a00e8d4cc0fe8a3c2083043`  
		Last Modified: Fri, 25 Oct 2024 09:50:32 GMT  
		Size: 944.8 KB (944841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c543e1043c470ffc9bca0c243d676542df337e9a6e996c135ad2f78f672a4f0`  
		Last Modified: Fri, 25 Oct 2024 09:50:32 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7958c4da0e040043bad20bd8b15e89de25894621fb219fe83ac2fbf159452a5`  
		Last Modified: Fri, 25 Oct 2024 09:50:11 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:cfac385a69656c4bc61b504be55a26c78db57b8a604070bdfdc12dbbb3216fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76326f6043366dcee1d6cc4fb363dd045fd8c7b58baac7f73c132391c8b9ed46`

```dockerfile
```

-	Layers:
	-	`sha256:4857c7dcee21584b869465928007f9d02e7c629a554194f63fb75289d564a923`  
		Last Modified: Fri, 25 Oct 2024 09:50:29 GMT  
		Size: 2.1 MB (2145659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c6439a91f43d65978003cc2cd63ebe853980f94c8ba18b14b132d7692d373de`  
		Last Modified: Fri, 25 Oct 2024 09:50:29 GMT  
		Size: 30.9 KB (30897 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:ac8d71b74fc72077507d30cc50805203012d3d431189328ab346bec2a2c69362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72180557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38237ef2ad42e4abd9fec2cef110dda5ba4d73331f1b4ffe5989ec1a91627f09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9208ede8519d248128a660ad6cbef1b3a33b141374be176c946b5b17b2968ab4`  
		Last Modified: Sat, 07 Sep 2024 00:42:38 GMT  
		Size: 3.5 MB (3473993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabbdadb2babb53e22b8c60bffa37b66bacdd1495093eec38748ca15dabc8287`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2431f4d7c348124f66281fa6433fdcded6e6a093aedb9cdd6fa9c7d87a1407`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8632e206b7bc36b0bfe226c5ec5e94154bc411b3677a2903f0f33e8b4d06d3`  
		Last Modified: Fri, 25 Oct 2024 02:46:23 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950b6d1374ddd91229978b32c87237f1a304df6908d46a3e6c6617379120ecb`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fac98b72a50f285d80ad08584ff62de41c8b0ea0276e5187d77f6dddb0430e4`  
		Last Modified: Fri, 25 Oct 2024 02:46:25 GMT  
		Size: 20.4 MB (20422987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17a61d0d2aae412d208b48c74e3754c9fc7b3f3d0644186eb5a952c01d1d01a`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c55de606062f9878f968213cb2af563401f158dbc5f7b5612b565d5f23a8d8`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a65e35183739b8872e800265ad579948004dd6060f487f2295911c401548795`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 31.3 MB (31338414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c5278f124e717ca16fc2677a7e92e4331ffd330679687f8429c052a4980ca6`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbe0019b55069a840ff7d33ab47aa1388698ccd7de55346481fc06538f96bab`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 954.5 KB (954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942823da0620c6a8685cd25196843521489eac657adec4d60aadc71e5877dff`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe38bd91f2e8ddf38dbbc935628e7eca7377274d3b0e557d7c2bae841103d3e3`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:4a9995428838589af3cc454155789495893d62697a3752bd1afcf4d372428992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7b257062667dfefc37406d94da1c369836eff05846dc1bda28c0090bf6aac4`

```dockerfile
```

-	Layers:
	-	`sha256:b1c9fb6718635125713745a5dcd123fe5ab6937f08ab19273a2f2e76b28f1039`  
		Last Modified: Fri, 25 Oct 2024 06:34:15 GMT  
		Size: 2.1 MB (2145445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b72977063c3707f9c3b52de3dcb56482332296630c5a3b914ba5d277f3074027`  
		Last Modified: Fri, 25 Oct 2024 06:34:15 GMT  
		Size: 30.9 KB (30861 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.24`

```console
$ docker pull composer@sha256:46531d95ae84b4d0f44b109d365db86fca10d96d1cfb68999d9541426d89a43e
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
$ docker pull composer@sha256:1b8c7b7803441706a9e04bcb7c23d6c7d5935a6d27d7ab797183700fc4d3cda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71258353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d94b12f6cbd009a3fc780b7b1aa509b42f3a678572dc657b92d63c98ca8db49`
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:41457434eddc5cb99259de159d6a2dad43029452b1ab35975a3209703b9897f4`  
		Last Modified: Fri, 25 Oct 2024 02:16:38 GMT  
		Size: 12.5 MB (12504689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328056f851cc57837c30c7c30c8c1fba0e538db1bdb0f520508b064b7771388b`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66dabf5a41275ff903a5f9ccc8ba9ba981ff4f80da78ac30a649f683542b98c`  
		Last Modified: Fri, 25 Oct 2024 02:16:40 GMT  
		Size: 20.5 MB (20518417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab768f68c87e7a556fcaf812a92acd5c8bf122cc606c956394a6ec4bc208f0f1`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b263e76cc797a1f79fdee350bf8047c4fae8cea974168046c693eec0894545`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8e721d4ec60c167e217985a6634def0773d7c209c854c6cff384ae95d609e0`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 30.4 MB (30368247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482b3b3d18b4f075b12c4319e5dc322215e9ac691e238f09bbf7858afdc525cd`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9323b09d4891470d8d5dbad780102f127ee113898ab714b3cea5a8e051ef7ab5`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 935.9 KB (935910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ede80ac42873d95db4f1e1dc746ab53be2071011ecc8e0df9a2a05d6ff83f0`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9ebd623a6cd55899fbfa1cdbd8ed0b505385fc70414307c27b06e6306c2a50`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:85d2f659fdf26193b06cb76d853c0d73e75ba826c2b5b3d9e44f53aa15da98b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb3aef60fab8f0110068b8032e3b12e726d2978eb062c434b806dcbd8e0fb84`

```dockerfile
```

-	Layers:
	-	`sha256:b704440e485eec60929d9914b7388f77adb483eebc2626931665c90c8ea22b89`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 2.1 MB (2147494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f51685b55e387f4a3da1dc24d977b000fb70421efa45bf9f76f43d84f9c86bb`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 30.9 KB (30861 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; arm variant v6

```console
$ docker pull composer@sha256:30730658678c13b3fa13492b42fff3265b536c0a21aaa129acc0865633af891b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67981937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa096441dfd2778abfc7be3ff0a8e578eed66f710e8b6b8c94e3812a9c7c87b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78c7a9de9941e89cd785fc3ad14f52410d858d2259f5c9b2a852fd144612520`  
		Last Modified: Sat, 07 Sep 2024 00:48:55 GMT  
		Size: 3.3 MB (3269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbf8fddbe2a872480c609959838de42e95d1f5d5d3d8daadf7a1e44e5c381a2`  
		Last Modified: Sat, 07 Sep 2024 00:48:54 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d88511b2a3086248129999917d9f1e5928426fda8f08edf40ab5bafa37a9`  
		Last Modified: Sat, 07 Sep 2024 00:48:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2913caf4eeb0b47e0a269d5500be80ad644b55b830987923b9b25d7c47b779b6`  
		Last Modified: Fri, 25 Oct 2024 01:12:37 GMT  
		Size: 12.5 MB (12504684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd40e2319cfc199b8ddae2c1022299e653810d5c8fcff021ecf9e71bc732119`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8662dfadda858bf306da862403b12c0ebf0c2c06e8cc29019a10cec84a7ec93`  
		Last Modified: Fri, 25 Oct 2024 01:12:41 GMT  
		Size: 18.7 MB (18711875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0edc47bdf53f26bf4da16fdc4eec8b087534150b52237c0f603b8e571890a9`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43053646b918ed9c5822c17ca4869f057851bb96fcaabed794a5a7ec36dba34`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92515b32642bf33db09f5042274a35b3bf9dfd52f33a78bed3ddb0efab90867`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 29.2 MB (29169219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cececc96a315d5d1a226bb3d06189757c3df3f0bf808c3089f6a8c1ee57b169`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c2e6b61270c266b53490ff499b93ef054fbec927512a281cc7a6b24701805`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 935.5 KB (935497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff00edb04cb0f9ff5be423ef9e64b2cc05ec099877d249544ab29d1038f5de3d`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c6ab539bccdbdb0fcf7fafd68ce2bd97284eab5f8d8abf785cabec35588b7b`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:e4a9826fe50da350c6777297621c260458faba92b526041a376ce79aab8b81b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57b36f19d8ad3b6a6132c9b81dbfc98306a2cd534a3294c6f488017985d24eb`

```dockerfile
```

-	Layers:
	-	`sha256:37078fd6622f6a210d26c2f3f60d602e03823611193b605e55caca850fea26d2`  
		Last Modified: Fri, 25 Oct 2024 02:09:51 GMT  
		Size: 30.7 KB (30734 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; arm variant v7

```console
$ docker pull composer@sha256:c91cd5ffa3dbabd16ca1a5236effe469f34a169c118f5e08a70364c4028ba35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65895087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5708873007b11d781ab952dd94413afc61e3fb305d253bd5f588a1aa1c3b233`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12c01d5f758f7fce28807153dec7a85ae2e307cf0d73f644d575cd875cb994a`  
		Last Modified: Fri, 06 Sep 2024 23:45:25 GMT  
		Size: 3.1 MB (3079568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c3e48f803b4ca0c1ec0b16f85f80f0a17b054845918112eb73b80eb9bd7297`  
		Last Modified: Fri, 06 Sep 2024 23:45:23 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7c21bdd57d9b7548f08c79a56f0a75d4e14a705967ae55d0450a10f0c6c43e`  
		Last Modified: Fri, 06 Sep 2024 23:45:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efe62db4f1f9f85f795e6cc1e7f8d835b0a8657d2a60143ba15d82d5863841`  
		Last Modified: Fri, 25 Oct 2024 02:37:26 GMT  
		Size: 12.5 MB (12504680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204359c9c9eb5cb76578981a5c068e3fac227ce0e7df1a86096569dc1230c85`  
		Last Modified: Fri, 25 Oct 2024 02:37:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2762620a9d567bff0020a3cda73a630f1a993bda6921efbd9554d75c9fd3377f`  
		Last Modified: Fri, 25 Oct 2024 02:37:28 GMT  
		Size: 17.5 MB (17478737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5a9688a15e4908bcd1ed18d76acd39f8678dd66decafbae483b2c884bf1c02`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66727798fd727eda6cfc82ff904b3773b442a67ae9e11967aac36d92e2e9be32`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ef898d316952fe64642bc94179ed2cc82e7c9404af0c91e8d0f5152097b5e8`  
		Last Modified: Fri, 25 Oct 2024 02:49:33 GMT  
		Size: 28.8 MB (28797969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48238d159943a0389cdf60849c19e218b8aeae434d69dfb9050fc0c71115bf9a`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac4b3d7e0e3d6c59f9af60415c3648615e5a2c56d6abd230155f2bb2576aee4`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 914.2 KB (914234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2f49471a8a3f6b47253e4796bc3559f6c7b389ce4b004d70ab0c04c933454`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d42470aa4461eb263340b714cf91223e64989da0efd82729652db07eec42cc`  
		Last Modified: Fri, 25 Oct 2024 02:49:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:78e4ea723042b217fb38f38c02ed1c4383b09141d7f0a2696ee5b72187989bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61c1b78d61c0e364b21a45b2caaf961a9f800a8657f779ca621199534929719`

```dockerfile
```

-	Layers:
	-	`sha256:8ded441250b18ed96be4decb09068cbebb97cc0c5b5a78a72c2398c31f6e2b31`  
		Last Modified: Fri, 25 Oct 2024 02:49:31 GMT  
		Size: 2.1 MB (2147807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f242ffe1dc15e1632f169cb0fdb9c52eff4f1cfa160aa2efe395c83193b8ea`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 30.9 KB (30949 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:b4735380fef3b40db741edcda06590075faaf8ce6788f71900223d5ee9681954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72716362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9f0e692053a7b858d9e4e322e492896e71d19567dc746f0c59e0ff768d0c67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ef8ad75958cd7eb0e453d0f85e72134ef3976f8351b5742370df35bc60ed42`  
		Last Modified: Sat, 07 Sep 2024 02:23:50 GMT  
		Size: 3.3 MB (3333388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f80c1299f6c626e7df88761199f03734cced725870be7a04dd95bf11e80104`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb3615e2ca5466e128fbfbd9bfcaa4cc0a7c5935f1d980f13d765c6bfde9144`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b324dba8535eea2357b994da9864afef849388a4c8e80235090810383253f31`  
		Last Modified: Fri, 25 Oct 2024 02:19:36 GMT  
		Size: 12.5 MB (12504686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e479347c3f32eee03df523edd0f1a869f7a7636702922f9d5db1ac9024ea211`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6b8889455c447cc20eb2d9881a51c22cdac63cc440a2e647d8e5c2c7f13cfc`  
		Last Modified: Fri, 25 Oct 2024 02:19:37 GMT  
		Size: 20.9 MB (20940181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eeecc80b8f4736452eb3054bbf21ee480f6a4eb724b114b31cb94ab034f53c`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93069ffa1c1f8ac20ef6e8c62fa71d5ba3e5ae3f4ce6b97965ae1a5a0f2562bb`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98eea5daa433de13908b8daf3e98a58f41b648a198629693556299898d3050f`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 30.9 MB (30879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24933c1ee11a72c73a8c1d127f5254b2e1a343115700bfd5d40922a70347acac`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557a745b32b20029beab65e3acdc0450cd4f061eb272e090e823072c4b8b8277`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 946.4 KB (946416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fbb3c72980ba7988a2db7b9613cdb24de6cd53d9f1c55a9bf587fa83e91bbf`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763a639df17e35391453ee7f589bafca0c377a16c7d0732f158ee93511e5f769`  
		Last Modified: Fri, 25 Oct 2024 04:22:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:caf94f6b789abd452f00a7c66c15651306dd21f55bbfbf41e9de10d2b6a43b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771e5d72f8d7aa1932d6904471851b84f38a74209160af344871cbe9a301a80d`

```dockerfile
```

-	Layers:
	-	`sha256:cd6c902d764be73511e42400a26661ea999092ccabef1d81e121b13769456d85`  
		Last Modified: Fri, 25 Oct 2024 04:22:33 GMT  
		Size: 2.1 MB (2147633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1effed70f7bcdf54c50bdaa8c95188f65bdc7c9791e0022cf05680e79ce5e10e`  
		Last Modified: Fri, 25 Oct 2024 04:22:33 GMT  
		Size: 31.0 KB (30977 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; 386

```console
$ docker pull composer@sha256:e33d8a8adc22b99db3cbddf647ea3ba3832f8c5d1d58bb90e42596ef8c94ad74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52353571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f2a1e5ee2c294d7c24728d23e74e9df91cf6999fa2a05097d4595fc8a11b68`
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:9eaf7c1d9791c6b12392f1f767948304f2c2e69cb0878ecec4d5df2be5af4dca`  
		Last Modified: Fri, 25 Oct 2024 04:22:20 GMT  
		Size: 12.5 MB (12504687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0bab9c844ca004a8fd6a7ea2a92c041012b047b66151b6d55f81e1e29009e`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609f4e456e59a3c94a5761b23648a66de98737427aa781c0b05b3296eacbef62`  
		Last Modified: Fri, 25 Oct 2024 04:22:23 GMT  
		Size: 20.8 MB (20818182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4455a0ae1ac0aca52a62943181a6673cf4e49459913cfea722ceb78acf98f28`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f23e94c0f2162ee0e26724220289d3609acb53f3117201cba2c8e6e5021efa`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 19.7 KB (19716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0d35444bc5e8c85dfb6fca26a91f8f71cbdaf010077d220932f53bc33453a`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 11.3 MB (11281319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbd8ee9662704273444a11a2628a08c55058235539da3ea7e96f3be43027311`  
		Last Modified: Fri, 25 Oct 2024 04:49:54 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd495a69bd985f7c58cbdc3bfb7fb84be69f050722b1426bfc91550c4ed7b967`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 923.7 KB (923654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffd79d5011bba75faf5b0334876e22a52625a56727cc43ceed2de7674d04399`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba53d57ff746cd2ddd87d6ced854a49c95ff92a78a41be2558d7a03fc458d45`  
		Last Modified: Fri, 25 Oct 2024 04:49:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:d503fa86a799da1a63e5ae8d28399ca6a0ff53d7c048f122664c7a3034c23420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.0 KB (452000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498f99d0fa1404bc185ba6674ca97861f0b724fe4a9d7f7f6f1ee3f18f329288`

```dockerfile
```

-	Layers:
	-	`sha256:05d26777b19bcefc825c58a638d76199a5f0c83020a0ecfcaa3e6bfb0dfb20f2`  
		Last Modified: Fri, 25 Oct 2024 04:49:52 GMT  
		Size: 421.2 KB (421168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6637a35e080632eed43344b1ae9739a1bfa92b13c73c5c1de56f4a96bb8d3dc4`  
		Last Modified: Fri, 25 Oct 2024 04:49:52 GMT  
		Size: 30.8 KB (30832 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; ppc64le

```console
$ docker pull composer@sha256:bb8414850435f77da1b614134245f5011e7056e4701a30ad8eadc93c5746ea88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73154547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e6e2487a5d491f3ab1e6ae7f9df85aab9b33def2334634655955afa8bd2544`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac727a268c34206d27f9588c3acfc276afdaf0623dfdc19b7d210a7a881ee4`  
		Last Modified: Sat, 07 Sep 2024 01:44:58 GMT  
		Size: 3.4 MB (3408322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564dcd8f1c226aa29a92bf07685b2a44ccb8ac47267a590bc34a56d25bbbcc4`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3867a87b0703f924c2a7915ce891a49d11c61af6d01613564e485431a9f78`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8622608d41f825e14aa5bd26799c3251549bceef128cf2eae2f52f1ab78913e`  
		Last Modified: Fri, 25 Oct 2024 00:57:34 GMT  
		Size: 12.5 MB (12504690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b9b2cc7fa22223c46604afd8fd56f225e535ca1e7d006d545233f411a4a3c0`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9400d92782aead1169d2e61549cc961ef18b1a2f1468fe9a486ae165d901cf6b`  
		Last Modified: Fri, 25 Oct 2024 00:57:37 GMT  
		Size: 21.3 MB (21285751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ccc474f40266b6e9c07bd2bd8edf9b2feccdf7986579f0a7bfa017cb90929`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd3a52d6da309a1907e5c8310c6411753ee8823a82029f55b265da24bb7566d`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b86ce86d7510dbd92b9dd787d737ff21b3ba726f05cb8546ccc581875d372d`  
		Last Modified: Fri, 25 Oct 2024 03:09:39 GMT  
		Size: 31.4 MB (31402604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74408fea44fbe8cb944832b386c9752e053e23539d049cfad4f03cac46f658f4`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd275ee85ecbdd427da2151dde955458d6d1a75fde608151c2b458a299b5391`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 956.4 KB (956388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bcb717846c44afd18a6d65ecdb638100cda39ee224ab008e8ded724a526776`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7923799a776ec1502c18e4dd0b30afce84fb4ee98781a0ae21133ff02f527fea`  
		Last Modified: Fri, 25 Oct 2024 03:09:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:6c2cfe0bf3738dc08b980f54b00584a8aa061bd4b0c109dd7251fb983b0bb7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badc90556f39fbf10a2dc27c3b81c4f9243f8d46c8acc221ee4c6065b29a8020`

```dockerfile
```

-	Layers:
	-	`sha256:1e9a706865fea7597dadf4e06cddf10f4b67c21ee03790d8fe9f2e67ad69caee`  
		Last Modified: Fri, 25 Oct 2024 03:09:37 GMT  
		Size: 2.1 MB (2146043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbdd29b7434ab64926ee6535422d4b73de69aa7d5e5a2965da2d7037207cf3c4`  
		Last Modified: Fri, 25 Oct 2024 03:09:36 GMT  
		Size: 30.9 KB (30895 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; riscv64

```console
$ docker pull composer@sha256:1483db658441f9702ced09239b2970ade1f86231ff6df798df9986c760d535a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70847593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20f8993a43ef737a0eacb62c27cc4583c5be4796f1ea8178efc3044f496123d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160a71fe2c21fa0be03f4ecb3856d46307a8cab34f0749e89c452111c128a28e`  
		Last Modified: Sat, 07 Sep 2024 09:00:45 GMT  
		Size: 3.4 MB (3405216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99de0cdf41fffa764363801fb8a9efbd008b3689317846613f74f55be82ad4ec`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4878284381f1e57d12b980a3d3f2476a10fab26827866948f61cc0a2214a8`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d60d72a55a97ca66240c87e7bc1886bc5aa87d97579097a6d9bab88a75ae1d`  
		Last Modified: Fri, 25 Oct 2024 06:19:30 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55404ef143ec5be664bfb8b7d19253fad3452d91340eac96ad5cb7f88c34e9e`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f1fc6d05b292475d5cdd272dff683e4226cec9930f2394a99a2af5ad9a19c`  
		Last Modified: Fri, 25 Oct 2024 06:19:45 GMT  
		Size: 19.8 MB (19785919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f47a3a529d11fa207f1e96b631df8f8334701948d58152ac5419e07ef6f0b09`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5729eb71e7d125b843a7ed55653966533b980fcc3e19e4ee54ce1e25042a67`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d654c394fa744c0d5afc76db22431671980aa34529d74f487cfbb8e0857966`  
		Last Modified: Fri, 25 Oct 2024 09:50:35 GMT  
		Size: 30.8 MB (30811074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a58738e9c21fa9035cc24b974c8d99fbd269320abe6e366312beca87fb36e14`  
		Last Modified: Fri, 25 Oct 2024 09:50:31 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8406617ce7b268f103442ebf9014ebb6d00d67423a00e8d4cc0fe8a3c2083043`  
		Last Modified: Fri, 25 Oct 2024 09:50:32 GMT  
		Size: 944.8 KB (944841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c543e1043c470ffc9bca0c243d676542df337e9a6e996c135ad2f78f672a4f0`  
		Last Modified: Fri, 25 Oct 2024 09:50:32 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7958c4da0e040043bad20bd8b15e89de25894621fb219fe83ac2fbf159452a5`  
		Last Modified: Fri, 25 Oct 2024 09:50:11 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:cfac385a69656c4bc61b504be55a26c78db57b8a604070bdfdc12dbbb3216fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76326f6043366dcee1d6cc4fb363dd045fd8c7b58baac7f73c132391c8b9ed46`

```dockerfile
```

-	Layers:
	-	`sha256:4857c7dcee21584b869465928007f9d02e7c629a554194f63fb75289d564a923`  
		Last Modified: Fri, 25 Oct 2024 09:50:29 GMT  
		Size: 2.1 MB (2145659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c6439a91f43d65978003cc2cd63ebe853980f94c8ba18b14b132d7692d373de`  
		Last Modified: Fri, 25 Oct 2024 09:50:29 GMT  
		Size: 30.9 KB (30897 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.24` - linux; s390x

```console
$ docker pull composer@sha256:ac8d71b74fc72077507d30cc50805203012d3d431189328ab346bec2a2c69362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72180557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38237ef2ad42e4abd9fec2cef110dda5ba4d73331f1b4ffe5989ec1a91627f09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9208ede8519d248128a660ad6cbef1b3a33b141374be176c946b5b17b2968ab4`  
		Last Modified: Sat, 07 Sep 2024 00:42:38 GMT  
		Size: 3.5 MB (3473993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabbdadb2babb53e22b8c60bffa37b66bacdd1495093eec38748ca15dabc8287`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2431f4d7c348124f66281fa6433fdcded6e6a093aedb9cdd6fa9c7d87a1407`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8632e206b7bc36b0bfe226c5ec5e94154bc411b3677a2903f0f33e8b4d06d3`  
		Last Modified: Fri, 25 Oct 2024 02:46:23 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950b6d1374ddd91229978b32c87237f1a304df6908d46a3e6c6617379120ecb`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fac98b72a50f285d80ad08584ff62de41c8b0ea0276e5187d77f6dddb0430e4`  
		Last Modified: Fri, 25 Oct 2024 02:46:25 GMT  
		Size: 20.4 MB (20422987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17a61d0d2aae412d208b48c74e3754c9fc7b3f3d0644186eb5a952c01d1d01a`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c55de606062f9878f968213cb2af563401f158dbc5f7b5612b565d5f23a8d8`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a65e35183739b8872e800265ad579948004dd6060f487f2295911c401548795`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 31.3 MB (31338414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c5278f124e717ca16fc2677a7e92e4331ffd330679687f8429c052a4980ca6`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbe0019b55069a840ff7d33ab47aa1388698ccd7de55346481fc06538f96bab`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 954.5 KB (954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942823da0620c6a8685cd25196843521489eac657adec4d60aadc71e5877dff`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe38bd91f2e8ddf38dbbc935628e7eca7377274d3b0e557d7c2bae841103d3e3`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.24` - unknown; unknown

```console
$ docker pull composer@sha256:4a9995428838589af3cc454155789495893d62697a3752bd1afcf4d372428992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7b257062667dfefc37406d94da1c369836eff05846dc1bda28c0090bf6aac4`

```dockerfile
```

-	Layers:
	-	`sha256:b1c9fb6718635125713745a5dcd123fe5ab6937f08ab19273a2f2e76b28f1039`  
		Last Modified: Fri, 25 Oct 2024 06:34:15 GMT  
		Size: 2.1 MB (2145445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b72977063c3707f9c3b52de3dcb56482332296630c5a3b914ba5d277f3074027`  
		Last Modified: Fri, 25 Oct 2024 06:34:15 GMT  
		Size: 30.9 KB (30861 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8`

```console
$ docker pull composer@sha256:0d9ed84312bc8f0094c372b5074ddf89abffddd6e8b91d46f9d39f98cbd512b4
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
$ docker pull composer@sha256:a92e127cbf279c3b76b3f7a20bc4185c20d8d9b2124ed9e14ce2864d5732541b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71404941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8beffceb940b8587644cf8b44117807db3310b81a15145274e979407fdf7789c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 00:32:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Sep 2024 00:32:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 07 Sep 2024 00:32:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 07 Sep 2024 00:32:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Sep 2024 00:32:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 00:58:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
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
	-	`sha256:41457434eddc5cb99259de159d6a2dad43029452b1ab35975a3209703b9897f4`  
		Last Modified: Fri, 25 Oct 2024 02:16:38 GMT  
		Size: 12.5 MB (12504689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328056f851cc57837c30c7c30c8c1fba0e538db1bdb0f520508b064b7771388b`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66dabf5a41275ff903a5f9ccc8ba9ba981ff4f80da78ac30a649f683542b98c`  
		Last Modified: Fri, 25 Oct 2024 02:16:40 GMT  
		Size: 20.5 MB (20518417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab768f68c87e7a556fcaf812a92acd5c8bf122cc606c956394a6ec4bc208f0f1`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b263e76cc797a1f79fdee350bf8047c4fae8cea974168046c693eec0894545`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8c6e46e9e203f16f774d50fa9cee35406c7828c4fb2f3fe24a868e8cdbe576`  
		Last Modified: Fri, 25 Oct 2024 02:49:45 GMT  
		Size: 30.4 MB (30368357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b27fd7d7d1f5948b1fbe2965594f3bcce94435155a4c35a60b2d608d5ea2fd`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e9f4aa8790c6e63ad881b3900ab9120ea46bad338a9f9dc641af2fb1545dc8`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 1.1 MB (1082386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0fd2babfe1056ad805d84256fb3ec3d62cbaa0be56261a2c2c79a55c100052`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844c7c8ba204421ae47d0e4129dad01122cef45bef67ab49236fe225f2414e48`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:07e9c44c65d288981528af88e5f1ea62f7a8c5f6c4b047fb70b5ced53a2e17d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea337cfabf9cc40ac248aa582e15c6274d46217f1dd85555f1e5d03dd0cf1a8c`

```dockerfile
```

-	Layers:
	-	`sha256:2c8925f43dd72726464493496debe8d9254a2f386420933c92b82b7e17328db8`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 2.1 MB (2147788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac23cb17204e28cf366d9ea488f6d59fad0bc9ebb7c72a01b9f405bcc7ad7f9`  
		Last Modified: Fri, 25 Oct 2024 02:49:43 GMT  
		Size: 31.2 KB (31168 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:0731814f66fc6c48bd0c0807e80c89dc2e55e00fbb2f0f313bb22c127f7dd22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68128183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a45cc575b5b053051af22c57e1635b28ace0c5da57cd7994fc69278fc802ca0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:30:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:30:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:30:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:30:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:30:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:51:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78c7a9de9941e89cd785fc3ad14f52410d858d2259f5c9b2a852fd144612520`  
		Last Modified: Sat, 07 Sep 2024 00:48:55 GMT  
		Size: 3.3 MB (3269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbf8fddbe2a872480c609959838de42e95d1f5d5d3d8daadf7a1e44e5c381a2`  
		Last Modified: Sat, 07 Sep 2024 00:48:54 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d88511b2a3086248129999917d9f1e5928426fda8f08edf40ab5bafa37a9`  
		Last Modified: Sat, 07 Sep 2024 00:48:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2913caf4eeb0b47e0a269d5500be80ad644b55b830987923b9b25d7c47b779b6`  
		Last Modified: Fri, 25 Oct 2024 01:12:37 GMT  
		Size: 12.5 MB (12504684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd40e2319cfc199b8ddae2c1022299e653810d5c8fcff021ecf9e71bc732119`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8662dfadda858bf306da862403b12c0ebf0c2c06e8cc29019a10cec84a7ec93`  
		Last Modified: Fri, 25 Oct 2024 01:12:41 GMT  
		Size: 18.7 MB (18711875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0edc47bdf53f26bf4da16fdc4eec8b087534150b52237c0f603b8e571890a9`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43053646b918ed9c5822c17ca4869f057851bb96fcaabed794a5a7ec36dba34`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92515b32642bf33db09f5042274a35b3bf9dfd52f33a78bed3ddb0efab90867`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 29.2 MB (29169219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cececc96a315d5d1a226bb3d06189757c3df3f0bf808c3089f6a8c1ee57b169`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84dd6a8db95fd1cfab72745b588a6020c64ae5fa5e8e7eaf34da667e8998ebca`  
		Last Modified: Fri, 25 Oct 2024 02:11:27 GMT  
		Size: 1.1 MB (1081742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc448f86c117926316d64dc1703afc82d359157f79799cf045e2b86d86c667f6`  
		Last Modified: Mon, 07 Oct 2024 19:58:17 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53acd091d4bf5494fdd8f48f0cbdf90b0375e550a50197d0537f794786e4f735`  
		Last Modified: Fri, 25 Oct 2024 02:11:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:c70376116be9359f8d20e30b55fa4d81f4c5be21b3c1a64c07bb4141515b2ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56b4a57a86ddb1abdf163141d4bd42e27c5f5a4625178f8ea5a460ebe63b6a7`

```dockerfile
```

-	Layers:
	-	`sha256:f8dc929d2da75915ab1de51553bc89259f0f9e61645d119453a123ede1024cbc`  
		Last Modified: Fri, 25 Oct 2024 02:11:26 GMT  
		Size: 31.0 KB (31049 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:ff5c72f99787e7cd316fcc4395d97f53f714b04e6a96670c7af40a72e6f4be4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66041602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9624095698de01d4e75e21a48773fbb0d30e5fdca551bad82d4a57860f49e51`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:29:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 22:29:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 22:29:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 22:29:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 22:29:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 22:29:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:29:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:29:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 22:47:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12c01d5f758f7fce28807153dec7a85ae2e307cf0d73f644d575cd875cb994a`  
		Last Modified: Fri, 06 Sep 2024 23:45:25 GMT  
		Size: 3.1 MB (3079568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c3e48f803b4ca0c1ec0b16f85f80f0a17b054845918112eb73b80eb9bd7297`  
		Last Modified: Fri, 06 Sep 2024 23:45:23 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7c21bdd57d9b7548f08c79a56f0a75d4e14a705967ae55d0450a10f0c6c43e`  
		Last Modified: Fri, 06 Sep 2024 23:45:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efe62db4f1f9f85f795e6cc1e7f8d835b0a8657d2a60143ba15d82d5863841`  
		Last Modified: Fri, 25 Oct 2024 02:37:26 GMT  
		Size: 12.5 MB (12504680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204359c9c9eb5cb76578981a5c068e3fac227ce0e7df1a86096569dc1230c85`  
		Last Modified: Fri, 25 Oct 2024 02:37:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2762620a9d567bff0020a3cda73a630f1a993bda6921efbd9554d75c9fd3377f`  
		Last Modified: Fri, 25 Oct 2024 02:37:28 GMT  
		Size: 17.5 MB (17478737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5a9688a15e4908bcd1ed18d76acd39f8678dd66decafbae483b2c884bf1c02`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66727798fd727eda6cfc82ff904b3773b442a67ae9e11967aac36d92e2e9be32`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ef898d316952fe64642bc94179ed2cc82e7c9404af0c91e8d0f5152097b5e8`  
		Last Modified: Fri, 25 Oct 2024 02:49:33 GMT  
		Size: 28.8 MB (28797969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48238d159943a0389cdf60849c19e218b8aeae434d69dfb9050fc0c71115bf9a`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b58a4408498db5e9ab01414bd6385d998cb8f21dabb6be95a750906ae5b1f3c`  
		Last Modified: Fri, 25 Oct 2024 02:51:11 GMT  
		Size: 1.1 MB (1060749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6503f2fca1c6898aa87f48db0cd634630c52a3268995b25f8caffb8bee8475a`  
		Last Modified: Fri, 25 Oct 2024 02:51:10 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fabf1a07b3bdac00b08274fdd1b79967aabe3c4f6526c99bd7c80255a9c5c07`  
		Last Modified: Fri, 25 Oct 2024 02:51:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:29a9862fa241870ee9e9744c1234cb68935ff206aa43236d0f21de7a297aa903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38703114d6a9c5f9de4eeae5759012126d06ad4b07f8ce0d8348157c7a9c8ff`

```dockerfile
```

-	Layers:
	-	`sha256:d1bb5967213b8eacf025fbae03caf581e6326e1e330d4c01ebb58cbb27eac34e`  
		Last Modified: Fri, 25 Oct 2024 02:51:10 GMT  
		Size: 2.1 MB (2148109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b80953e51404205596c003a9bf2f30426361239bd88f3d5879f028987ab723e`  
		Last Modified: Fri, 25 Oct 2024 02:51:10 GMT  
		Size: 31.3 KB (31264 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:4575910a0d4a9df7ffd9da094b4d4e73f4a2be32d36246e7329d623454ae6329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72860831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3c631a63beae9b8ee7bcc06a3f14113fb4fc0765bc591470a50ddcb080bde6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 00:43:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Sep 2024 00:43:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 07 Sep 2024 00:43:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 07 Sep 2024 00:43:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Sep 2024 00:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 01:04:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ef8ad75958cd7eb0e453d0f85e72134ef3976f8351b5742370df35bc60ed42`  
		Last Modified: Sat, 07 Sep 2024 02:23:50 GMT  
		Size: 3.3 MB (3333388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f80c1299f6c626e7df88761199f03734cced725870be7a04dd95bf11e80104`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb3615e2ca5466e128fbfbd9bfcaa4cc0a7c5935f1d980f13d765c6bfde9144`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b324dba8535eea2357b994da9864afef849388a4c8e80235090810383253f31`  
		Last Modified: Fri, 25 Oct 2024 02:19:36 GMT  
		Size: 12.5 MB (12504686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e479347c3f32eee03df523edd0f1a869f7a7636702922f9d5db1ac9024ea211`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6b8889455c447cc20eb2d9881a51c22cdac63cc440a2e647d8e5c2c7f13cfc`  
		Last Modified: Fri, 25 Oct 2024 02:19:37 GMT  
		Size: 20.9 MB (20940181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eeecc80b8f4736452eb3054bbf21ee480f6a4eb724b114b31cb94ab034f53c`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93069ffa1c1f8ac20ef6e8c62fa71d5ba3e5ae3f4ce6b97965ae1a5a0f2562bb`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98eea5daa433de13908b8daf3e98a58f41b648a198629693556299898d3050f`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 30.9 MB (30879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24933c1ee11a72c73a8c1d127f5254b2e1a343115700bfd5d40922a70347acac`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b210b09c1b5dce1b5094e57caea0452e5776bb3f43f7c8d5e388cb69ced01d44`  
		Last Modified: Fri, 25 Oct 2024 04:26:34 GMT  
		Size: 1.1 MB (1090886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b5d0e63e39d147a5ff8487e68431854584ec90cd07275ae0a841e77cd539f9`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec155f53f4ab45bdf10f33bb071a35ac7b7777b50897579201c20b6fc9223dec`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:f165a4ca8adb8f345a4fbbd2d0e6ce7423ff3cccbe80bc6b4f74cd433103cc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732da8b9d36aadf2652af89a530a393a085bba4c677c1b4310dd4bb506d19e83`

```dockerfile
```

-	Layers:
	-	`sha256:84135c99834ab363c853372259a9196b615745b6251e3f49a3b9ae0f2786b92a`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 2.1 MB (2147939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9042f9e0e6a93e08e64a8eb7f1f3caba691460c8068e0cafe27485b1de12b43`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 31.3 KB (31296 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; 386

```console
$ docker pull composer@sha256:62aac98b8ddd75628e726dfa617ad4cb8999c542b5694731ad2a759ce8db7f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52499599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3c0137caf6333752ae7e9a4c6dab56a54051e5561cd9e4eb1bf546ff340517`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:57:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 22:57:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 22:57:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 22:57:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 22:57:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 22:57:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:57:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:57:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:42:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
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
	-	`sha256:9eaf7c1d9791c6b12392f1f767948304f2c2e69cb0878ecec4d5df2be5af4dca`  
		Last Modified: Fri, 25 Oct 2024 04:22:20 GMT  
		Size: 12.5 MB (12504687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0bab9c844ca004a8fd6a7ea2a92c041012b047b66151b6d55f81e1e29009e`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609f4e456e59a3c94a5761b23648a66de98737427aa781c0b05b3296eacbef62`  
		Last Modified: Fri, 25 Oct 2024 04:22:23 GMT  
		Size: 20.8 MB (20818182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4455a0ae1ac0aca52a62943181a6673cf4e49459913cfea722ceb78acf98f28`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f23e94c0f2162ee0e26724220289d3609acb53f3117201cba2c8e6e5021efa`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 19.7 KB (19716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119b4f99527dc6b667937203167ecff4617fc1078093fefa09df11b56496bf86`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 11.3 MB (11281335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbd8ee9662704273444a11a2628a08c55058235539da3ea7e96f3be43027311`  
		Last Modified: Fri, 25 Oct 2024 04:49:54 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982fbbf47d3c6ccff37f0a09b37729d82c7be79b8418a3f9890760f66666dc11`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 1.1 MB (1069665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b690f8f3106cb91a4c9197600b5e08e921bd5e48167d98cc698e9b0a085932a`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba53d57ff746cd2ddd87d6ced854a49c95ff92a78a41be2558d7a03fc458d45`  
		Last Modified: Fri, 25 Oct 2024 04:49:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:b05663c6150f09f5c8cc8b3e66d66d5f7decf8d4a8e6501c5fc07ac0bbf1cf02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.6 KB (452592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767141b0e93d0dd0919fa135fc78c8810e5b45b3fd3a831748335d78739fdc15`

```dockerfile
```

-	Layers:
	-	`sha256:bdce856b61660e66f0a1aed4d46ce39f3daa23773798f7a159f6f932a8c99052`  
		Last Modified: Fri, 25 Oct 2024 04:49:52 GMT  
		Size: 421.5 KB (421457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:172b30ef88591f77f9105b14ce9ad0ecf845d37ba979e1a51d7522746131a64f`  
		Last Modified: Fri, 25 Oct 2024 04:49:52 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; ppc64le

```console
$ docker pull composer@sha256:514d02ab64c17c9661db088c7bd01663e131e812fe045faa21c2bc31fe3d14e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73298747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615d60ab2fbdfd79a1d5e5a420e377c65cf49849451d90d947acbabc776ecf0c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:15:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:15:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:15:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:15:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:15:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:15:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:15:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:15:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:59:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac727a268c34206d27f9588c3acfc276afdaf0623dfdc19b7d210a7a881ee4`  
		Last Modified: Sat, 07 Sep 2024 01:44:58 GMT  
		Size: 3.4 MB (3408322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564dcd8f1c226aa29a92bf07685b2a44ccb8ac47267a590bc34a56d25bbbcc4`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3867a87b0703f924c2a7915ce891a49d11c61af6d01613564e485431a9f78`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8622608d41f825e14aa5bd26799c3251549bceef128cf2eae2f52f1ab78913e`  
		Last Modified: Fri, 25 Oct 2024 00:57:34 GMT  
		Size: 12.5 MB (12504690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b9b2cc7fa22223c46604afd8fd56f225e535ca1e7d006d545233f411a4a3c0`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9400d92782aead1169d2e61549cc961ef18b1a2f1468fe9a486ae165d901cf6b`  
		Last Modified: Fri, 25 Oct 2024 00:57:37 GMT  
		Size: 21.3 MB (21285751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ccc474f40266b6e9c07bd2bd8edf9b2feccdf7986579f0a7bfa017cb90929`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd3a52d6da309a1907e5c8310c6411753ee8823a82029f55b265da24bb7566d`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b86ce86d7510dbd92b9dd787d737ff21b3ba726f05cb8546ccc581875d372d`  
		Last Modified: Fri, 25 Oct 2024 03:09:39 GMT  
		Size: 31.4 MB (31402604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74408fea44fbe8cb944832b386c9752e053e23539d049cfad4f03cac46f658f4`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a2527a077a4616f721fa663d0ca3489ff9339802683a454f33b02dc6f3a5ef`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 1.1 MB (1100590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5c0b62db8c3bc2c36a0f17863b36a9da96fecd16d1a11bb1c7bf4a3b8d0cd7`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7567addbbdfe6e8636a200946db7a20e451b5dc0b427ed4c7f7e94676d4512`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:69aa48fe58658360cfb45c08a2c949bc3df95a17f5976a9a53ad335c4975e49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be82f43a76d2877c96c039cebe054f9492a94289537f65c05cee1723c18f2f90`

```dockerfile
```

-	Layers:
	-	`sha256:b8018d8ff9cfcaa1e7981ccd02fbd578df967e6fe88a67a69cb534170a840689`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 2.1 MB (2146343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d004ece9537d1fca87b30c996e372e9be5d9d107c20b6330d54bdfcedd4b43`  
		Last Modified: Fri, 25 Oct 2024 03:13:24 GMT  
		Size: 31.2 KB (31210 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; riscv64

```console
$ docker pull composer@sha256:b85847218fed0f16adfe08f5033a1bb3af32a56c8c5673e6d02addb24b5a0e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70994586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f832367514159c2134fdd37035ec3e2cca2a3910dac92396623338265832020`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:47:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:48:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:48:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:48:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:48:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:48:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 02:23:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160a71fe2c21fa0be03f4ecb3856d46307a8cab34f0749e89c452111c128a28e`  
		Last Modified: Sat, 07 Sep 2024 09:00:45 GMT  
		Size: 3.4 MB (3405216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99de0cdf41fffa764363801fb8a9efbd008b3689317846613f74f55be82ad4ec`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4878284381f1e57d12b980a3d3f2476a10fab26827866948f61cc0a2214a8`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d60d72a55a97ca66240c87e7bc1886bc5aa87d97579097a6d9bab88a75ae1d`  
		Last Modified: Fri, 25 Oct 2024 06:19:30 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55404ef143ec5be664bfb8b7d19253fad3452d91340eac96ad5cb7f88c34e9e`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f1fc6d05b292475d5cdd272dff683e4226cec9930f2394a99a2af5ad9a19c`  
		Last Modified: Fri, 25 Oct 2024 06:19:45 GMT  
		Size: 19.8 MB (19785919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f47a3a529d11fa207f1e96b631df8f8334701948d58152ac5419e07ef6f0b09`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5729eb71e7d125b843a7ed55653966533b980fcc3e19e4ee54ce1e25042a67`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d654c394fa744c0d5afc76db22431671980aa34529d74f487cfbb8e0857966`  
		Last Modified: Fri, 25 Oct 2024 09:50:35 GMT  
		Size: 30.8 MB (30811074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a58738e9c21fa9035cc24b974c8d99fbd269320abe6e366312beca87fb36e14`  
		Last Modified: Fri, 25 Oct 2024 09:50:31 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a9a1e4fd8e3bf5b73e9bba70b3e759e3a9d62b4f8080b8e7b7736c9f348d7`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 1.1 MB (1091833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c042c1d89021264e3a0e83d52ac888997c99220d598ac2eab13ab9c70a716d`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d024f2c5a6071b7c47d8215d6863b5debb180ccf8cb3fabcdd49f7f4e356275`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:ed96702ad5984311f8f58c099ddca3ecd95815043cd65fff7932e96466d3bdad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695236301c163da8ea46b617897966c76d78801c85a766096edea8496bc2ca88`

```dockerfile
```

-	Layers:
	-	`sha256:f8c3581250db3b3d15f4ff5f70365568b7dc495a10d276d3ba4c65caaa52a8b4`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 2.1 MB (2145959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b41aa3f4db744694fac0b293d66cc0a5f4065b53d8145d57fe3db9f9dda1515`  
		Last Modified: Fri, 25 Oct 2024 10:02:49 GMT  
		Size: 31.2 KB (31210 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; s390x

```console
$ docker pull composer@sha256:ea9eaad310b7a1eb6e71a04d999fff99df034c4e6e3cab0143fd27bfe4b485ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72324825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6321a175cb81ff121817f97d578326ba1fd54ea787a0beaa2cb91695fc662418`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:21:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:21:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:21:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:21:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:21:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:42:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9208ede8519d248128a660ad6cbef1b3a33b141374be176c946b5b17b2968ab4`  
		Last Modified: Sat, 07 Sep 2024 00:42:38 GMT  
		Size: 3.5 MB (3473993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabbdadb2babb53e22b8c60bffa37b66bacdd1495093eec38748ca15dabc8287`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2431f4d7c348124f66281fa6433fdcded6e6a093aedb9cdd6fa9c7d87a1407`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8632e206b7bc36b0bfe226c5ec5e94154bc411b3677a2903f0f33e8b4d06d3`  
		Last Modified: Fri, 25 Oct 2024 02:46:23 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950b6d1374ddd91229978b32c87237f1a304df6908d46a3e6c6617379120ecb`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fac98b72a50f285d80ad08584ff62de41c8b0ea0276e5187d77f6dddb0430e4`  
		Last Modified: Fri, 25 Oct 2024 02:46:25 GMT  
		Size: 20.4 MB (20422987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17a61d0d2aae412d208b48c74e3754c9fc7b3f3d0644186eb5a952c01d1d01a`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c55de606062f9878f968213cb2af563401f158dbc5f7b5612b565d5f23a8d8`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a65e35183739b8872e800265ad579948004dd6060f487f2295911c401548795`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 31.3 MB (31338414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c5278f124e717ca16fc2677a7e92e4331ffd330679687f8429c052a4980ca6`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac84ea67d37f2f607682a88ba709d3ca1d7ec45ffa78bf119c0d99f10f2b8d`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 1.1 MB (1098760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a848938d0078bf52df4fa2a8e8aa39affeeeda8eec7e20a5223789502a279b3c`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720a49fb844cd885e2f5780d44f0f9463fa2ebf0019ec117c14b3db14a6df2d3`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:25870622ae7e5ca41223a45c6b4697934b29ca8accf161069a09ea9ce2462cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b49fa50dd59377e3482258ce9585d6abc69ea39fb8ffb16cf1bdc4844fd8505`

```dockerfile
```

-	Layers:
	-	`sha256:33f7b202cdb48083456840312ed4b34234ccd718584600e47a3ae6e88fda4091`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 2.1 MB (2145739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d35b36e0e9d0af4df173a651dd2132192a1fac59fa923225d506c76e3c067`  
		Last Modified: Fri, 25 Oct 2024 06:41:07 GMT  
		Size: 31.2 KB (31168 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8.1`

```console
$ docker pull composer@sha256:0d9ed84312bc8f0094c372b5074ddf89abffddd6e8b91d46f9d39f98cbd512b4
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

### `composer:2.8.1` - linux; amd64

```console
$ docker pull composer@sha256:a92e127cbf279c3b76b3f7a20bc4185c20d8d9b2124ed9e14ce2864d5732541b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71404941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8beffceb940b8587644cf8b44117807db3310b81a15145274e979407fdf7789c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 00:32:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Sep 2024 00:32:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 07 Sep 2024 00:32:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 07 Sep 2024 00:32:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Sep 2024 00:32:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 00:58:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
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
	-	`sha256:41457434eddc5cb99259de159d6a2dad43029452b1ab35975a3209703b9897f4`  
		Last Modified: Fri, 25 Oct 2024 02:16:38 GMT  
		Size: 12.5 MB (12504689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328056f851cc57837c30c7c30c8c1fba0e538db1bdb0f520508b064b7771388b`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66dabf5a41275ff903a5f9ccc8ba9ba981ff4f80da78ac30a649f683542b98c`  
		Last Modified: Fri, 25 Oct 2024 02:16:40 GMT  
		Size: 20.5 MB (20518417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab768f68c87e7a556fcaf812a92acd5c8bf122cc606c956394a6ec4bc208f0f1`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b263e76cc797a1f79fdee350bf8047c4fae8cea974168046c693eec0894545`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8c6e46e9e203f16f774d50fa9cee35406c7828c4fb2f3fe24a868e8cdbe576`  
		Last Modified: Fri, 25 Oct 2024 02:49:45 GMT  
		Size: 30.4 MB (30368357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b27fd7d7d1f5948b1fbe2965594f3bcce94435155a4c35a60b2d608d5ea2fd`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e9f4aa8790c6e63ad881b3900ab9120ea46bad338a9f9dc641af2fb1545dc8`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 1.1 MB (1082386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0fd2babfe1056ad805d84256fb3ec3d62cbaa0be56261a2c2c79a55c100052`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844c7c8ba204421ae47d0e4129dad01122cef45bef67ab49236fe225f2414e48`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.1` - unknown; unknown

```console
$ docker pull composer@sha256:07e9c44c65d288981528af88e5f1ea62f7a8c5f6c4b047fb70b5ced53a2e17d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea337cfabf9cc40ac248aa582e15c6274d46217f1dd85555f1e5d03dd0cf1a8c`

```dockerfile
```

-	Layers:
	-	`sha256:2c8925f43dd72726464493496debe8d9254a2f386420933c92b82b7e17328db8`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 2.1 MB (2147788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac23cb17204e28cf366d9ea488f6d59fad0bc9ebb7c72a01b9f405bcc7ad7f9`  
		Last Modified: Fri, 25 Oct 2024 02:49:43 GMT  
		Size: 31.2 KB (31168 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.1` - linux; arm variant v6

```console
$ docker pull composer@sha256:0731814f66fc6c48bd0c0807e80c89dc2e55e00fbb2f0f313bb22c127f7dd22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68128183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a45cc575b5b053051af22c57e1635b28ace0c5da57cd7994fc69278fc802ca0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:30:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:30:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:30:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:30:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:30:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:51:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78c7a9de9941e89cd785fc3ad14f52410d858d2259f5c9b2a852fd144612520`  
		Last Modified: Sat, 07 Sep 2024 00:48:55 GMT  
		Size: 3.3 MB (3269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbf8fddbe2a872480c609959838de42e95d1f5d5d3d8daadf7a1e44e5c381a2`  
		Last Modified: Sat, 07 Sep 2024 00:48:54 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d88511b2a3086248129999917d9f1e5928426fda8f08edf40ab5bafa37a9`  
		Last Modified: Sat, 07 Sep 2024 00:48:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2913caf4eeb0b47e0a269d5500be80ad644b55b830987923b9b25d7c47b779b6`  
		Last Modified: Fri, 25 Oct 2024 01:12:37 GMT  
		Size: 12.5 MB (12504684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd40e2319cfc199b8ddae2c1022299e653810d5c8fcff021ecf9e71bc732119`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8662dfadda858bf306da862403b12c0ebf0c2c06e8cc29019a10cec84a7ec93`  
		Last Modified: Fri, 25 Oct 2024 01:12:41 GMT  
		Size: 18.7 MB (18711875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0edc47bdf53f26bf4da16fdc4eec8b087534150b52237c0f603b8e571890a9`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43053646b918ed9c5822c17ca4869f057851bb96fcaabed794a5a7ec36dba34`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92515b32642bf33db09f5042274a35b3bf9dfd52f33a78bed3ddb0efab90867`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 29.2 MB (29169219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cececc96a315d5d1a226bb3d06189757c3df3f0bf808c3089f6a8c1ee57b169`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84dd6a8db95fd1cfab72745b588a6020c64ae5fa5e8e7eaf34da667e8998ebca`  
		Last Modified: Fri, 25 Oct 2024 02:11:27 GMT  
		Size: 1.1 MB (1081742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc448f86c117926316d64dc1703afc82d359157f79799cf045e2b86d86c667f6`  
		Last Modified: Mon, 07 Oct 2024 19:58:17 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53acd091d4bf5494fdd8f48f0cbdf90b0375e550a50197d0537f794786e4f735`  
		Last Modified: Fri, 25 Oct 2024 02:11:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.1` - unknown; unknown

```console
$ docker pull composer@sha256:c70376116be9359f8d20e30b55fa4d81f4c5be21b3c1a64c07bb4141515b2ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56b4a57a86ddb1abdf163141d4bd42e27c5f5a4625178f8ea5a460ebe63b6a7`

```dockerfile
```

-	Layers:
	-	`sha256:f8dc929d2da75915ab1de51553bc89259f0f9e61645d119453a123ede1024cbc`  
		Last Modified: Fri, 25 Oct 2024 02:11:26 GMT  
		Size: 31.0 KB (31049 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.1` - linux; arm variant v7

```console
$ docker pull composer@sha256:ff5c72f99787e7cd316fcc4395d97f53f714b04e6a96670c7af40a72e6f4be4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66041602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9624095698de01d4e75e21a48773fbb0d30e5fdca551bad82d4a57860f49e51`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:29:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 22:29:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 22:29:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 22:29:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 22:29:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 22:29:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:29:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:29:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 22:47:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12c01d5f758f7fce28807153dec7a85ae2e307cf0d73f644d575cd875cb994a`  
		Last Modified: Fri, 06 Sep 2024 23:45:25 GMT  
		Size: 3.1 MB (3079568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c3e48f803b4ca0c1ec0b16f85f80f0a17b054845918112eb73b80eb9bd7297`  
		Last Modified: Fri, 06 Sep 2024 23:45:23 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7c21bdd57d9b7548f08c79a56f0a75d4e14a705967ae55d0450a10f0c6c43e`  
		Last Modified: Fri, 06 Sep 2024 23:45:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efe62db4f1f9f85f795e6cc1e7f8d835b0a8657d2a60143ba15d82d5863841`  
		Last Modified: Fri, 25 Oct 2024 02:37:26 GMT  
		Size: 12.5 MB (12504680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204359c9c9eb5cb76578981a5c068e3fac227ce0e7df1a86096569dc1230c85`  
		Last Modified: Fri, 25 Oct 2024 02:37:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2762620a9d567bff0020a3cda73a630f1a993bda6921efbd9554d75c9fd3377f`  
		Last Modified: Fri, 25 Oct 2024 02:37:28 GMT  
		Size: 17.5 MB (17478737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5a9688a15e4908bcd1ed18d76acd39f8678dd66decafbae483b2c884bf1c02`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66727798fd727eda6cfc82ff904b3773b442a67ae9e11967aac36d92e2e9be32`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ef898d316952fe64642bc94179ed2cc82e7c9404af0c91e8d0f5152097b5e8`  
		Last Modified: Fri, 25 Oct 2024 02:49:33 GMT  
		Size: 28.8 MB (28797969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48238d159943a0389cdf60849c19e218b8aeae434d69dfb9050fc0c71115bf9a`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b58a4408498db5e9ab01414bd6385d998cb8f21dabb6be95a750906ae5b1f3c`  
		Last Modified: Fri, 25 Oct 2024 02:51:11 GMT  
		Size: 1.1 MB (1060749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6503f2fca1c6898aa87f48db0cd634630c52a3268995b25f8caffb8bee8475a`  
		Last Modified: Fri, 25 Oct 2024 02:51:10 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fabf1a07b3bdac00b08274fdd1b79967aabe3c4f6526c99bd7c80255a9c5c07`  
		Last Modified: Fri, 25 Oct 2024 02:51:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.1` - unknown; unknown

```console
$ docker pull composer@sha256:29a9862fa241870ee9e9744c1234cb68935ff206aa43236d0f21de7a297aa903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38703114d6a9c5f9de4eeae5759012126d06ad4b07f8ce0d8348157c7a9c8ff`

```dockerfile
```

-	Layers:
	-	`sha256:d1bb5967213b8eacf025fbae03caf581e6326e1e330d4c01ebb58cbb27eac34e`  
		Last Modified: Fri, 25 Oct 2024 02:51:10 GMT  
		Size: 2.1 MB (2148109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b80953e51404205596c003a9bf2f30426361239bd88f3d5879f028987ab723e`  
		Last Modified: Fri, 25 Oct 2024 02:51:10 GMT  
		Size: 31.3 KB (31264 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:4575910a0d4a9df7ffd9da094b4d4e73f4a2be32d36246e7329d623454ae6329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72860831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3c631a63beae9b8ee7bcc06a3f14113fb4fc0765bc591470a50ddcb080bde6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 00:43:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Sep 2024 00:43:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 07 Sep 2024 00:43:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 07 Sep 2024 00:43:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Sep 2024 00:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 01:04:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ef8ad75958cd7eb0e453d0f85e72134ef3976f8351b5742370df35bc60ed42`  
		Last Modified: Sat, 07 Sep 2024 02:23:50 GMT  
		Size: 3.3 MB (3333388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f80c1299f6c626e7df88761199f03734cced725870be7a04dd95bf11e80104`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb3615e2ca5466e128fbfbd9bfcaa4cc0a7c5935f1d980f13d765c6bfde9144`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b324dba8535eea2357b994da9864afef849388a4c8e80235090810383253f31`  
		Last Modified: Fri, 25 Oct 2024 02:19:36 GMT  
		Size: 12.5 MB (12504686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e479347c3f32eee03df523edd0f1a869f7a7636702922f9d5db1ac9024ea211`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6b8889455c447cc20eb2d9881a51c22cdac63cc440a2e647d8e5c2c7f13cfc`  
		Last Modified: Fri, 25 Oct 2024 02:19:37 GMT  
		Size: 20.9 MB (20940181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eeecc80b8f4736452eb3054bbf21ee480f6a4eb724b114b31cb94ab034f53c`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93069ffa1c1f8ac20ef6e8c62fa71d5ba3e5ae3f4ce6b97965ae1a5a0f2562bb`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98eea5daa433de13908b8daf3e98a58f41b648a198629693556299898d3050f`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 30.9 MB (30879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24933c1ee11a72c73a8c1d127f5254b2e1a343115700bfd5d40922a70347acac`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b210b09c1b5dce1b5094e57caea0452e5776bb3f43f7c8d5e388cb69ced01d44`  
		Last Modified: Fri, 25 Oct 2024 04:26:34 GMT  
		Size: 1.1 MB (1090886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b5d0e63e39d147a5ff8487e68431854584ec90cd07275ae0a841e77cd539f9`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec155f53f4ab45bdf10f33bb071a35ac7b7777b50897579201c20b6fc9223dec`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.1` - unknown; unknown

```console
$ docker pull composer@sha256:f165a4ca8adb8f345a4fbbd2d0e6ce7423ff3cccbe80bc6b4f74cd433103cc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732da8b9d36aadf2652af89a530a393a085bba4c677c1b4310dd4bb506d19e83`

```dockerfile
```

-	Layers:
	-	`sha256:84135c99834ab363c853372259a9196b615745b6251e3f49a3b9ae0f2786b92a`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 2.1 MB (2147939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9042f9e0e6a93e08e64a8eb7f1f3caba691460c8068e0cafe27485b1de12b43`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 31.3 KB (31296 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.1` - linux; 386

```console
$ docker pull composer@sha256:62aac98b8ddd75628e726dfa617ad4cb8999c542b5694731ad2a759ce8db7f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52499599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3c0137caf6333752ae7e9a4c6dab56a54051e5561cd9e4eb1bf546ff340517`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:57:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 22:57:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 22:57:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 22:57:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 22:57:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 22:57:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:57:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:57:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:42:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
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
	-	`sha256:9eaf7c1d9791c6b12392f1f767948304f2c2e69cb0878ecec4d5df2be5af4dca`  
		Last Modified: Fri, 25 Oct 2024 04:22:20 GMT  
		Size: 12.5 MB (12504687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0bab9c844ca004a8fd6a7ea2a92c041012b047b66151b6d55f81e1e29009e`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609f4e456e59a3c94a5761b23648a66de98737427aa781c0b05b3296eacbef62`  
		Last Modified: Fri, 25 Oct 2024 04:22:23 GMT  
		Size: 20.8 MB (20818182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4455a0ae1ac0aca52a62943181a6673cf4e49459913cfea722ceb78acf98f28`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f23e94c0f2162ee0e26724220289d3609acb53f3117201cba2c8e6e5021efa`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 19.7 KB (19716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119b4f99527dc6b667937203167ecff4617fc1078093fefa09df11b56496bf86`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 11.3 MB (11281335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbd8ee9662704273444a11a2628a08c55058235539da3ea7e96f3be43027311`  
		Last Modified: Fri, 25 Oct 2024 04:49:54 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982fbbf47d3c6ccff37f0a09b37729d82c7be79b8418a3f9890760f66666dc11`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 1.1 MB (1069665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b690f8f3106cb91a4c9197600b5e08e921bd5e48167d98cc698e9b0a085932a`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba53d57ff746cd2ddd87d6ced854a49c95ff92a78a41be2558d7a03fc458d45`  
		Last Modified: Fri, 25 Oct 2024 04:49:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.1` - unknown; unknown

```console
$ docker pull composer@sha256:b05663c6150f09f5c8cc8b3e66d66d5f7decf8d4a8e6501c5fc07ac0bbf1cf02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.6 KB (452592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767141b0e93d0dd0919fa135fc78c8810e5b45b3fd3a831748335d78739fdc15`

```dockerfile
```

-	Layers:
	-	`sha256:bdce856b61660e66f0a1aed4d46ce39f3daa23773798f7a159f6f932a8c99052`  
		Last Modified: Fri, 25 Oct 2024 04:49:52 GMT  
		Size: 421.5 KB (421457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:172b30ef88591f77f9105b14ce9ad0ecf845d37ba979e1a51d7522746131a64f`  
		Last Modified: Fri, 25 Oct 2024 04:49:52 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.1` - linux; ppc64le

```console
$ docker pull composer@sha256:514d02ab64c17c9661db088c7bd01663e131e812fe045faa21c2bc31fe3d14e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73298747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615d60ab2fbdfd79a1d5e5a420e377c65cf49849451d90d947acbabc776ecf0c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:15:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:15:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:15:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:15:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:15:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:15:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:15:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:15:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:59:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac727a268c34206d27f9588c3acfc276afdaf0623dfdc19b7d210a7a881ee4`  
		Last Modified: Sat, 07 Sep 2024 01:44:58 GMT  
		Size: 3.4 MB (3408322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564dcd8f1c226aa29a92bf07685b2a44ccb8ac47267a590bc34a56d25bbbcc4`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3867a87b0703f924c2a7915ce891a49d11c61af6d01613564e485431a9f78`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8622608d41f825e14aa5bd26799c3251549bceef128cf2eae2f52f1ab78913e`  
		Last Modified: Fri, 25 Oct 2024 00:57:34 GMT  
		Size: 12.5 MB (12504690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b9b2cc7fa22223c46604afd8fd56f225e535ca1e7d006d545233f411a4a3c0`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9400d92782aead1169d2e61549cc961ef18b1a2f1468fe9a486ae165d901cf6b`  
		Last Modified: Fri, 25 Oct 2024 00:57:37 GMT  
		Size: 21.3 MB (21285751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ccc474f40266b6e9c07bd2bd8edf9b2feccdf7986579f0a7bfa017cb90929`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd3a52d6da309a1907e5c8310c6411753ee8823a82029f55b265da24bb7566d`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b86ce86d7510dbd92b9dd787d737ff21b3ba726f05cb8546ccc581875d372d`  
		Last Modified: Fri, 25 Oct 2024 03:09:39 GMT  
		Size: 31.4 MB (31402604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74408fea44fbe8cb944832b386c9752e053e23539d049cfad4f03cac46f658f4`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a2527a077a4616f721fa663d0ca3489ff9339802683a454f33b02dc6f3a5ef`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 1.1 MB (1100590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5c0b62db8c3bc2c36a0f17863b36a9da96fecd16d1a11bb1c7bf4a3b8d0cd7`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7567addbbdfe6e8636a200946db7a20e451b5dc0b427ed4c7f7e94676d4512`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.1` - unknown; unknown

```console
$ docker pull composer@sha256:69aa48fe58658360cfb45c08a2c949bc3df95a17f5976a9a53ad335c4975e49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be82f43a76d2877c96c039cebe054f9492a94289537f65c05cee1723c18f2f90`

```dockerfile
```

-	Layers:
	-	`sha256:b8018d8ff9cfcaa1e7981ccd02fbd578df967e6fe88a67a69cb534170a840689`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 2.1 MB (2146343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d004ece9537d1fca87b30c996e372e9be5d9d107c20b6330d54bdfcedd4b43`  
		Last Modified: Fri, 25 Oct 2024 03:13:24 GMT  
		Size: 31.2 KB (31210 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.1` - linux; riscv64

```console
$ docker pull composer@sha256:b85847218fed0f16adfe08f5033a1bb3af32a56c8c5673e6d02addb24b5a0e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70994586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f832367514159c2134fdd37035ec3e2cca2a3910dac92396623338265832020`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:47:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:48:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:48:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:48:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:48:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:48:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 02:23:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160a71fe2c21fa0be03f4ecb3856d46307a8cab34f0749e89c452111c128a28e`  
		Last Modified: Sat, 07 Sep 2024 09:00:45 GMT  
		Size: 3.4 MB (3405216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99de0cdf41fffa764363801fb8a9efbd008b3689317846613f74f55be82ad4ec`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4878284381f1e57d12b980a3d3f2476a10fab26827866948f61cc0a2214a8`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d60d72a55a97ca66240c87e7bc1886bc5aa87d97579097a6d9bab88a75ae1d`  
		Last Modified: Fri, 25 Oct 2024 06:19:30 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55404ef143ec5be664bfb8b7d19253fad3452d91340eac96ad5cb7f88c34e9e`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f1fc6d05b292475d5cdd272dff683e4226cec9930f2394a99a2af5ad9a19c`  
		Last Modified: Fri, 25 Oct 2024 06:19:45 GMT  
		Size: 19.8 MB (19785919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f47a3a529d11fa207f1e96b631df8f8334701948d58152ac5419e07ef6f0b09`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5729eb71e7d125b843a7ed55653966533b980fcc3e19e4ee54ce1e25042a67`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d654c394fa744c0d5afc76db22431671980aa34529d74f487cfbb8e0857966`  
		Last Modified: Fri, 25 Oct 2024 09:50:35 GMT  
		Size: 30.8 MB (30811074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a58738e9c21fa9035cc24b974c8d99fbd269320abe6e366312beca87fb36e14`  
		Last Modified: Fri, 25 Oct 2024 09:50:31 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a9a1e4fd8e3bf5b73e9bba70b3e759e3a9d62b4f8080b8e7b7736c9f348d7`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 1.1 MB (1091833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c042c1d89021264e3a0e83d52ac888997c99220d598ac2eab13ab9c70a716d`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d024f2c5a6071b7c47d8215d6863b5debb180ccf8cb3fabcdd49f7f4e356275`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.1` - unknown; unknown

```console
$ docker pull composer@sha256:ed96702ad5984311f8f58c099ddca3ecd95815043cd65fff7932e96466d3bdad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695236301c163da8ea46b617897966c76d78801c85a766096edea8496bc2ca88`

```dockerfile
```

-	Layers:
	-	`sha256:f8c3581250db3b3d15f4ff5f70365568b7dc495a10d276d3ba4c65caaa52a8b4`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 2.1 MB (2145959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b41aa3f4db744694fac0b293d66cc0a5f4065b53d8145d57fe3db9f9dda1515`  
		Last Modified: Fri, 25 Oct 2024 10:02:49 GMT  
		Size: 31.2 KB (31210 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.1` - linux; s390x

```console
$ docker pull composer@sha256:ea9eaad310b7a1eb6e71a04d999fff99df034c4e6e3cab0143fd27bfe4b485ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72324825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6321a175cb81ff121817f97d578326ba1fd54ea787a0beaa2cb91695fc662418`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:21:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:21:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:21:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:21:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:21:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:42:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9208ede8519d248128a660ad6cbef1b3a33b141374be176c946b5b17b2968ab4`  
		Last Modified: Sat, 07 Sep 2024 00:42:38 GMT  
		Size: 3.5 MB (3473993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabbdadb2babb53e22b8c60bffa37b66bacdd1495093eec38748ca15dabc8287`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2431f4d7c348124f66281fa6433fdcded6e6a093aedb9cdd6fa9c7d87a1407`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8632e206b7bc36b0bfe226c5ec5e94154bc411b3677a2903f0f33e8b4d06d3`  
		Last Modified: Fri, 25 Oct 2024 02:46:23 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950b6d1374ddd91229978b32c87237f1a304df6908d46a3e6c6617379120ecb`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fac98b72a50f285d80ad08584ff62de41c8b0ea0276e5187d77f6dddb0430e4`  
		Last Modified: Fri, 25 Oct 2024 02:46:25 GMT  
		Size: 20.4 MB (20422987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17a61d0d2aae412d208b48c74e3754c9fc7b3f3d0644186eb5a952c01d1d01a`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c55de606062f9878f968213cb2af563401f158dbc5f7b5612b565d5f23a8d8`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a65e35183739b8872e800265ad579948004dd6060f487f2295911c401548795`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 31.3 MB (31338414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c5278f124e717ca16fc2677a7e92e4331ffd330679687f8429c052a4980ca6`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac84ea67d37f2f607682a88ba709d3ca1d7ec45ffa78bf119c0d99f10f2b8d`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 1.1 MB (1098760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a848938d0078bf52df4fa2a8e8aa39affeeeda8eec7e20a5223789502a279b3c`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720a49fb844cd885e2f5780d44f0f9463fa2ebf0019ec117c14b3db14a6df2d3`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.1` - unknown; unknown

```console
$ docker pull composer@sha256:25870622ae7e5ca41223a45c6b4697934b29ca8accf161069a09ea9ce2462cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b49fa50dd59377e3482258ce9585d6abc69ea39fb8ffb16cf1bdc4844fd8505`

```dockerfile
```

-	Layers:
	-	`sha256:33f7b202cdb48083456840312ed4b34234ccd718584600e47a3ae6e88fda4091`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 2.1 MB (2145739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d35b36e0e9d0af4df173a651dd2132192a1fac59fa923225d506c76e3c067`  
		Last Modified: Fri, 25 Oct 2024 06:41:07 GMT  
		Size: 31.2 KB (31168 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:0d9ed84312bc8f0094c372b5074ddf89abffddd6e8b91d46f9d39f98cbd512b4
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
$ docker pull composer@sha256:a92e127cbf279c3b76b3f7a20bc4185c20d8d9b2124ed9e14ce2864d5732541b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71404941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8beffceb940b8587644cf8b44117807db3310b81a15145274e979407fdf7789c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 00:32:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Sep 2024 00:32:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 07 Sep 2024 00:32:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 07 Sep 2024 00:32:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Sep 2024 00:32:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 00:58:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
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
	-	`sha256:41457434eddc5cb99259de159d6a2dad43029452b1ab35975a3209703b9897f4`  
		Last Modified: Fri, 25 Oct 2024 02:16:38 GMT  
		Size: 12.5 MB (12504689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328056f851cc57837c30c7c30c8c1fba0e538db1bdb0f520508b064b7771388b`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66dabf5a41275ff903a5f9ccc8ba9ba981ff4f80da78ac30a649f683542b98c`  
		Last Modified: Fri, 25 Oct 2024 02:16:40 GMT  
		Size: 20.5 MB (20518417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab768f68c87e7a556fcaf812a92acd5c8bf122cc606c956394a6ec4bc208f0f1`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b263e76cc797a1f79fdee350bf8047c4fae8cea974168046c693eec0894545`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8c6e46e9e203f16f774d50fa9cee35406c7828c4fb2f3fe24a868e8cdbe576`  
		Last Modified: Fri, 25 Oct 2024 02:49:45 GMT  
		Size: 30.4 MB (30368357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b27fd7d7d1f5948b1fbe2965594f3bcce94435155a4c35a60b2d608d5ea2fd`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e9f4aa8790c6e63ad881b3900ab9120ea46bad338a9f9dc641af2fb1545dc8`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 1.1 MB (1082386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0fd2babfe1056ad805d84256fb3ec3d62cbaa0be56261a2c2c79a55c100052`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844c7c8ba204421ae47d0e4129dad01122cef45bef67ab49236fe225f2414e48`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:07e9c44c65d288981528af88e5f1ea62f7a8c5f6c4b047fb70b5ced53a2e17d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea337cfabf9cc40ac248aa582e15c6274d46217f1dd85555f1e5d03dd0cf1a8c`

```dockerfile
```

-	Layers:
	-	`sha256:2c8925f43dd72726464493496debe8d9254a2f386420933c92b82b7e17328db8`  
		Last Modified: Fri, 25 Oct 2024 02:49:44 GMT  
		Size: 2.1 MB (2147788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac23cb17204e28cf366d9ea488f6d59fad0bc9ebb7c72a01b9f405bcc7ad7f9`  
		Last Modified: Fri, 25 Oct 2024 02:49:43 GMT  
		Size: 31.2 KB (31168 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:0731814f66fc6c48bd0c0807e80c89dc2e55e00fbb2f0f313bb22c127f7dd22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68128183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a45cc575b5b053051af22c57e1635b28ace0c5da57cd7994fc69278fc802ca0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:30:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:30:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:30:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:30:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:30:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:51:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78c7a9de9941e89cd785fc3ad14f52410d858d2259f5c9b2a852fd144612520`  
		Last Modified: Sat, 07 Sep 2024 00:48:55 GMT  
		Size: 3.3 MB (3269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbf8fddbe2a872480c609959838de42e95d1f5d5d3d8daadf7a1e44e5c381a2`  
		Last Modified: Sat, 07 Sep 2024 00:48:54 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d88511b2a3086248129999917d9f1e5928426fda8f08edf40ab5bafa37a9`  
		Last Modified: Sat, 07 Sep 2024 00:48:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2913caf4eeb0b47e0a269d5500be80ad644b55b830987923b9b25d7c47b779b6`  
		Last Modified: Fri, 25 Oct 2024 01:12:37 GMT  
		Size: 12.5 MB (12504684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd40e2319cfc199b8ddae2c1022299e653810d5c8fcff021ecf9e71bc732119`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8662dfadda858bf306da862403b12c0ebf0c2c06e8cc29019a10cec84a7ec93`  
		Last Modified: Fri, 25 Oct 2024 01:12:41 GMT  
		Size: 18.7 MB (18711875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0edc47bdf53f26bf4da16fdc4eec8b087534150b52237c0f603b8e571890a9`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43053646b918ed9c5822c17ca4869f057851bb96fcaabed794a5a7ec36dba34`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92515b32642bf33db09f5042274a35b3bf9dfd52f33a78bed3ddb0efab90867`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 29.2 MB (29169219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cececc96a315d5d1a226bb3d06189757c3df3f0bf808c3089f6a8c1ee57b169`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84dd6a8db95fd1cfab72745b588a6020c64ae5fa5e8e7eaf34da667e8998ebca`  
		Last Modified: Fri, 25 Oct 2024 02:11:27 GMT  
		Size: 1.1 MB (1081742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc448f86c117926316d64dc1703afc82d359157f79799cf045e2b86d86c667f6`  
		Last Modified: Mon, 07 Oct 2024 19:58:17 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53acd091d4bf5494fdd8f48f0cbdf90b0375e550a50197d0537f794786e4f735`  
		Last Modified: Fri, 25 Oct 2024 02:11:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:c70376116be9359f8d20e30b55fa4d81f4c5be21b3c1a64c07bb4141515b2ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56b4a57a86ddb1abdf163141d4bd42e27c5f5a4625178f8ea5a460ebe63b6a7`

```dockerfile
```

-	Layers:
	-	`sha256:f8dc929d2da75915ab1de51553bc89259f0f9e61645d119453a123ede1024cbc`  
		Last Modified: Fri, 25 Oct 2024 02:11:26 GMT  
		Size: 31.0 KB (31049 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:ff5c72f99787e7cd316fcc4395d97f53f714b04e6a96670c7af40a72e6f4be4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66041602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9624095698de01d4e75e21a48773fbb0d30e5fdca551bad82d4a57860f49e51`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:29:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 22:29:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 22:29:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 22:29:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 22:29:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 22:29:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:29:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:29:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 22:47:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12c01d5f758f7fce28807153dec7a85ae2e307cf0d73f644d575cd875cb994a`  
		Last Modified: Fri, 06 Sep 2024 23:45:25 GMT  
		Size: 3.1 MB (3079568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c3e48f803b4ca0c1ec0b16f85f80f0a17b054845918112eb73b80eb9bd7297`  
		Last Modified: Fri, 06 Sep 2024 23:45:23 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7c21bdd57d9b7548f08c79a56f0a75d4e14a705967ae55d0450a10f0c6c43e`  
		Last Modified: Fri, 06 Sep 2024 23:45:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efe62db4f1f9f85f795e6cc1e7f8d835b0a8657d2a60143ba15d82d5863841`  
		Last Modified: Fri, 25 Oct 2024 02:37:26 GMT  
		Size: 12.5 MB (12504680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204359c9c9eb5cb76578981a5c068e3fac227ce0e7df1a86096569dc1230c85`  
		Last Modified: Fri, 25 Oct 2024 02:37:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2762620a9d567bff0020a3cda73a630f1a993bda6921efbd9554d75c9fd3377f`  
		Last Modified: Fri, 25 Oct 2024 02:37:28 GMT  
		Size: 17.5 MB (17478737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5a9688a15e4908bcd1ed18d76acd39f8678dd66decafbae483b2c884bf1c02`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66727798fd727eda6cfc82ff904b3773b442a67ae9e11967aac36d92e2e9be32`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ef898d316952fe64642bc94179ed2cc82e7c9404af0c91e8d0f5152097b5e8`  
		Last Modified: Fri, 25 Oct 2024 02:49:33 GMT  
		Size: 28.8 MB (28797969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48238d159943a0389cdf60849c19e218b8aeae434d69dfb9050fc0c71115bf9a`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b58a4408498db5e9ab01414bd6385d998cb8f21dabb6be95a750906ae5b1f3c`  
		Last Modified: Fri, 25 Oct 2024 02:51:11 GMT  
		Size: 1.1 MB (1060749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6503f2fca1c6898aa87f48db0cd634630c52a3268995b25f8caffb8bee8475a`  
		Last Modified: Fri, 25 Oct 2024 02:51:10 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fabf1a07b3bdac00b08274fdd1b79967aabe3c4f6526c99bd7c80255a9c5c07`  
		Last Modified: Fri, 25 Oct 2024 02:51:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:29a9862fa241870ee9e9744c1234cb68935ff206aa43236d0f21de7a297aa903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38703114d6a9c5f9de4eeae5759012126d06ad4b07f8ce0d8348157c7a9c8ff`

```dockerfile
```

-	Layers:
	-	`sha256:d1bb5967213b8eacf025fbae03caf581e6326e1e330d4c01ebb58cbb27eac34e`  
		Last Modified: Fri, 25 Oct 2024 02:51:10 GMT  
		Size: 2.1 MB (2148109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b80953e51404205596c003a9bf2f30426361239bd88f3d5879f028987ab723e`  
		Last Modified: Fri, 25 Oct 2024 02:51:10 GMT  
		Size: 31.3 KB (31264 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:4575910a0d4a9df7ffd9da094b4d4e73f4a2be32d36246e7329d623454ae6329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72860831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3c631a63beae9b8ee7bcc06a3f14113fb4fc0765bc591470a50ddcb080bde6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 00:43:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Sep 2024 00:43:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 07 Sep 2024 00:43:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 07 Sep 2024 00:43:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Sep 2024 00:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 01:04:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ef8ad75958cd7eb0e453d0f85e72134ef3976f8351b5742370df35bc60ed42`  
		Last Modified: Sat, 07 Sep 2024 02:23:50 GMT  
		Size: 3.3 MB (3333388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f80c1299f6c626e7df88761199f03734cced725870be7a04dd95bf11e80104`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb3615e2ca5466e128fbfbd9bfcaa4cc0a7c5935f1d980f13d765c6bfde9144`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b324dba8535eea2357b994da9864afef849388a4c8e80235090810383253f31`  
		Last Modified: Fri, 25 Oct 2024 02:19:36 GMT  
		Size: 12.5 MB (12504686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e479347c3f32eee03df523edd0f1a869f7a7636702922f9d5db1ac9024ea211`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6b8889455c447cc20eb2d9881a51c22cdac63cc440a2e647d8e5c2c7f13cfc`  
		Last Modified: Fri, 25 Oct 2024 02:19:37 GMT  
		Size: 20.9 MB (20940181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eeecc80b8f4736452eb3054bbf21ee480f6a4eb724b114b31cb94ab034f53c`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93069ffa1c1f8ac20ef6e8c62fa71d5ba3e5ae3f4ce6b97965ae1a5a0f2562bb`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98eea5daa433de13908b8daf3e98a58f41b648a198629693556299898d3050f`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 30.9 MB (30879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24933c1ee11a72c73a8c1d127f5254b2e1a343115700bfd5d40922a70347acac`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b210b09c1b5dce1b5094e57caea0452e5776bb3f43f7c8d5e388cb69ced01d44`  
		Last Modified: Fri, 25 Oct 2024 04:26:34 GMT  
		Size: 1.1 MB (1090886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b5d0e63e39d147a5ff8487e68431854584ec90cd07275ae0a841e77cd539f9`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec155f53f4ab45bdf10f33bb071a35ac7b7777b50897579201c20b6fc9223dec`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:f165a4ca8adb8f345a4fbbd2d0e6ce7423ff3cccbe80bc6b4f74cd433103cc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732da8b9d36aadf2652af89a530a393a085bba4c677c1b4310dd4bb506d19e83`

```dockerfile
```

-	Layers:
	-	`sha256:84135c99834ab363c853372259a9196b615745b6251e3f49a3b9ae0f2786b92a`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 2.1 MB (2147939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9042f9e0e6a93e08e64a8eb7f1f3caba691460c8068e0cafe27485b1de12b43`  
		Last Modified: Fri, 25 Oct 2024 04:26:33 GMT  
		Size: 31.3 KB (31296 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:62aac98b8ddd75628e726dfa617ad4cb8999c542b5694731ad2a759ce8db7f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52499599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3c0137caf6333752ae7e9a4c6dab56a54051e5561cd9e4eb1bf546ff340517`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:57:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 22:57:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 22:57:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 22:57:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 22:57:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 22:57:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:57:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:57:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:42:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
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
	-	`sha256:9eaf7c1d9791c6b12392f1f767948304f2c2e69cb0878ecec4d5df2be5af4dca`  
		Last Modified: Fri, 25 Oct 2024 04:22:20 GMT  
		Size: 12.5 MB (12504687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0bab9c844ca004a8fd6a7ea2a92c041012b047b66151b6d55f81e1e29009e`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609f4e456e59a3c94a5761b23648a66de98737427aa781c0b05b3296eacbef62`  
		Last Modified: Fri, 25 Oct 2024 04:22:23 GMT  
		Size: 20.8 MB (20818182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4455a0ae1ac0aca52a62943181a6673cf4e49459913cfea722ceb78acf98f28`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f23e94c0f2162ee0e26724220289d3609acb53f3117201cba2c8e6e5021efa`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 19.7 KB (19716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119b4f99527dc6b667937203167ecff4617fc1078093fefa09df11b56496bf86`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 11.3 MB (11281335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbd8ee9662704273444a11a2628a08c55058235539da3ea7e96f3be43027311`  
		Last Modified: Fri, 25 Oct 2024 04:49:54 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982fbbf47d3c6ccff37f0a09b37729d82c7be79b8418a3f9890760f66666dc11`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 1.1 MB (1069665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b690f8f3106cb91a4c9197600b5e08e921bd5e48167d98cc698e9b0a085932a`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba53d57ff746cd2ddd87d6ced854a49c95ff92a78a41be2558d7a03fc458d45`  
		Last Modified: Fri, 25 Oct 2024 04:49:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:b05663c6150f09f5c8cc8b3e66d66d5f7decf8d4a8e6501c5fc07ac0bbf1cf02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.6 KB (452592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767141b0e93d0dd0919fa135fc78c8810e5b45b3fd3a831748335d78739fdc15`

```dockerfile
```

-	Layers:
	-	`sha256:bdce856b61660e66f0a1aed4d46ce39f3daa23773798f7a159f6f932a8c99052`  
		Last Modified: Fri, 25 Oct 2024 04:49:52 GMT  
		Size: 421.5 KB (421457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:172b30ef88591f77f9105b14ce9ad0ecf845d37ba979e1a51d7522746131a64f`  
		Last Modified: Fri, 25 Oct 2024 04:49:52 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:514d02ab64c17c9661db088c7bd01663e131e812fe045faa21c2bc31fe3d14e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73298747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615d60ab2fbdfd79a1d5e5a420e377c65cf49849451d90d947acbabc776ecf0c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:15:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:15:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:15:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:15:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:15:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:15:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:15:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:15:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:59:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac727a268c34206d27f9588c3acfc276afdaf0623dfdc19b7d210a7a881ee4`  
		Last Modified: Sat, 07 Sep 2024 01:44:58 GMT  
		Size: 3.4 MB (3408322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564dcd8f1c226aa29a92bf07685b2a44ccb8ac47267a590bc34a56d25bbbcc4`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3867a87b0703f924c2a7915ce891a49d11c61af6d01613564e485431a9f78`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8622608d41f825e14aa5bd26799c3251549bceef128cf2eae2f52f1ab78913e`  
		Last Modified: Fri, 25 Oct 2024 00:57:34 GMT  
		Size: 12.5 MB (12504690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b9b2cc7fa22223c46604afd8fd56f225e535ca1e7d006d545233f411a4a3c0`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9400d92782aead1169d2e61549cc961ef18b1a2f1468fe9a486ae165d901cf6b`  
		Last Modified: Fri, 25 Oct 2024 00:57:37 GMT  
		Size: 21.3 MB (21285751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ccc474f40266b6e9c07bd2bd8edf9b2feccdf7986579f0a7bfa017cb90929`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd3a52d6da309a1907e5c8310c6411753ee8823a82029f55b265da24bb7566d`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b86ce86d7510dbd92b9dd787d737ff21b3ba726f05cb8546ccc581875d372d`  
		Last Modified: Fri, 25 Oct 2024 03:09:39 GMT  
		Size: 31.4 MB (31402604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74408fea44fbe8cb944832b386c9752e053e23539d049cfad4f03cac46f658f4`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a2527a077a4616f721fa663d0ca3489ff9339802683a454f33b02dc6f3a5ef`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 1.1 MB (1100590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5c0b62db8c3bc2c36a0f17863b36a9da96fecd16d1a11bb1c7bf4a3b8d0cd7`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7567addbbdfe6e8636a200946db7a20e451b5dc0b427ed4c7f7e94676d4512`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:69aa48fe58658360cfb45c08a2c949bc3df95a17f5976a9a53ad335c4975e49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be82f43a76d2877c96c039cebe054f9492a94289537f65c05cee1723c18f2f90`

```dockerfile
```

-	Layers:
	-	`sha256:b8018d8ff9cfcaa1e7981ccd02fbd578df967e6fe88a67a69cb534170a840689`  
		Last Modified: Fri, 25 Oct 2024 03:13:25 GMT  
		Size: 2.1 MB (2146343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d004ece9537d1fca87b30c996e372e9be5d9d107c20b6330d54bdfcedd4b43`  
		Last Modified: Fri, 25 Oct 2024 03:13:24 GMT  
		Size: 31.2 KB (31210 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:b85847218fed0f16adfe08f5033a1bb3af32a56c8c5673e6d02addb24b5a0e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70994586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f832367514159c2134fdd37035ec3e2cca2a3910dac92396623338265832020`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:47:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:48:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:48:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:48:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:48:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:48:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 02:23:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160a71fe2c21fa0be03f4ecb3856d46307a8cab34f0749e89c452111c128a28e`  
		Last Modified: Sat, 07 Sep 2024 09:00:45 GMT  
		Size: 3.4 MB (3405216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99de0cdf41fffa764363801fb8a9efbd008b3689317846613f74f55be82ad4ec`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4878284381f1e57d12b980a3d3f2476a10fab26827866948f61cc0a2214a8`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d60d72a55a97ca66240c87e7bc1886bc5aa87d97579097a6d9bab88a75ae1d`  
		Last Modified: Fri, 25 Oct 2024 06:19:30 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55404ef143ec5be664bfb8b7d19253fad3452d91340eac96ad5cb7f88c34e9e`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f1fc6d05b292475d5cdd272dff683e4226cec9930f2394a99a2af5ad9a19c`  
		Last Modified: Fri, 25 Oct 2024 06:19:45 GMT  
		Size: 19.8 MB (19785919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f47a3a529d11fa207f1e96b631df8f8334701948d58152ac5419e07ef6f0b09`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5729eb71e7d125b843a7ed55653966533b980fcc3e19e4ee54ce1e25042a67`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d654c394fa744c0d5afc76db22431671980aa34529d74f487cfbb8e0857966`  
		Last Modified: Fri, 25 Oct 2024 09:50:35 GMT  
		Size: 30.8 MB (30811074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a58738e9c21fa9035cc24b974c8d99fbd269320abe6e366312beca87fb36e14`  
		Last Modified: Fri, 25 Oct 2024 09:50:31 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a9a1e4fd8e3bf5b73e9bba70b3e759e3a9d62b4f8080b8e7b7736c9f348d7`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 1.1 MB (1091833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c042c1d89021264e3a0e83d52ac888997c99220d598ac2eab13ab9c70a716d`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d024f2c5a6071b7c47d8215d6863b5debb180ccf8cb3fabcdd49f7f4e356275`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:ed96702ad5984311f8f58c099ddca3ecd95815043cd65fff7932e96466d3bdad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695236301c163da8ea46b617897966c76d78801c85a766096edea8496bc2ca88`

```dockerfile
```

-	Layers:
	-	`sha256:f8c3581250db3b3d15f4ff5f70365568b7dc495a10d276d3ba4c65caaa52a8b4`  
		Last Modified: Fri, 25 Oct 2024 10:02:50 GMT  
		Size: 2.1 MB (2145959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b41aa3f4db744694fac0b293d66cc0a5f4065b53d8145d57fe3db9f9dda1515`  
		Last Modified: Fri, 25 Oct 2024 10:02:49 GMT  
		Size: 31.2 KB (31210 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:ea9eaad310b7a1eb6e71a04d999fff99df034c4e6e3cab0143fd27bfe4b485ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72324825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6321a175cb81ff121817f97d578326ba1fd54ea787a0beaa2cb91695fc662418`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:21:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:21:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:21:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:21:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:21:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:42:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_VERSION=8.3.13
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 04 Oct 2024 13:25:53 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Oct 2024 13:25:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Oct 2024 13:25:53 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Fri, 04 Oct 2024 13:25:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["php" "-a"]
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 04 Oct 2024 13:25:53 GMT
ENV COMPOSER_VERSION=2.8.1
# Fri, 04 Oct 2024 13:25:53 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 04 Oct 2024 13:25:53 GMT
WORKDIR /app
# Fri, 04 Oct 2024 13:25:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 13:25:53 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9208ede8519d248128a660ad6cbef1b3a33b141374be176c946b5b17b2968ab4`  
		Last Modified: Sat, 07 Sep 2024 00:42:38 GMT  
		Size: 3.5 MB (3473993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabbdadb2babb53e22b8c60bffa37b66bacdd1495093eec38748ca15dabc8287`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2431f4d7c348124f66281fa6433fdcded6e6a093aedb9cdd6fa9c7d87a1407`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8632e206b7bc36b0bfe226c5ec5e94154bc411b3677a2903f0f33e8b4d06d3`  
		Last Modified: Fri, 25 Oct 2024 02:46:23 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950b6d1374ddd91229978b32c87237f1a304df6908d46a3e6c6617379120ecb`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fac98b72a50f285d80ad08584ff62de41c8b0ea0276e5187d77f6dddb0430e4`  
		Last Modified: Fri, 25 Oct 2024 02:46:25 GMT  
		Size: 20.4 MB (20422987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17a61d0d2aae412d208b48c74e3754c9fc7b3f3d0644186eb5a952c01d1d01a`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c55de606062f9878f968213cb2af563401f158dbc5f7b5612b565d5f23a8d8`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a65e35183739b8872e800265ad579948004dd6060f487f2295911c401548795`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 31.3 MB (31338414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c5278f124e717ca16fc2677a7e92e4331ffd330679687f8429c052a4980ca6`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac84ea67d37f2f607682a88ba709d3ca1d7ec45ffa78bf119c0d99f10f2b8d`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 1.1 MB (1098760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a848938d0078bf52df4fa2a8e8aa39affeeeda8eec7e20a5223789502a279b3c`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720a49fb844cd885e2f5780d44f0f9463fa2ebf0019ec117c14b3db14a6df2d3`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:25870622ae7e5ca41223a45c6b4697934b29ca8accf161069a09ea9ce2462cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b49fa50dd59377e3482258ce9585d6abc69ea39fb8ffb16cf1bdc4844fd8505`

```dockerfile
```

-	Layers:
	-	`sha256:33f7b202cdb48083456840312ed4b34234ccd718584600e47a3ae6e88fda4091`  
		Last Modified: Fri, 25 Oct 2024 06:41:08 GMT  
		Size: 2.1 MB (2145739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d35b36e0e9d0af4df173a651dd2132192a1fac59fa923225d506c76e3c067`  
		Last Modified: Fri, 25 Oct 2024 06:41:07 GMT  
		Size: 31.2 KB (31168 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:lts`

```console
$ docker pull composer@sha256:46531d95ae84b4d0f44b109d365db86fca10d96d1cfb68999d9541426d89a43e
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
$ docker pull composer@sha256:1b8c7b7803441706a9e04bcb7c23d6c7d5935a6d27d7ab797183700fc4d3cda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71258353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d94b12f6cbd009a3fc780b7b1aa509b42f3a678572dc657b92d63c98ca8db49`
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:41457434eddc5cb99259de159d6a2dad43029452b1ab35975a3209703b9897f4`  
		Last Modified: Fri, 25 Oct 2024 02:16:38 GMT  
		Size: 12.5 MB (12504689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328056f851cc57837c30c7c30c8c1fba0e538db1bdb0f520508b064b7771388b`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66dabf5a41275ff903a5f9ccc8ba9ba981ff4f80da78ac30a649f683542b98c`  
		Last Modified: Fri, 25 Oct 2024 02:16:40 GMT  
		Size: 20.5 MB (20518417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab768f68c87e7a556fcaf812a92acd5c8bf122cc606c956394a6ec4bc208f0f1`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b263e76cc797a1f79fdee350bf8047c4fae8cea974168046c693eec0894545`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8e721d4ec60c167e217985a6634def0773d7c209c854c6cff384ae95d609e0`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 30.4 MB (30368247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482b3b3d18b4f075b12c4319e5dc322215e9ac691e238f09bbf7858afdc525cd`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9323b09d4891470d8d5dbad780102f127ee113898ab714b3cea5a8e051ef7ab5`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 935.9 KB (935910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ede80ac42873d95db4f1e1dc746ab53be2071011ecc8e0df9a2a05d6ff83f0`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9ebd623a6cd55899fbfa1cdbd8ed0b505385fc70414307c27b06e6306c2a50`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:85d2f659fdf26193b06cb76d853c0d73e75ba826c2b5b3d9e44f53aa15da98b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb3aef60fab8f0110068b8032e3b12e726d2978eb062c434b806dcbd8e0fb84`

```dockerfile
```

-	Layers:
	-	`sha256:b704440e485eec60929d9914b7388f77adb483eebc2626931665c90c8ea22b89`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 2.1 MB (2147494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f51685b55e387f4a3da1dc24d977b000fb70421efa45bf9f76f43d84f9c86bb`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 30.9 KB (30861 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v6

```console
$ docker pull composer@sha256:30730658678c13b3fa13492b42fff3265b536c0a21aaa129acc0865633af891b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67981937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa096441dfd2778abfc7be3ff0a8e578eed66f710e8b6b8c94e3812a9c7c87b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78c7a9de9941e89cd785fc3ad14f52410d858d2259f5c9b2a852fd144612520`  
		Last Modified: Sat, 07 Sep 2024 00:48:55 GMT  
		Size: 3.3 MB (3269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbf8fddbe2a872480c609959838de42e95d1f5d5d3d8daadf7a1e44e5c381a2`  
		Last Modified: Sat, 07 Sep 2024 00:48:54 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d88511b2a3086248129999917d9f1e5928426fda8f08edf40ab5bafa37a9`  
		Last Modified: Sat, 07 Sep 2024 00:48:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2913caf4eeb0b47e0a269d5500be80ad644b55b830987923b9b25d7c47b779b6`  
		Last Modified: Fri, 25 Oct 2024 01:12:37 GMT  
		Size: 12.5 MB (12504684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd40e2319cfc199b8ddae2c1022299e653810d5c8fcff021ecf9e71bc732119`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8662dfadda858bf306da862403b12c0ebf0c2c06e8cc29019a10cec84a7ec93`  
		Last Modified: Fri, 25 Oct 2024 01:12:41 GMT  
		Size: 18.7 MB (18711875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0edc47bdf53f26bf4da16fdc4eec8b087534150b52237c0f603b8e571890a9`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43053646b918ed9c5822c17ca4869f057851bb96fcaabed794a5a7ec36dba34`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92515b32642bf33db09f5042274a35b3bf9dfd52f33a78bed3ddb0efab90867`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 29.2 MB (29169219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cececc96a315d5d1a226bb3d06189757c3df3f0bf808c3089f6a8c1ee57b169`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c2e6b61270c266b53490ff499b93ef054fbec927512a281cc7a6b24701805`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 935.5 KB (935497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff00edb04cb0f9ff5be423ef9e64b2cc05ec099877d249544ab29d1038f5de3d`  
		Last Modified: Fri, 30 Aug 2024 21:19:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c6ab539bccdbdb0fcf7fafd68ce2bd97284eab5f8d8abf785cabec35588b7b`  
		Last Modified: Fri, 25 Oct 2024 02:09:53 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:e4a9826fe50da350c6777297621c260458faba92b526041a376ce79aab8b81b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57b36f19d8ad3b6a6132c9b81dbfc98306a2cd534a3294c6f488017985d24eb`

```dockerfile
```

-	Layers:
	-	`sha256:37078fd6622f6a210d26c2f3f60d602e03823611193b605e55caca850fea26d2`  
		Last Modified: Fri, 25 Oct 2024 02:09:51 GMT  
		Size: 30.7 KB (30734 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v7

```console
$ docker pull composer@sha256:c91cd5ffa3dbabd16ca1a5236effe469f34a169c118f5e08a70364c4028ba35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65895087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5708873007b11d781ab952dd94413afc61e3fb305d253bd5f588a1aa1c3b233`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12c01d5f758f7fce28807153dec7a85ae2e307cf0d73f644d575cd875cb994a`  
		Last Modified: Fri, 06 Sep 2024 23:45:25 GMT  
		Size: 3.1 MB (3079568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c3e48f803b4ca0c1ec0b16f85f80f0a17b054845918112eb73b80eb9bd7297`  
		Last Modified: Fri, 06 Sep 2024 23:45:23 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7c21bdd57d9b7548f08c79a56f0a75d4e14a705967ae55d0450a10f0c6c43e`  
		Last Modified: Fri, 06 Sep 2024 23:45:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efe62db4f1f9f85f795e6cc1e7f8d835b0a8657d2a60143ba15d82d5863841`  
		Last Modified: Fri, 25 Oct 2024 02:37:26 GMT  
		Size: 12.5 MB (12504680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204359c9c9eb5cb76578981a5c068e3fac227ce0e7df1a86096569dc1230c85`  
		Last Modified: Fri, 25 Oct 2024 02:37:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2762620a9d567bff0020a3cda73a630f1a993bda6921efbd9554d75c9fd3377f`  
		Last Modified: Fri, 25 Oct 2024 02:37:28 GMT  
		Size: 17.5 MB (17478737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5a9688a15e4908bcd1ed18d76acd39f8678dd66decafbae483b2c884bf1c02`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66727798fd727eda6cfc82ff904b3773b442a67ae9e11967aac36d92e2e9be32`  
		Last Modified: Fri, 25 Oct 2024 02:37:24 GMT  
		Size: 19.5 KB (19519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ef898d316952fe64642bc94179ed2cc82e7c9404af0c91e8d0f5152097b5e8`  
		Last Modified: Fri, 25 Oct 2024 02:49:33 GMT  
		Size: 28.8 MB (28797969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48238d159943a0389cdf60849c19e218b8aeae434d69dfb9050fc0c71115bf9a`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac4b3d7e0e3d6c59f9af60415c3648615e5a2c56d6abd230155f2bb2576aee4`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 914.2 KB (914234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2f49471a8a3f6b47253e4796bc3559f6c7b389ce4b004d70ab0c04c933454`  
		Last Modified: Fri, 25 Oct 2024 02:49:32 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d42470aa4461eb263340b714cf91223e64989da0efd82729652db07eec42cc`  
		Last Modified: Fri, 25 Oct 2024 02:49:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:78e4ea723042b217fb38f38c02ed1c4383b09141d7f0a2696ee5b72187989bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61c1b78d61c0e364b21a45b2caaf961a9f800a8657f779ca621199534929719`

```dockerfile
```

-	Layers:
	-	`sha256:8ded441250b18ed96be4decb09068cbebb97cc0c5b5a78a72c2398c31f6e2b31`  
		Last Modified: Fri, 25 Oct 2024 02:49:31 GMT  
		Size: 2.1 MB (2147807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f242ffe1dc15e1632f169cb0fdb9c52eff4f1cfa160aa2efe395c83193b8ea`  
		Last Modified: Fri, 25 Oct 2024 02:49:30 GMT  
		Size: 30.9 KB (30949 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:b4735380fef3b40db741edcda06590075faaf8ce6788f71900223d5ee9681954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72716362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9f0e692053a7b858d9e4e322e492896e71d19567dc746f0c59e0ff768d0c67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ef8ad75958cd7eb0e453d0f85e72134ef3976f8351b5742370df35bc60ed42`  
		Last Modified: Sat, 07 Sep 2024 02:23:50 GMT  
		Size: 3.3 MB (3333388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f80c1299f6c626e7df88761199f03734cced725870be7a04dd95bf11e80104`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb3615e2ca5466e128fbfbd9bfcaa4cc0a7c5935f1d980f13d765c6bfde9144`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b324dba8535eea2357b994da9864afef849388a4c8e80235090810383253f31`  
		Last Modified: Fri, 25 Oct 2024 02:19:36 GMT  
		Size: 12.5 MB (12504686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e479347c3f32eee03df523edd0f1a869f7a7636702922f9d5db1ac9024ea211`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6b8889455c447cc20eb2d9881a51c22cdac63cc440a2e647d8e5c2c7f13cfc`  
		Last Modified: Fri, 25 Oct 2024 02:19:37 GMT  
		Size: 20.9 MB (20940181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eeecc80b8f4736452eb3054bbf21ee480f6a4eb724b114b31cb94ab034f53c`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93069ffa1c1f8ac20ef6e8c62fa71d5ba3e5ae3f4ce6b97965ae1a5a0f2562bb`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98eea5daa433de13908b8daf3e98a58f41b648a198629693556299898d3050f`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 30.9 MB (30879665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24933c1ee11a72c73a8c1d127f5254b2e1a343115700bfd5d40922a70347acac`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557a745b32b20029beab65e3acdc0450cd4f061eb272e090e823072c4b8b8277`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 946.4 KB (946416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fbb3c72980ba7988a2db7b9613cdb24de6cd53d9f1c55a9bf587fa83e91bbf`  
		Last Modified: Fri, 25 Oct 2024 04:22:35 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763a639df17e35391453ee7f589bafca0c377a16c7d0732f158ee93511e5f769`  
		Last Modified: Fri, 25 Oct 2024 04:22:36 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:caf94f6b789abd452f00a7c66c15651306dd21f55bbfbf41e9de10d2b6a43b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771e5d72f8d7aa1932d6904471851b84f38a74209160af344871cbe9a301a80d`

```dockerfile
```

-	Layers:
	-	`sha256:cd6c902d764be73511e42400a26661ea999092ccabef1d81e121b13769456d85`  
		Last Modified: Fri, 25 Oct 2024 04:22:33 GMT  
		Size: 2.1 MB (2147633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1effed70f7bcdf54c50bdaa8c95188f65bdc7c9791e0022cf05680e79ce5e10e`  
		Last Modified: Fri, 25 Oct 2024 04:22:33 GMT  
		Size: 31.0 KB (30977 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; 386

```console
$ docker pull composer@sha256:e33d8a8adc22b99db3cbddf647ea3ba3832f8c5d1d58bb90e42596ef8c94ad74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52353571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f2a1e5ee2c294d7c24728d23e74e9df91cf6999fa2a05097d4595fc8a11b68`
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:9eaf7c1d9791c6b12392f1f767948304f2c2e69cb0878ecec4d5df2be5af4dca`  
		Last Modified: Fri, 25 Oct 2024 04:22:20 GMT  
		Size: 12.5 MB (12504687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0bab9c844ca004a8fd6a7ea2a92c041012b047b66151b6d55f81e1e29009e`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609f4e456e59a3c94a5761b23648a66de98737427aa781c0b05b3296eacbef62`  
		Last Modified: Fri, 25 Oct 2024 04:22:23 GMT  
		Size: 20.8 MB (20818182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4455a0ae1ac0aca52a62943181a6673cf4e49459913cfea722ceb78acf98f28`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f23e94c0f2162ee0e26724220289d3609acb53f3117201cba2c8e6e5021efa`  
		Last Modified: Fri, 25 Oct 2024 04:22:18 GMT  
		Size: 19.7 KB (19716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0d35444bc5e8c85dfb6fca26a91f8f71cbdaf010077d220932f53bc33453a`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 11.3 MB (11281319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbd8ee9662704273444a11a2628a08c55058235539da3ea7e96f3be43027311`  
		Last Modified: Fri, 25 Oct 2024 04:49:54 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd495a69bd985f7c58cbdc3bfb7fb84be69f050722b1426bfc91550c4ed7b967`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 923.7 KB (923654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffd79d5011bba75faf5b0334876e22a52625a56727cc43ceed2de7674d04399`  
		Last Modified: Fri, 25 Oct 2024 04:49:53 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba53d57ff746cd2ddd87d6ced854a49c95ff92a78a41be2558d7a03fc458d45`  
		Last Modified: Fri, 25 Oct 2024 04:49:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:d503fa86a799da1a63e5ae8d28399ca6a0ff53d7c048f122664c7a3034c23420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.0 KB (452000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498f99d0fa1404bc185ba6674ca97861f0b724fe4a9d7f7f6f1ee3f18f329288`

```dockerfile
```

-	Layers:
	-	`sha256:05d26777b19bcefc825c58a638d76199a5f0c83020a0ecfcaa3e6bfb0dfb20f2`  
		Last Modified: Fri, 25 Oct 2024 04:49:52 GMT  
		Size: 421.2 KB (421168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6637a35e080632eed43344b1ae9739a1bfa92b13c73c5c1de56f4a96bb8d3dc4`  
		Last Modified: Fri, 25 Oct 2024 04:49:52 GMT  
		Size: 30.8 KB (30832 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; ppc64le

```console
$ docker pull composer@sha256:bb8414850435f77da1b614134245f5011e7056e4701a30ad8eadc93c5746ea88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73154547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e6e2487a5d491f3ab1e6ae7f9df85aab9b33def2334634655955afa8bd2544`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac727a268c34206d27f9588c3acfc276afdaf0623dfdc19b7d210a7a881ee4`  
		Last Modified: Sat, 07 Sep 2024 01:44:58 GMT  
		Size: 3.4 MB (3408322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564dcd8f1c226aa29a92bf07685b2a44ccb8ac47267a590bc34a56d25bbbcc4`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3867a87b0703f924c2a7915ce891a49d11c61af6d01613564e485431a9f78`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8622608d41f825e14aa5bd26799c3251549bceef128cf2eae2f52f1ab78913e`  
		Last Modified: Fri, 25 Oct 2024 00:57:34 GMT  
		Size: 12.5 MB (12504690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b9b2cc7fa22223c46604afd8fd56f225e535ca1e7d006d545233f411a4a3c0`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9400d92782aead1169d2e61549cc961ef18b1a2f1468fe9a486ae165d901cf6b`  
		Last Modified: Fri, 25 Oct 2024 00:57:37 GMT  
		Size: 21.3 MB (21285751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ccc474f40266b6e9c07bd2bd8edf9b2feccdf7986579f0a7bfa017cb90929`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd3a52d6da309a1907e5c8310c6411753ee8823a82029f55b265da24bb7566d`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b86ce86d7510dbd92b9dd787d737ff21b3ba726f05cb8546ccc581875d372d`  
		Last Modified: Fri, 25 Oct 2024 03:09:39 GMT  
		Size: 31.4 MB (31402604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74408fea44fbe8cb944832b386c9752e053e23539d049cfad4f03cac46f658f4`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd275ee85ecbdd427da2151dde955458d6d1a75fde608151c2b458a299b5391`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 956.4 KB (956388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bcb717846c44afd18a6d65ecdb638100cda39ee224ab008e8ded724a526776`  
		Last Modified: Fri, 25 Oct 2024 03:09:38 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7923799a776ec1502c18e4dd0b30afce84fb4ee98781a0ae21133ff02f527fea`  
		Last Modified: Fri, 25 Oct 2024 03:09:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:6c2cfe0bf3738dc08b980f54b00584a8aa061bd4b0c109dd7251fb983b0bb7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badc90556f39fbf10a2dc27c3b81c4f9243f8d46c8acc221ee4c6065b29a8020`

```dockerfile
```

-	Layers:
	-	`sha256:1e9a706865fea7597dadf4e06cddf10f4b67c21ee03790d8fe9f2e67ad69caee`  
		Last Modified: Fri, 25 Oct 2024 03:09:37 GMT  
		Size: 2.1 MB (2146043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbdd29b7434ab64926ee6535422d4b73de69aa7d5e5a2965da2d7037207cf3c4`  
		Last Modified: Fri, 25 Oct 2024 03:09:36 GMT  
		Size: 30.9 KB (30895 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; riscv64

```console
$ docker pull composer@sha256:1483db658441f9702ced09239b2970ade1f86231ff6df798df9986c760d535a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70847593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20f8993a43ef737a0eacb62c27cc4583c5be4796f1ea8178efc3044f496123d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160a71fe2c21fa0be03f4ecb3856d46307a8cab34f0749e89c452111c128a28e`  
		Last Modified: Sat, 07 Sep 2024 09:00:45 GMT  
		Size: 3.4 MB (3405216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99de0cdf41fffa764363801fb8a9efbd008b3689317846613f74f55be82ad4ec`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4878284381f1e57d12b980a3d3f2476a10fab26827866948f61cc0a2214a8`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d60d72a55a97ca66240c87e7bc1886bc5aa87d97579097a6d9bab88a75ae1d`  
		Last Modified: Fri, 25 Oct 2024 06:19:30 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55404ef143ec5be664bfb8b7d19253fad3452d91340eac96ad5cb7f88c34e9e`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f1fc6d05b292475d5cdd272dff683e4226cec9930f2394a99a2af5ad9a19c`  
		Last Modified: Fri, 25 Oct 2024 06:19:45 GMT  
		Size: 19.8 MB (19785919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f47a3a529d11fa207f1e96b631df8f8334701948d58152ac5419e07ef6f0b09`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5729eb71e7d125b843a7ed55653966533b980fcc3e19e4ee54ce1e25042a67`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d654c394fa744c0d5afc76db22431671980aa34529d74f487cfbb8e0857966`  
		Last Modified: Fri, 25 Oct 2024 09:50:35 GMT  
		Size: 30.8 MB (30811074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a58738e9c21fa9035cc24b974c8d99fbd269320abe6e366312beca87fb36e14`  
		Last Modified: Fri, 25 Oct 2024 09:50:31 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8406617ce7b268f103442ebf9014ebb6d00d67423a00e8d4cc0fe8a3c2083043`  
		Last Modified: Fri, 25 Oct 2024 09:50:32 GMT  
		Size: 944.8 KB (944841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c543e1043c470ffc9bca0c243d676542df337e9a6e996c135ad2f78f672a4f0`  
		Last Modified: Fri, 25 Oct 2024 09:50:32 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7958c4da0e040043bad20bd8b15e89de25894621fb219fe83ac2fbf159452a5`  
		Last Modified: Fri, 25 Oct 2024 09:50:11 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:cfac385a69656c4bc61b504be55a26c78db57b8a604070bdfdc12dbbb3216fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76326f6043366dcee1d6cc4fb363dd045fd8c7b58baac7f73c132391c8b9ed46`

```dockerfile
```

-	Layers:
	-	`sha256:4857c7dcee21584b869465928007f9d02e7c629a554194f63fb75289d564a923`  
		Last Modified: Fri, 25 Oct 2024 09:50:29 GMT  
		Size: 2.1 MB (2145659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c6439a91f43d65978003cc2cd63ebe853980f94c8ba18b14b132d7692d373de`  
		Last Modified: Fri, 25 Oct 2024 09:50:29 GMT  
		Size: 30.9 KB (30897 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; s390x

```console
$ docker pull composer@sha256:ac8d71b74fc72077507d30cc50805203012d3d431189328ab346bec2a2c69362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72180557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38237ef2ad42e4abd9fec2cef110dda5ba4d73331f1b4ffe5989ec1a91627f09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 09:31:03 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
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
ENV PHP_VERSION=8.3.13
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 20 Jun 2024 09:31:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9208ede8519d248128a660ad6cbef1b3a33b141374be176c946b5b17b2968ab4`  
		Last Modified: Sat, 07 Sep 2024 00:42:38 GMT  
		Size: 3.5 MB (3473993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabbdadb2babb53e22b8c60bffa37b66bacdd1495093eec38748ca15dabc8287`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2431f4d7c348124f66281fa6433fdcded6e6a093aedb9cdd6fa9c7d87a1407`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8632e206b7bc36b0bfe226c5ec5e94154bc411b3677a2903f0f33e8b4d06d3`  
		Last Modified: Fri, 25 Oct 2024 02:46:23 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950b6d1374ddd91229978b32c87237f1a304df6908d46a3e6c6617379120ecb`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fac98b72a50f285d80ad08584ff62de41c8b0ea0276e5187d77f6dddb0430e4`  
		Last Modified: Fri, 25 Oct 2024 02:46:25 GMT  
		Size: 20.4 MB (20422987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17a61d0d2aae412d208b48c74e3754c9fc7b3f3d0644186eb5a952c01d1d01a`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c55de606062f9878f968213cb2af563401f158dbc5f7b5612b565d5f23a8d8`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a65e35183739b8872e800265ad579948004dd6060f487f2295911c401548795`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 31.3 MB (31338414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c5278f124e717ca16fc2677a7e92e4331ffd330679687f8429c052a4980ca6`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbe0019b55069a840ff7d33ab47aa1388698ccd7de55346481fc06538f96bab`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 954.5 KB (954493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942823da0620c6a8685cd25196843521489eac657adec4d60aadc71e5877dff`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe38bd91f2e8ddf38dbbc935628e7eca7377274d3b0e557d7c2bae841103d3e3`  
		Last Modified: Fri, 25 Oct 2024 06:34:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:4a9995428838589af3cc454155789495893d62697a3752bd1afcf4d372428992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7b257062667dfefc37406d94da1c369836eff05846dc1bda28c0090bf6aac4`

```dockerfile
```

-	Layers:
	-	`sha256:b1c9fb6718635125713745a5dcd123fe5ab6937f08ab19273a2f2e76b28f1039`  
		Last Modified: Fri, 25 Oct 2024 06:34:15 GMT  
		Size: 2.1 MB (2145445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b72977063c3707f9c3b52de3dcb56482332296630c5a3b914ba5d277f3074027`  
		Last Modified: Fri, 25 Oct 2024 06:34:15 GMT  
		Size: 30.9 KB (30861 bytes)  
		MIME: application/vnd.in-toto+json
