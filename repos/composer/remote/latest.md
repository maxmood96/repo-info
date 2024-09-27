## `composer:latest`

```console
$ docker pull composer@sha256:5205aab12996c90fa90ec68322160fa81fbbc59b9a1b9a90feb87f2b077410cf
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
$ docker pull composer@sha256:57d668f89bfb97187cad9a4f2a9df5a24b64d79f8202d414e8340549d009bd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68443228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e401e0c0405c7d5c7f7534e3665c525af54dd830fe8a0c25114527af98cfb33a`
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
ENV PHP_VERSION=8.3.12
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.12.tar.xz.asc
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_SHA256=f774e28633e26fc8c5197f4dae58ec9e3ff87d1b4311cbc61ab05a7ad24bd131
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
	-	`sha256:e567f6a279d6230e9f2dfe3ce224ced757f36a350ad19c01a56514c379d9b40c`  
		Last Modified: Fri, 27 Sep 2024 01:02:21 GMT  
		Size: 12.5 MB (12514554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c15fd3b41bdfc8b5af169f77fdd27b0b15cf69afe4e260f650cca4d3c80600`  
		Last Modified: Fri, 27 Sep 2024 01:02:19 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eea53e5dd457c24459f7202e5d629033c0951eb5add7b1e823d763add96b0c8`  
		Last Modified: Fri, 27 Sep 2024 01:02:22 GMT  
		Size: 17.7 MB (17680084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417f9a398261bed58b52188f04ac3f78079c718c4acf213cb149f192c6b4a190`  
		Last Modified: Fri, 27 Sep 2024 01:02:20 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca23a67aef6035b25a1778f5468293e5e07824ff2b9a8a23469cc3f592865840`  
		Last Modified: Fri, 27 Sep 2024 01:02:19 GMT  
		Size: 19.7 KB (19710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a82bcfd91ef6eeff60a57b11a3775a64f0d82fe8edc99e837aed75bad95a67`  
		Last Modified: Fri, 27 Sep 2024 01:51:47 GMT  
		Size: 30.4 MB (30367660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fb93cef93c9ab5437aeda3f8fcef35cb533fcb206c01c3a7335742cba10cb3`  
		Last Modified: Fri, 27 Sep 2024 01:51:45 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb53576217843bdad720d57152037c8144d06173bb0053f4e76a87c87d5dad09`  
		Last Modified: Fri, 27 Sep 2024 01:51:46 GMT  
		Size: 949.9 KB (949855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a73dcee5a8d5154575cf0a309c5a94868ab3b9bfdf74f36c5ba41a287da166`  
		Last Modified: Fri, 27 Sep 2024 01:51:45 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e125b08fbbe2862aa375c7a8629bed2a81f9ca9a54b0a878f8976712596abac4`  
		Last Modified: Fri, 27 Sep 2024 01:51:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:b792c725a143b8025e9ab998da3462dc1432337ccf0c27352c55b70ea40fb400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29f4c6dd28b0c4fe0b4d012496220c4cf1186d520fbd1099e81ab7a2f8a9471`

```dockerfile
```

-	Layers:
	-	`sha256:3189dbc296d30ce1a459dccbf88a790fc2d5772e7066c219b5688b731b19baa6`  
		Last Modified: Fri, 27 Sep 2024 01:51:45 GMT  
		Size: 2.1 MB (2147479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f36729db6963f2aa8223e112c962d018390840f829278fb3e95f83dbd3f0d6`  
		Last Modified: Fri, 27 Sep 2024 01:51:45 GMT  
		Size: 31.1 KB (31131 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:82bfb7e55096bc2ba98a6fec4964e41e81e4bf9b824b3389b6c9c462ae94453d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65483877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27309fabb9a6c316d360d53397155c71c7e06b87bec777b61afd1e6005eb852e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Sep 2024 08:44:06 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
ENV PHP_VERSION=8.3.12
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.12.tar.xz.asc
# Thu, 05 Sep 2024 08:44:06 GMT
ENV PHP_SHA256=f774e28633e26fc8c5197f4dae58ec9e3ff87d1b4311cbc61ab05a7ad24bd131
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
	-	`sha256:d7c4dc0857754cd2c564ef877edf4f66552abba13bbc570b80171aece21a862f`  
		Last Modified: Thu, 26 Sep 2024 23:20:45 GMT  
		Size: 12.5 MB (12514551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a7ba510e7175895c0b057be30068d36d087a85fa6eb5eec0a2e209c46949f7`  
		Last Modified: Thu, 26 Sep 2024 23:20:43 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319194738769a0ae6189f29964cf24e039b800d3009154086d4c6f24098fb6c1`  
		Last Modified: Thu, 26 Sep 2024 23:20:48 GMT  
		Size: 16.2 MB (16190614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d4f39b98b9a5cd503b003a6856876ea548c8bc153993635dd05a272e05c68b`  
		Last Modified: Thu, 26 Sep 2024 23:20:43 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8730d6d8d90653a28887d010e600c8bb57b59bb43e314f492237f2b92a9bac6`  
		Last Modified: Thu, 26 Sep 2024 23:20:43 GMT  
		Size: 19.5 KB (19494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b9782d09edec854abec71d3075daf825c8809450f829a7bbc36fffa7ab488d`  
		Last Modified: Fri, 27 Sep 2024 00:38:50 GMT  
		Size: 29.2 MB (29169260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1359daf7572c248a07cfcc966c2232e8b8299094933e85fe2fa8e02837b258ec`  
		Last Modified: Fri, 27 Sep 2024 00:38:49 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e404d92fe5cba2d5d785c4ef0761c338acfb2f35506ec629df090ea521dcad`  
		Last Modified: Fri, 27 Sep 2024 00:40:46 GMT  
		Size: 948.8 KB (948802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12ece5c7e8ab6982a7044cbac04f6e5410efdba180cf3f82d3664a6a5b17b46`  
		Last Modified: Thu, 05 Sep 2024 22:03:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebb664920def107ca09e5dfc2abd9f659f085e0d4411f5bb5dd186b8e4e4e3d`  
		Last Modified: Fri, 27 Sep 2024 00:40:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:cd7214dff8aa4a26288167357387d2053495573aad6acc4a2a7ff09e678e85c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790b57dd7eb492a98e049d836147329780af91676fcfb3b1cf01b3bb8ccba417`

```dockerfile
```

-	Layers:
	-	`sha256:66dea08be6481c9d2afb101eb189063f2dc17bf7563a07daf618ae743dcb0bef`  
		Last Modified: Fri, 27 Sep 2024 00:40:45 GMT  
		Size: 31.0 KB (31008 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:cc9c13285874e83836bb386dced648db899ae8b6642bf2af5eb99c69f12e7951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63427368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4105f185e3b55eab37c0f65625afe961ce2a73fb06dff9aa07c6cb10a139b0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Sep 2024 08:44:06 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
	-	`sha256:b707cba0501c723b1d166e95765dd8eb1aa35cea083ec1dac51f6560f0c8603b`  
		Last Modified: Fri, 06 Sep 2024 23:47:19 GMT  
		Size: 12.5 MB (12502093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a5db13d53ae8bdf446dcf46090f6b372e98a996df5c81f693ebeb399a13be7`  
		Last Modified: Fri, 06 Sep 2024 23:47:19 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164c27d0aa58b3a9174687599926129a6eea4cb5f8f618b52107bca9cd2323ff`  
		Last Modified: Fri, 06 Sep 2024 23:47:21 GMT  
		Size: 14.7 MB (14712133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621fced4d7d689429b3cc545ce5164837f0120dbdc186b0a0d008067e01f856b`  
		Last Modified: Fri, 06 Sep 2024 23:47:19 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ace985d7b160f40bcda5b385580cbd72a8c99c1972342477a29d15b039e1e3`  
		Last Modified: Fri, 06 Sep 2024 23:47:19 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbb8003641201be45a6224b5b2ef30f22847aa74c4ac6c285c28f0f4e10f932`  
		Last Modified: Sat, 07 Sep 2024 13:19:25 GMT  
		Size: 29.1 MB (29074017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046847f27b66563c5152f3dd5e1ec4d519f696f9e23de9be60370160a3e11d26`  
		Last Modified: Sat, 07 Sep 2024 13:19:24 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a2b4f001a0d6941f45368aa9a20350084f760f58b7af80c1bee43742e8179e`  
		Last Modified: Sat, 07 Sep 2024 13:20:57 GMT  
		Size: 939.7 KB (939686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1510fd3cef8a5cf2b47f02b92dffb98617f20563af9c0a5e391a77ddebe32c`  
		Last Modified: Sat, 07 Sep 2024 13:20:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8949c1032f0413a79d37dd4e213f94443f4bcc6d3339c3028dc15257c5795e`  
		Last Modified: Sat, 07 Sep 2024 13:20:57 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:5a7c51afe004b550ccd9d3c09df119eb6d105bd30cd44542951f666edb016fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a11314a5de3780e216bae303a729acb5a0e5ededefe7af2658734336d4e280`

```dockerfile
```

-	Layers:
	-	`sha256:44e53ff8b9b79f762f7ea5b93dedf34d09baeeb07a0f117da6f9ac4c31148f61`  
		Last Modified: Sat, 07 Sep 2024 13:20:57 GMT  
		Size: 2.1 MB (2147787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229e29e905b7339185283cd921bab9666239485f9c91097f865c1289c34571c3`  
		Last Modified: Sat, 07 Sep 2024 13:20:56 GMT  
		Size: 31.2 KB (31227 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:0a841f93d6b8c6ec6ad1025aeecfd5d5db4ecff217e5bcd807d6155c4019bdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69258539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1094bea0be70d84c03b245a06b8123549e0d3aaec22f2fa9e73f1bd32dd53af7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Sep 2024 08:44:06 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:a50ccf490cfb7487f9a2e9dfbee2a390ac1f98fe3e133c196b70e25ad38f1076`  
		Last Modified: Sat, 07 Sep 2024 02:25:21 GMT  
		Size: 12.5 MB (12502094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6371e4db634122b2be8513e59ae0ec8d172a1bf76a9e9bdfd0a9f89c3f81a50f`  
		Last Modified: Sat, 07 Sep 2024 02:25:20 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ca192fefdde723ae56f378651d8fe0aa6c79be187cc3428c87acc6bfbbe20e`  
		Last Modified: Sat, 07 Sep 2024 02:25:22 GMT  
		Size: 17.2 MB (17197116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e357b0a92f547d86d409a0f71105010a8fe9350f2542621c36a521f76e2851`  
		Last Modified: Sat, 07 Sep 2024 02:25:20 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e06eedb66fe527de3b15d9808c9e4bbea74e056c2f7013dade06a5d117fce3c`  
		Last Modified: Sat, 07 Sep 2024 02:25:20 GMT  
		Size: 19.5 KB (19485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feda614d660266ce277aac9be6b02146ed995d7d5baab2a2ec4c6f984289de37`  
		Last Modified: Sat, 07 Sep 2024 12:25:56 GMT  
		Size: 31.2 MB (31163162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a5d9d702adb21caaadea2d9a010b2870d46bb964923ba56d2c0f2d7c64a22f`  
		Last Modified: Sat, 07 Sep 2024 12:25:56 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2be4128333b505e55d46e21257836b180acf0fca538691e54fcaefcb41e139`  
		Last Modified: Sat, 07 Sep 2024 12:27:15 GMT  
		Size: 950.8 KB (950771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef4fcbf3f70bf3b47ed26b4fe2be3d6f64b1783fee1c67c4b066f807e2d37dc`  
		Last Modified: Sat, 07 Sep 2024 12:27:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621ab9467e1b5ff14ba19f7c8b648087de1f1a59749a853b3aeb06eef7027477`  
		Last Modified: Sat, 07 Sep 2024 12:27:15 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:9ec613d31d792725bd209ecd99c59b809fac8dec05a6d5d85903f1e38ec5a034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2179049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc68dc12bfc1679b309c0cce16e47c18dd70e35cd36bb0eb01854b894cc1c58`

```dockerfile
```

-	Layers:
	-	`sha256:ee4486f74f0d77ab03dc40aa23dab086756a73d2b2c427d20ab7db0abf98328e`  
		Last Modified: Sat, 07 Sep 2024 12:27:15 GMT  
		Size: 2.1 MB (2147617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d19be80bd1437bf684df517f333ee44e2c7e72a8af36776f4ae6df7b87a5eb76`  
		Last Modified: Sat, 07 Sep 2024 12:27:14 GMT  
		Size: 31.4 KB (31432 bytes)  
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
$ docker pull composer@sha256:bb242c21d2a5c3e8c3a4f883455c4b13b4e9af1cf1fabbd63a09971d531b390f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70232109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad533b9929c6f631438a3b905ecb1aa8a42e84b66465c4e22925f0a8f9ce0ec5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Sep 2024 08:44:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:30fae27c36debbf04d9fdea54c48a8f31f1814d6b1b2c73fb1a53c48f93aebe6`  
		Last Modified: Sat, 07 Sep 2024 01:49:49 GMT  
		Size: 12.5 MB (12502098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f628678ba4099c144c70d74aac27a734b115995ccc4c3dcf0628185560fdb868`  
		Last Modified: Sat, 07 Sep 2024 01:49:48 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f074974ba46fe1d74401d8f38f2f6276d50a721ed113fe440a9b0379d3065624`  
		Last Modified: Sat, 07 Sep 2024 01:49:51 GMT  
		Size: 18.1 MB (18089786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efba8b066ac24f382591c416cb6a61a33ac7a11c8118d14f248782e4f99ee6de`  
		Last Modified: Sat, 07 Sep 2024 01:49:48 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0720370106824d4cd02c163080fab24fdb637de6f330d37101da27e8b9fa05`  
		Last Modified: Sat, 07 Sep 2024 01:49:48 GMT  
		Size: 19.5 KB (19483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f701e6623f9794fc7a962dded2889a9dee18ae28a715d18c421db6f85119ad9`  
		Last Modified: Sat, 07 Sep 2024 12:09:58 GMT  
		Size: 31.7 MB (31678426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0213279186a9a5b91313b73664094a4827beb2eab147b1ea3d9015c28220b9`  
		Last Modified: Sat, 07 Sep 2024 12:09:57 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51210b96e9a316305d8b6b65f0ec8525a250bded00311e723fab1a54b3b159ce`  
		Last Modified: Sat, 07 Sep 2024 12:11:48 GMT  
		Size: 956.7 KB (956699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534cd8b05f8b415745bcfd35d0fc7c256d78e67536e27df37fe35d3e833f8ca3`  
		Last Modified: Sat, 07 Sep 2024 12:11:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c871d25e7d286117b64383db1b6171fc247e3b9e63886749f0c097e189c7a5`  
		Last Modified: Sat, 07 Sep 2024 12:11:48 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:0db82695a04f944ce709cdc145d178358abaa5b6c76ac38604e34d0a5642403a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2177194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1b667738e2bfb8dc10d73a4485b0eee8663eb754b7271b4b836868e3249341`

```dockerfile
```

-	Layers:
	-	`sha256:e8bfe1b3cd1179f974621b57cddaaea0bf363ab595559af86a515089ab929074`  
		Last Modified: Sat, 07 Sep 2024 12:11:48 GMT  
		Size: 2.1 MB (2146021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:503420ff7ee430ff82b5f86e53c208061cff7f62369e49e2ccdcef45a26f9641`  
		Last Modified: Sat, 07 Sep 2024 12:11:47 GMT  
		Size: 31.2 KB (31173 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:2043c2f8f46ce6f0445fe5e57fd52434ee4d5510b1dd52f6daa134f8fe2625d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68124960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3565cc1e15698e57a8150b288782ea260b102c9ba0cc4b79ccdbb2c8336827bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Sep 2024 08:44:06 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
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
	-	`sha256:09bf9557432bbdef33ddb427f92043fcebd0801fc505a1adf668ed52df601428`  
		Last Modified: Sat, 07 Sep 2024 09:02:35 GMT  
		Size: 12.5 MB (12502100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832fbd36a37bb647d4f369ae513f801bbc86b1f4660c03543efccad3481d5168`  
		Last Modified: Sat, 07 Sep 2024 09:02:30 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c711af5c4c1695485d28012b13d1c51a265543fc8db40e1a81008dd13ca8e74f`  
		Last Modified: Sat, 07 Sep 2024 09:02:45 GMT  
		Size: 16.8 MB (16787330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9215c2521b4074fbf982728e57977eab49d5ef1608b0d6f3924211ff3bd87bb`  
		Last Modified: Sat, 07 Sep 2024 09:02:30 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329ef831e65bdb4c518b251afea95ece6a716e3f73451587ac2df22a4e718e95`  
		Last Modified: Sat, 07 Sep 2024 09:02:30 GMT  
		Size: 19.5 KB (19496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa97e2db644792ccf751d1c283a6f89e0fb9c4ebbf9783f8fab17983847876c`  
		Last Modified: Sat, 07 Sep 2024 18:13:40 GMT  
		Size: 31.1 MB (31085662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a813d6316bc0ba8e70a0f35c2dec361800572fcf1dad07c66889e436eb8f0536`  
		Last Modified: Sat, 07 Sep 2024 18:13:35 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a1f45cffca6f700b86d1840991a29aa2ff28d761517bf06cf4265a759ab0e4`  
		Last Modified: Sat, 07 Sep 2024 18:34:12 GMT  
		Size: 948.8 KB (948822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ae820656a3026d75cd896ddfb8c712b63434f5e78ca547f38a87da2d57760c`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88639190a87fd119a136357be816f8905fd74600573e3bd1f934f3bb9629f145`  
		Last Modified: Sat, 07 Sep 2024 18:34:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:9df12b784247f4dfe41eed5de310db57fa42265b3d8ded30d8836ef8e717df28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad3aea1250c0e48410483987db42056df9ad0399e2b3950f99c9f2c5dea0de5`

```dockerfile
```

-	Layers:
	-	`sha256:dbbf57917c9f72d7f732c2067c8a5ed976686e5d4085358266e5f9e8243424f2`  
		Last Modified: Sat, 07 Sep 2024 18:34:12 GMT  
		Size: 2.1 MB (2145637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9cf3cca05d56421ee93b00df713dd99121c604932856dcb2c5df01105adcf1d`  
		Last Modified: Sat, 07 Sep 2024 18:34:12 GMT  
		Size: 31.2 KB (31173 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:ff36d9001fa41a2d6c84d62a0359735d72fcda1401731bfa772abb23d1f44025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69321300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7902f98b3d7be99b0c11b8cf1cb828892d9d62ea6d097a9e486bf9f21b39dcff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 05 Sep 2024 08:44:06 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
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
	-	`sha256:b01bc6eedfe1940010bf7f80686ab2c59f5c198ebd2cd96093d1954d0793fc7e`  
		Last Modified: Sat, 07 Sep 2024 00:43:52 GMT  
		Size: 12.5 MB (12502104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd07af6543bea86ebf354e041998ee8f2235f43aea892f548bfc7143db166a4d`  
		Last Modified: Sat, 07 Sep 2024 00:43:51 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bc72055f530c49bcc69cdf1e7a38ee801645be80f623310d25b3e26799945d`  
		Last Modified: Sat, 07 Sep 2024 00:43:54 GMT  
		Size: 17.3 MB (17293779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1fcff7d6756a1533b94a7b036ee522447d7bea7d01858674c8f78bc02db06b`  
		Last Modified: Sat, 07 Sep 2024 00:43:51 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688b07c5a1515de52e3cbf1fc05e3c6eb711dafe243d32d431657f02f7712106`  
		Last Modified: Sat, 07 Sep 2024 00:43:51 GMT  
		Size: 19.5 KB (19480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff27e4636448080f5041d7e73b0f85523bc0de9af9a8acb1f0574e0ca92c54b1`  
		Last Modified: Sat, 07 Sep 2024 11:03:25 GMT  
		Size: 31.6 MB (31612782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2577ec2ae6b1383d8224a070bb97330c00a13b4527a34c06bdf7ed9444cde7a`  
		Last Modified: Sat, 07 Sep 2024 11:03:24 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dd3f05b8c360f1507484329ec3695bd4e2432dbaa71bf968718da07248057c`  
		Last Modified: Sat, 07 Sep 2024 11:04:52 GMT  
		Size: 952.7 KB (952685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bae736bcf962bebe1953244d8c96c8fc17b311ba45a0419f1cd8adae1804e35`  
		Last Modified: Sat, 07 Sep 2024 11:04:52 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bee60f4bfc73495fae957ce9fa2754fe26174d143b860fb56231d74f6748c8`  
		Last Modified: Sat, 07 Sep 2024 11:04:52 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:153abbedd2f8587bcc7b939e8072a680fb4eb37dfa74e869f36a00a332372e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e44cdc250416fd5f39bb439a18a9a49878e94a71f52618314d0565b88001ad0`

```dockerfile
```

-	Layers:
	-	`sha256:88a01f1241570c71c796f0e4847dc0fcee2b46ca550eb678a763e720b313bf4c`  
		Last Modified: Sat, 07 Sep 2024 11:04:52 GMT  
		Size: 2.1 MB (2145417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43be1f0ffb072f57c35b5a00d000334a6e663d9cd9590970cd4fa00c5b5eb2a2`  
		Last Modified: Sat, 07 Sep 2024 11:04:52 GMT  
		Size: 31.1 KB (31130 bytes)  
		MIME: application/vnd.in-toto+json
