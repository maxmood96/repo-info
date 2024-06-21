## `composer:latest`

```console
$ docker pull composer@sha256:e61fcaa4a0cd4c18a36f3e6cc06e150b02aed0d4a3a53bc1a02524e2aeaa7c0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 15
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
	-	linux; s390x
	-	unknown; unknown

### `composer:latest` - linux; amd64

```console
$ docker pull composer@sha256:910b91b0e98a3ed369f0f6c0d68b4ceb483dceceb85dfa9e1c0293e4437715ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68219516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47499b4276acad8bae9b4b605dd0c79209942065c0f37e17e0c337961ff7295f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:05:12 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:05:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:05:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_VERSION=8.3.8
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:05:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:05:12 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:05:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_VERSION=2.7.7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ed43a8165048a0688eda4741a1c89e730a72a7647897adef61a18b9017f2fc`  
		Last Modified: Fri, 21 Jun 2024 02:20:31 GMT  
		Size: 3.3 MB (3267719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82333a17c7c21e5bb46fbe4c79ef67474e6b016204698b266e09dc1477d55f18`  
		Last Modified: Fri, 21 Jun 2024 02:20:31 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bc217d680f55bf9778238a32a4aa5b811c1e9199fbee493c57c487d7f0adf2`  
		Last Modified: Fri, 21 Jun 2024 02:20:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d17a28ca59a005c545829d6693ffcb76f82e43baacb8c2a1efcd386d2bd2228`  
		Last Modified: Fri, 21 Jun 2024 02:20:29 GMT  
		Size: 12.5 MB (12502034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281242b060e09df5af82e5d83f5fa6b18bf4427fafa7fac46dd0e6fee9a3e6c5`  
		Last Modified: Fri, 21 Jun 2024 02:20:28 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ec29a3be40123d66c37253b9bbc229f060613033abced58d04511d2e385f5c`  
		Last Modified: Fri, 21 Jun 2024 02:20:31 GMT  
		Size: 17.2 MB (17210029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290fd3d444de4282ad968c14bbe4671bdf2467c8b3c472443c2251e89a03b78b`  
		Last Modified: Fri, 21 Jun 2024 02:20:28 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166bdd0a726df8b909142652fb668ad0b321e257caef1c8f50b2135ee6bfc3e0`  
		Last Modified: Fri, 21 Jun 2024 02:20:28 GMT  
		Size: 19.7 KB (19686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0214d91cdd64e7351b9629a36e6502888d1c49d1c1f8424b35e4e2696754f9`  
		Last Modified: Fri, 21 Jun 2024 02:58:48 GMT  
		Size: 30.6 MB (30645049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450abb24060d190c0e9af6364617d87ea7a0f62cfa2b035923511a4a60f90ca3`  
		Last Modified: Fri, 21 Jun 2024 02:58:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eaef02d19855bc9d7d14106c2471e743e60ea475ece47876c87dc01aa88471`  
		Last Modified: Fri, 21 Jun 2024 02:58:48 GMT  
		Size: 946.3 KB (946282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b27cf78bfae83356b7bb26e768d860d12a2c581ef49ecffa48f36c9566abfc`  
		Last Modified: Fri, 21 Jun 2024 02:58:46 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090322b946344e19d4cf2563cbee0c1885e9afcab4c5f30e462cd0d2c2d9cccf`  
		Last Modified: Fri, 21 Jun 2024 02:58:48 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:53038122def012fb679c4f3074cfd6aadbfe1c13092132a654871b7fb03c997f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d164367bf9cef3ec886985a6d94b746d1542646460bc7b190b4521b63fc8aa13`

```dockerfile
```

-	Layers:
	-	`sha256:7550c6d3331a36cc5e7a84597af78551ac0f8b24a22266cd978dd9f8adc3a8db`  
		Last Modified: Fri, 21 Jun 2024 02:58:48 GMT  
		Size: 2.1 MB (2132368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6210a112f4e23fcd416b0d94d0de35552b549ae26df4c325cd71bbd0e16581a`  
		Last Modified: Fri, 21 Jun 2024 02:58:48 GMT  
		Size: 31.1 KB (31113 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:324039c0427922d28098eab5604fb50faddbe5d24e5501898fec7d0654f0ac66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65261593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007fe135b15e4d76452771533e5b14de4aea9a6c32d003b6b5241c085e15e369`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:05:12 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:05:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:05:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_VERSION=8.3.8
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:05:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:05:12 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:05:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_VERSION=2.7.7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b742a94a2a02339935795e4cfe19c5c5a34bda515f8dd7093f6b3b3d8c4bc8d7`  
		Last Modified: Thu, 20 Jun 2024 23:09:54 GMT  
		Size: 3.3 MB (3256620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c77d1b62b835ef15e0949a470ee8d8f22fee0fbe8b58a2e2fd20e0a4c846b39`  
		Last Modified: Thu, 20 Jun 2024 23:09:52 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709ede69d280e5de26d94feca8b022309b197b315f50154ceffead1e18a5edd6`  
		Last Modified: Thu, 20 Jun 2024 23:09:52 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4a4d8bd85e4d8c121c1a7b38c4910dabe1a9dccdb862002454563be758891f`  
		Last Modified: Thu, 20 Jun 2024 23:09:52 GMT  
		Size: 12.5 MB (12502045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254de13501e7bab1164c77361a8975eda7a6cedb8aacb1d8f4a30d24587a2000`  
		Last Modified: Thu, 20 Jun 2024 23:09:50 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d749cd7122c2df0580749401b19571fcbd831e31b20b7172ec5c4d05397459ed`  
		Last Modified: Thu, 20 Jun 2024 23:09:55 GMT  
		Size: 15.7 MB (15716563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d930f5540a9042044b9bda8eda4261512ed4df887cfa09db062df6bf0bdad91d`  
		Last Modified: Thu, 20 Jun 2024 23:09:50 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b80f4d80d45fe5eb756db7bbd1395b37dafc0a52406703ca3a8087c235ca35`  
		Last Modified: Thu, 20 Jun 2024 23:09:50 GMT  
		Size: 19.5 KB (19486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0c0175610da90188c806aa760c4e5de24c814c3c6d1b6767f0a0fed70c1959`  
		Last Modified: Fri, 21 Jun 2024 05:23:06 GMT  
		Size: 29.4 MB (29449586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7302695c8e3dadfdc14ac05eb7059dd513acc46710c4e887512b2bbb8bd9eae`  
		Last Modified: Fri, 21 Jun 2024 05:23:06 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc94b43c8cb8d295ed392c0f574d29a59a8f41d636bc7f0e974c8883e0887e9`  
		Last Modified: Fri, 21 Jun 2024 05:23:06 GMT  
		Size: 945.3 KB (945269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd9e8b8c28479a4962be2b69172d093d0c589c0419361b4ab4f961e0a79d76f`  
		Last Modified: Fri, 21 Jun 2024 05:23:06 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a777225a37e81c7edcac34b917d70711cab896ad900e6c0f4b19f69b2cb2df`  
		Last Modified: Fri, 21 Jun 2024 05:23:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:0882738cd9a37a790afd462c3a9c80735ce457f1a4f03be51a960752f9c96b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (30989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec567da8cf3036fcb166f6fa1142d6c7ce846965b61748e35a9409a451d0eef`

```dockerfile
```

-	Layers:
	-	`sha256:ddc1784dd57acb09939ad2eca5c071eff0c24cf20128fe1d464c7effa27137d9`  
		Last Modified: Fri, 21 Jun 2024 05:23:03 GMT  
		Size: 31.0 KB (30989 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:273763bfecd5d177ce1800c606bff9c38e7285f17c9e03aea92ffbdb7dc41db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63409244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c311488361f4f03889633fd74a4711d817e7be5e93a6e09ac84005fb6e771d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:05:12 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:05:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:05:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_VERSION=8.3.8
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:05:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:05:12 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:05:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_VERSION=2.7.7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b938a00e90a786cd6136482ec16d36fde70734970bf1a3417ac3a7bc1ae3db78`  
		Last Modified: Thu, 20 Jun 2024 20:08:04 GMT  
		Size: 3.1 MB (3069230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff9bafae6056d786c9d80432f880c7019dc7cbabf4b4422e3722984e47fc241`  
		Last Modified: Thu, 20 Jun 2024 20:08:02 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bf863a52c49447e08f0ca17d6916598399d3a5919085117aee7b8825dff07e`  
		Last Modified: Thu, 20 Jun 2024 20:08:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cee402e485981021b2420ecd2ba2775d94ab320ce68cfe4fc0855883d3b6f6`  
		Last Modified: Thu, 20 Jun 2024 20:08:02 GMT  
		Size: 12.5 MB (12502049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d436dcee1d16793a23599741cd1b91ee720f57192832352f460f803b16910c3`  
		Last Modified: Thu, 20 Jun 2024 20:08:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cbe638b2d63295e18b4282a2532c8fdcdca510f12fc04d1f715a819f65d14c`  
		Last Modified: Thu, 20 Jun 2024 20:08:04 GMT  
		Size: 14.7 MB (14709501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7875aa1d47c778f951cd5347a822fd677883923fcdfe2546212461964a5902`  
		Last Modified: Thu, 20 Jun 2024 20:08:00 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4595c8b3410790eeb56a5772045e8278c250bea46b956180163e5dc34e64c5`  
		Last Modified: Thu, 20 Jun 2024 20:08:00 GMT  
		Size: 19.5 KB (19486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8375a84043e25ef3c5ec30c08daca826b7abccc709d1afde82f163b09c0113ac`  
		Last Modified: Fri, 21 Jun 2024 05:12:37 GMT  
		Size: 29.1 MB (29072554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0f7dba9577c30e9ea521543a4f0836faca7c39f8f10b4cd1a84cdd43742747`  
		Last Modified: Fri, 21 Jun 2024 05:12:36 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace9c0c72d08e5eb2c9bd07e2cebdd68752d40fa54f93f366ee113c76de07535`  
		Last Modified: Fri, 21 Jun 2024 05:12:37 GMT  
		Size: 936.7 KB (936696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be2f02fd5c93a28a6bbf8c9409679f65dd5055dc8f37ec8d4bcb46496894bb5`  
		Last Modified: Fri, 21 Jun 2024 05:12:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5de1e063351a1b4cb229925fe7ae4c22aba8d85e286e5d578c3d88edb58874a`  
		Last Modified: Fri, 21 Jun 2024 05:12:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:2e94d7dd018de849f6a2759fd7c4d5fc350cf2e7963d41ce94dcca1ec37e445a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f83e4799ef14574ce39278dfb5e097fa02fcbe036a61b179eb779a956f3053a`

```dockerfile
```

-	Layers:
	-	`sha256:29a10c61622d436f64f00db3ecb6ce0f3784a1d938879d4f6b2249e4c5c58de3`  
		Last Modified: Fri, 21 Jun 2024 05:12:34 GMT  
		Size: 2.1 MB (2132689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bae2a188bb4c3913164d3e4e9e82be12a00bc27934ac36e71b50bbe2de6fa3b9`  
		Last Modified: Fri, 21 Jun 2024 05:12:34 GMT  
		Size: 31.2 KB (31209 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:629546a8248a5927baee023f21d83f005e1a52c1393ea2a51cfe17c6f270b6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69232448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9850a0a80b95a73c1da7e9f7da21315bca58be8d74f31a0ddbc0a03b28594816`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:05:12 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:05:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:05:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_VERSION=8.3.8
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:05:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:05:12 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:05:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_VERSION=2.7.7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7259c6ecde9ace3d2e6f16129e48d1f2a4617a863b50141060d68dff3bca6be4`  
		Last Modified: Thu, 20 Jun 2024 23:57:33 GMT  
		Size: 3.3 MB (3321315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba877fe96736ac16322578eac8e248770148b6e42b5f6059172ee20a2285ebf`  
		Last Modified: Thu, 20 Jun 2024 23:57:32 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8737749d8335aefd2aa7a5ecff2afc3bd5458f2f463a8dd634f9e53e953f7fa`  
		Last Modified: Thu, 20 Jun 2024 23:57:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663cd32f6f3843f89edcb11a813e21fb8a17e226a40fc7f33a7631bdb34fe1b8`  
		Last Modified: Thu, 20 Jun 2024 23:57:31 GMT  
		Size: 12.5 MB (12502041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ba0065b2b0fb1d6ad7811b1d21a3ae1f7f5ec752bd6d06416949c074f60cc2`  
		Last Modified: Thu, 20 Jun 2024 23:57:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebca2c445520008a7713de489ef71d91d0003bdca482e5ac3e3744919d1548`  
		Last Modified: Thu, 20 Jun 2024 23:57:32 GMT  
		Size: 17.2 MB (17185572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565810ee00e8c63409007ca2e4f78d964e5df47fbe55e1c8e3274889bd3b3ad3`  
		Last Modified: Thu, 20 Jun 2024 23:57:30 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9816fea9e05e1cc7b771a8a13fc5171cd3280163a881c673003e1f61825844`  
		Last Modified: Thu, 20 Jun 2024 23:57:30 GMT  
		Size: 19.5 KB (19473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc30eb39c17aab6156f2c533603f53e8ec9c2842b4dc1df1c0ca94d755b51ca7`  
		Last Modified: Fri, 21 Jun 2024 07:08:02 GMT  
		Size: 31.2 MB (31163100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b22da20955254b3e6b2ddd6557ddb91e5be2141b65fb67ce20a98c122165f03`  
		Last Modified: Fri, 21 Jun 2024 07:08:01 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a461179847826c59abf304a7de5c7107eefd64b1ed37b53c0dfb01931158ea93`  
		Last Modified: Fri, 21 Jun 2024 07:08:02 GMT  
		Size: 947.3 KB (947275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd47c6dc33a8b66f79cc8d4649b99281cd120ca413cbc449e9aa0519762d9520`  
		Last Modified: Fri, 21 Jun 2024 07:08:02 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a018835f71d5c199dd2a6e304bbebcd8f3827817c5cd0d14c746a3004dd7916`  
		Last Modified: Fri, 21 Jun 2024 07:08:02 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:16407951b38e2e43f140fa0706cb282ff305ea353e995f2a94c672c0184cb2bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d249dd64ae7f0c84223db37cf9b6b7fa7ef1f4de5096831e04d5c2309fdf10d`

```dockerfile
```

-	Layers:
	-	`sha256:a8b33aeb025569ee96b16f547875abb9acbd7aa71a3444d9b8de206b6fe045d0`  
		Last Modified: Fri, 21 Jun 2024 07:07:59 GMT  
		Size: 2.1 MB (2132519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14dfc9ea37f4c06c7f0cb3b997c0fbccc1d5ed55d0cc3801ac5062f43bb12d3e`  
		Last Modified: Fri, 21 Jun 2024 07:07:59 GMT  
		Size: 31.4 KB (31414 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:ddacfd687f90d05a357391adbe100456a7f7bc4d366b560e1f527e0c44f2263f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49164819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de242ece60ef963098c5848f3bac676b52e1f2b945b3d87a9d8164fee19415f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:05:12 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:05:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:05:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_VERSION=8.3.8
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:05:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:05:12 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:05:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_VERSION=2.7.7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2323366a64c9696e4b985a0b5c338075544e5c4feec46f2d10d51a7b595e29`  
		Last Modified: Thu, 20 Jun 2024 22:59:30 GMT  
		Size: 3.3 MB (3318654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed21a4a2f5c9deb46389e5d3a9c39b9a42ef686b0202b042c9f8e3658a211b2`  
		Last Modified: Thu, 20 Jun 2024 22:59:29 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4dc126214224f26071d0bbfbff76af0e96a93d7e261c5c921b22224b77f616`  
		Last Modified: Thu, 20 Jun 2024 22:59:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ed12bb4615ffa6cd183ca1a7023b36ea37824b4797b7e04541c6150f4661cb`  
		Last Modified: Thu, 20 Jun 2024 22:59:28 GMT  
		Size: 12.5 MB (12502037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90be338f99d81d0b78a1a7fe59b136d504415dc406442da50f6d2f8bfa1cac5`  
		Last Modified: Thu, 20 Jun 2024 22:59:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1054d71cd628ae8cf3000c70839e795eba6aa0d783220f241fdf3ecb68df4c2b`  
		Last Modified: Thu, 20 Jun 2024 22:59:32 GMT  
		Size: 17.6 MB (17644973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3fad65207ceb77f2fe35bdf6c8bb7808ebe7b2cd1f4e4298178ec461052890`  
		Last Modified: Thu, 20 Jun 2024 22:59:27 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01ac6a2ac96f96101f3797e77b8fe4fded39c835dfc33c493fd17c2b10bfe38`  
		Last Modified: Thu, 20 Jun 2024 22:59:27 GMT  
		Size: 19.7 KB (19692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fa631ffc652ee62453a5e05acba962ac2e762531d66b02c71521a23b0340ff`  
		Last Modified: Fri, 21 Jun 2024 01:02:44 GMT  
		Size: 11.3 MB (11281342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db61a4ad3953d7d2b7d418cc0e1ad1360121959dc110fa3e2318e292b40fdcfe`  
		Last Modified: Fri, 21 Jun 2024 01:02:43 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dffb8f80c0d5997b33ddfeb79eddfb24b9c047d3a14aef3812515c9431dace4`  
		Last Modified: Fri, 21 Jun 2024 01:02:43 GMT  
		Size: 923.8 KB (923782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386741bce3dde9b65505d51bd9f1394d4c389f7c805e970a861df81acd3b7d14`  
		Last Modified: Fri, 21 Jun 2024 01:02:43 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249bc2f0930080d38050bdbab222749a6a7428035efedc4ab02ba9bd6cd5ea8d`  
		Last Modified: Fri, 21 Jun 2024 01:02:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:3be8353aba5c837deb0ca92cfb857baf4978a6821e2ed8c1b0b56818e87311d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.5 KB (438547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfef3a9acec353e65ad09457a5afc2cc0290ccb0a4a29e0ff6f89abb3964736`

```dockerfile
```

-	Layers:
	-	`sha256:b22950591204297d287a2aff7cfbc8fee014df24a7d75e70a6f145a60922e148`  
		Last Modified: Fri, 21 Jun 2024 01:02:43 GMT  
		Size: 407.5 KB (407467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f9d10b08a2deb525d973a98dd4d9bc589b9e0dc3ea1174ba00e13808ed8bfb6`  
		Last Modified: Fri, 21 Jun 2024 01:02:43 GMT  
		Size: 31.1 KB (31080 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:42ea5dfe7cdb66d70b0b94d664b6388af0bea8c6b45837b76c63f8e3fad288e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70203636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4676cd8ccf7eeea47909089c6cd29078427b4c178caf7833c1fbeac5606d314f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:05:12 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:05:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:05:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_VERSION=8.3.8
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:05:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:05:12 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:05:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_VERSION=2.7.7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a26704de1bf6248f6df44727e1e01ae48fec7917e229bc3e343c672804b51`  
		Last Modified: Thu, 20 Jun 2024 19:38:43 GMT  
		Size: 3.4 MB (3395236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ee9c5937bf5aa444d1623e38c7154bb2971a8bd3cbd2f3b736c22ed6c73927`  
		Last Modified: Thu, 20 Jun 2024 19:38:41 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84c1b8ee2969afc28f29a4447dc6ee6dbe5a916abb033890d01ce72b9e98d79`  
		Last Modified: Thu, 20 Jun 2024 19:38:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89529e8b651a22e085a5430cb7f479d395fcbd64e3127aedabb48e8181332f78`  
		Last Modified: Thu, 20 Jun 2024 19:38:41 GMT  
		Size: 12.5 MB (12502054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473e9d469b421e659e412a9f333e6bd6a0ed28269cc6b4a9fb8d31d3c5acdd54`  
		Last Modified: Thu, 20 Jun 2024 19:38:40 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529ce7b17230c441489dd80760dce433a5f3517fa6a9858c4a1005ed542497a4`  
		Last Modified: Thu, 20 Jun 2024 19:38:43 GMT  
		Size: 18.1 MB (18079918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db790725292d505da33caf1514fe7a4b2dce4a460e9dbceef4338df8251835a3`  
		Last Modified: Thu, 20 Jun 2024 19:38:39 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047ee18af0632ce98c883d9cac613bc2a040a169dd040b8fd40ad6408c46dff3`  
		Last Modified: Thu, 20 Jun 2024 19:38:39 GMT  
		Size: 19.5 KB (19477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3862ebc86c7a40200fe7fc6afe05c4e71ea3611adeede2ca849eb46f27ec8a3`  
		Last Modified: Fri, 21 Jun 2024 03:21:06 GMT  
		Size: 31.7 MB (31677190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34147d5325ece828dad7e4ff27630443c10a41d5f7838a309c018da76e194b33`  
		Last Modified: Fri, 21 Jun 2024 03:21:06 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7102a56659a02f87c948d67018aab910e78eb044ec31c72e9ca1fb65bfd1bd2a`  
		Last Modified: Fri, 21 Jun 2024 03:21:06 GMT  
		Size: 953.2 KB (953185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef58f3fb56121aaee76f78fe7a298cf5b6f6d7d9cf557c5f1e1714422ea2b07`  
		Last Modified: Fri, 21 Jun 2024 03:21:06 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fd471bcc8d4840dee5a045055598d0c895e38dae4077c274d140e9bae1eb6f`  
		Last Modified: Fri, 21 Jun 2024 03:21:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:505b18c3cdb8fae35bbfd822c389d22e565d653a315b65f9efd384c3a6b4dc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2162078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc3918f4231822f163f5821502a7aebc920f6440b267c3357917d9385b91c8d`

```dockerfile
```

-	Layers:
	-	`sha256:6cb003299873bf47f6f30d693e83f7ffe3c75799870918a33854055289cec765`  
		Last Modified: Fri, 21 Jun 2024 03:21:03 GMT  
		Size: 2.1 MB (2130923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cd1cc38f04424dc2026249734ea29e6a6afb6e6d048e9d256877de31fa0c9f9`  
		Last Modified: Fri, 21 Jun 2024 03:21:03 GMT  
		Size: 31.2 KB (31155 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:e9cf6ccb474d06537006c4df951553d2a3d55fa46d4119ffb2b89e7c0a66925a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68101857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e6be11e953a461b5f9ee83c1de8490b6991336c313629200d95351414df33b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:03 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 20 Jun 2024 18:18:04 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 20:56:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 20:56:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 20:56:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 20:56:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 20:56:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 20:56:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 20:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 20:56:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 20:56:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Jun 2024 20:56:16 GMT
ENV PHP_VERSION=8.3.8
# Thu, 20 Jun 2024 20:56:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Thu, 20 Jun 2024 20:56:17 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Thu, 20 Jun 2024 20:56:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 20:56:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 21:43:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 21:43:35 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 20 Jun 2024 21:43:42 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 21:43:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 21:43:43 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_VERSION=2.7.7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75477805297b2e5d3e45445d2b14ef5781642095163a9180372584156228308d`  
		Last Modified: Fri, 21 Jun 2024 03:29:15 GMT  
		Size: 3.4 MB (3390439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f052e2934ece7510f678f44b5c8af4ca01c8c831d77f69244bf017c94d869629`  
		Last Modified: Fri, 21 Jun 2024 03:29:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb6c1f73b878cfca599e88261cc519ca171226efafcdd1238320261b2c41459`  
		Last Modified: Fri, 21 Jun 2024 03:29:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee3f62bf16f7ef1294f1096cec84c1085b891b6b4bc54329a861da523dd4111`  
		Last Modified: Fri, 21 Jun 2024 03:29:15 GMT  
		Size: 12.5 MB (12502047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3fa197fcdc4dfa020c22ecd62c21572959a1b3e497405525011e0b132ab20e`  
		Last Modified: Fri, 21 Jun 2024 03:29:09 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5883f456186079d5e35bc0b97895d167b676f00d217fea3451e9865f38d55977`  
		Last Modified: Fri, 21 Jun 2024 03:29:27 GMT  
		Size: 16.8 MB (16784256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e04dc0c5d1c0750e89c9c3ca7fc8b1e54c7b44b7d18cd939f635f75a71e7ff`  
		Last Modified: Fri, 21 Jun 2024 03:29:09 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e365e7f369d1f1ab642c1e128f166e116cfcd84c330c7d124f2b71466d796481`  
		Last Modified: Fri, 21 Jun 2024 03:29:09 GMT  
		Size: 19.5 KB (19487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8180c8ea3de9e6f1935fd612ec023e0b69d30ab8f88f68cab2453b268d9a28`  
		Last Modified: Fri, 21 Jun 2024 04:19:36 GMT  
		Size: 31.1 MB (31083741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea99d964a7b43e0ec43d6e9f704efb67fb78b9a7fa262eece696e2218c0cc63`  
		Last Modified: Fri, 21 Jun 2024 04:19:08 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6cd5030b8869e7ec986a7dc38a2ae6c0bc59ac3f8afdb959d171589de3e251`  
		Last Modified: Fri, 21 Jun 2024 04:19:09 GMT  
		Size: 946.0 KB (945966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4583856d2043094e62e61079e10429af017662fe6ffd55212be8702701d0d00`  
		Last Modified: Fri, 21 Jun 2024 04:19:08 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8562378508bedb30a7743fbb6f454aaefa60feb24fd988b1072cc2cb9721d4f`  
		Last Modified: Fri, 21 Jun 2024 04:19:08 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:6dec3826417e304e6543e3a84c6ff51d3883227c6edb13154ce6b33f4d3e2f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69297496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460f7d7239e21da11f04db6b178935d3954f207396653caca26de542b827203c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:05:12 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:05:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:05:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_VERSION=8.3.8
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 11 Jun 2024 08:05:12 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:05:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:05:12 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:05:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:05:12 GMT
ENV COMPOSER_VERSION=2.7.7
# Tue, 11 Jun 2024 08:05:12 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:05:12 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:05:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:05:12 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3e83a7b4cb32d011e679386186946d82818581def86d57f1b8c9ca8c934c1c`  
		Last Modified: Fri, 21 Jun 2024 02:02:33 GMT  
		Size: 3.5 MB (3462701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1864acc991a0f2fd74bdcd479ec121dcab7cd543eb1e6666fac2260843f34bbd`  
		Last Modified: Fri, 21 Jun 2024 02:02:32 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed80ee1d18ee2422d537f9fbb168383860d34cfce3c9b043a35b6d86b38f2da6`  
		Last Modified: Fri, 21 Jun 2024 02:02:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6488a0b1d5fd5f27443e1c0873cb7dfac092f0b4dd25cac2fb283d3f8ddd68`  
		Last Modified: Fri, 21 Jun 2024 02:02:31 GMT  
		Size: 12.5 MB (12502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d20a89b6f41dfd236a74abaf243262d7efb53fb417be4080840b604abeda6c7`  
		Last Modified: Fri, 21 Jun 2024 02:02:30 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b37417151fccf67f67a76563d9ca2b51debebd8fc103273e0f142af3609510`  
		Last Modified: Fri, 21 Jun 2024 02:02:33 GMT  
		Size: 17.3 MB (17287366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bd3dc4f6309edc200f24ea8ecab8a01ed01dffcf95c77685700f7eca31c83d`  
		Last Modified: Fri, 21 Jun 2024 02:02:31 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564d26ce9a330b24d712bc548e4709d561ae3e07d88efcfcbd1f1216dffe90af`  
		Last Modified: Fri, 21 Jun 2024 02:02:31 GMT  
		Size: 19.5 KB (19479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e584f930f14e509714f73327c56a416fc2889a27bfaa446115a43537b2fc61`  
		Last Modified: Fri, 21 Jun 2024 06:11:17 GMT  
		Size: 31.6 MB (31610114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407f8ef0793193a13e9d94eebdd94d5b135741881fce6ae154aabd3a86816e00`  
		Last Modified: Fri, 21 Jun 2024 06:11:16 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fec9b088551f3a6e56034bd648da03e7f37f3729d51ade2112e462077dec89a`  
		Last Modified: Fri, 21 Jun 2024 06:11:16 GMT  
		Size: 949.1 KB (949056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066216edfceee464d18d4de980eca245181f3429f8c43bebc6caa873642f66b4`  
		Last Modified: Fri, 21 Jun 2024 06:11:16 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3e1b0ad8dfeb893ad5168ba03270f5faf30193d0f58e3a5cb18c1923f739d4`  
		Last Modified: Fri, 21 Jun 2024 06:11:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:30528a28c222de70a0920fc11a6b10bafec4ceb79ce1eb9124765a63a9212851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01458a3d72a479767dbfdf4d8acf21b1a97e26a4c2ec109dc5fc9ccfeb925fae`

```dockerfile
```

-	Layers:
	-	`sha256:8496af57e3d54ef35136d2da2f4dc92443349b2855633af7cd3af0a3c94ba6e6`  
		Last Modified: Fri, 21 Jun 2024 06:11:14 GMT  
		Size: 2.1 MB (2130319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:677b65f3294489b343097544d0f9cbc218901d50c07b924acad75bf9cf5fda60`  
		Last Modified: Fri, 21 Jun 2024 06:11:14 GMT  
		Size: 31.1 KB (31113 bytes)  
		MIME: application/vnd.in-toto+json
