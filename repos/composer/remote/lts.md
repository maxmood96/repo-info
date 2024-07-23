## `composer:lts`

```console
$ docker pull composer@sha256:445430866314684111bb56d2d3d2a59dc35b283938cbda281aa234aa6e265a71
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
$ docker pull composer@sha256:b2011bd375b9e1524799ded0cab5cde1ab03581ebeafdafc4425c4d55c8b05a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68080192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527e72c389d61b71f8b24df24c012141dea95266844dc9f514291c47d31ea6df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:09:22 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:09:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:09:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_VERSION=8.3.9
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:09:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:09:22 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_VERSION=2.2.24
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae0d9dfc4dada15e6a030ba7b9c9a3b16f9f5a7597a4d46ff24226e91b91db7`  
		Last Modified: Tue, 23 Jul 2024 03:55:04 GMT  
		Size: 3.3 MB (3272601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce295ca8623e5dc914104e970c5496db996db5f2abb336389bcbadd10465d21d`  
		Last Modified: Tue, 23 Jul 2024 03:55:03 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d3eb99f3c122bc8d6c22107602ed9c22fce771289b54bb2598142d1626f693`  
		Last Modified: Tue, 23 Jul 2024 03:55:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da48d7a5e0690b25131025f4187cd876e3ef774226b1565897b1d8a7bd5e5dd`  
		Last Modified: Tue, 23 Jul 2024 03:58:16 GMT  
		Size: 12.5 MB (12491144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e142cb738903ef1899d23399f4e2e6300c8874a2c664604ec9b2775ef9e258`  
		Last Modified: Tue, 23 Jul 2024 03:58:15 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29730a6e13b27677c98aae645d2b244d383908506ec4529f6e3f3b447d6b1a70`  
		Last Modified: Tue, 23 Jul 2024 03:58:18 GMT  
		Size: 17.2 MB (17209325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c72ceb0cb5822610cc809ab8555d5d0668bcc1cefae5ec982bae91a0ed6ef1`  
		Last Modified: Tue, 23 Jul 2024 03:58:15 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ea4d2072fa2a974ecf0027c6c9717307073d1cb4e7e4f583505df1c1e58c3d`  
		Last Modified: Tue, 23 Jul 2024 03:58:15 GMT  
		Size: 19.7 KB (19694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136603b9481a092492d97d93bac94ae8281d32cebc40c7f8e134b08f4817f446`  
		Last Modified: Tue, 23 Jul 2024 06:08:46 GMT  
		Size: 30.6 MB (30645585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2984ac9050c233513a01b1a72905ea1a95d8f085ccb0e28cb41e655318a6ec`  
		Last Modified: Tue, 23 Jul 2024 06:08:45 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517a519ea021a03a6460f36a2d996ed72a31f6d6e52e68a2275205a082be669e`  
		Last Modified: Tue, 23 Jul 2024 06:08:46 GMT  
		Size: 814.1 KB (814077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710fc30e42ba716c01be37060c510c8a64b6e8900f5e81e6a0abb20107dafb46`  
		Last Modified: Tue, 23 Jul 2024 06:08:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb46367a5cb912ce7be53b326c4d4a2fec889370e30ae42f2399e2c245fa7896`  
		Last Modified: Tue, 23 Jul 2024 06:08:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:040d91c665d1bf8357fb92eb7e0549f620495b782673f7480f229d5f9e9c22bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2178006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2149ab7fed68904437662bc8d4f44b27fe4559802e9c053596192bea6312da4e`

```dockerfile
```

-	Layers:
	-	`sha256:dccdb45d073a0cf74247a663207200e56399baf28c4b9682d591f39e0c0f2243`  
		Last Modified: Tue, 23 Jul 2024 06:08:44 GMT  
		Size: 2.1 MB (2147188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fa16623ef18031e2123bb925de6a1de07feaf03ea7d1a0cd010cfbad2f161f7`  
		Last Modified: Tue, 23 Jul 2024 06:08:44 GMT  
		Size: 30.8 KB (30818 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v6

```console
$ docker pull composer@sha256:9459caf92e3d1635e0c24fac9aa45b254a3caa34fe8605f87e4336f0472ae68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68082620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfb05032099ccee5f86854319ce6c8f620fe70a572976339f947f7cada7e666`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:09:22 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:09:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:09:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_VERSION=8.3.9
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:09:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:09:22 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_VERSION=2.2.24
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
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
	-	`sha256:e6ef44222dbd899ffd27a82e66c426246c6584e068ec366626b1969ad567f894`  
		Last Modified: Sat, 06 Jul 2024 01:46:58 GMT  
		Size: 12.5 MB (12491136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c7cbfcef68a2cf22e5290ac384248900d4ab2433b020e0dcec3197b67a065d`  
		Last Modified: Sat, 06 Jul 2024 01:46:57 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9557534c2cd897c888b3ac4b3eccb74c869d998549beaaf90a55344355579c83`  
		Last Modified: Sat, 06 Jul 2024 01:47:01 GMT  
		Size: 18.7 MB (18678789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0cf55048564d0937f80b89dece3f5f03d88485189b7fa9730195e52ebdbafa`  
		Last Modified: Sat, 06 Jul 2024 01:46:57 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28322a502c7f5e20da0a08379ceeaf2150665364e3f1901a4bb1f2f6e2cde8c4`  
		Last Modified: Sat, 06 Jul 2024 01:46:57 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5f527a3df91ff483760da80263ae0180f66270409208f012a6e4646c8d6f28`  
		Last Modified: Sat, 06 Jul 2024 03:04:16 GMT  
		Size: 29.5 MB (29450966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174cf292382b8d8251168d08af7657d3f80054de47d3a0625ad51127c6adc077`  
		Last Modified: Sat, 06 Jul 2024 03:04:15 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2376d6e65e85b34e139b60e20778222a58fe84537c3add70240aec080b864623`  
		Last Modified: Sat, 06 Jul 2024 03:07:59 GMT  
		Size: 813.6 KB (813606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea45f9716d3f03ddc088a78a95e47cfae018b1a25560acd4f746bcf64b9e066`  
		Last Modified: Sat, 06 Jul 2024 03:07:59 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71a9839d3f6306fa1a12deb90d1b4764d013fa62c093b73d0270ff73d83c241`  
		Last Modified: Sat, 06 Jul 2024 03:07:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:40167998f921c6f5faae0a2e2262f97362f340992a5e0f022e920edede059073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733057033e1e5ad170d9a09564db5c15fbe3bb3750a1301c491803733486a6e8`

```dockerfile
```

-	Layers:
	-	`sha256:e34f759d9cf14fe97ead1390e1d7a82ead9c307cb384a4076f856499cf1e4cd1`  
		Last Modified: Sat, 06 Jul 2024 03:07:59 GMT  
		Size: 30.7 KB (30687 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v7

```console
$ docker pull composer@sha256:ce693ac631cf68a2b2fd92431ab30486d474975864e119092837e56600e2d0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66010550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0629545c5ebed33b9f1591f9df48fc2ee561f4490b9d43e0b2707cf19a25f52`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:09:22 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:09:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:09:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_VERSION=8.3.9
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:09:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:09:22 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_VERSION=2.2.24
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
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
	-	`sha256:8dd40eaf05a250475706eb0b7de67873ecc0b3168c695553549c0c162e6490a5`  
		Last Modified: Sat, 06 Jul 2024 02:46:59 GMT  
		Size: 12.5 MB (12491140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0955935407e804e2e854fd94ecc622cc0effde2894e99ad4badec593bc548493`  
		Last Modified: Sat, 06 Jul 2024 02:46:58 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9262f66f464ca08bda456d4480071d4291409c6daf9ba24e470a80ed0d8a18a3`  
		Last Modified: Sat, 06 Jul 2024 02:47:01 GMT  
		Size: 17.5 MB (17453054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca99988bda80b5739958431b53206aa12982b6e05500631c49af80cc7bc85f7`  
		Last Modified: Sat, 06 Jul 2024 02:46:58 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e06a11222dd1c9edfd43273c4294c6e3ea6032f2d2afbcd935bc0e3741388a`  
		Last Modified: Sat, 06 Jul 2024 02:46:58 GMT  
		Size: 19.5 KB (19483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc31a9a6f59288c44d8bcd1625afd1efe539ba8755cd18413e9dc07e754d0353`  
		Last Modified: Sat, 06 Jul 2024 05:18:25 GMT  
		Size: 29.1 MB (29073228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d379cf81a38417537fd987dc679f54d2ca56044af1cb634bf71ef40082ba612c`  
		Last Modified: Sat, 06 Jul 2024 05:18:25 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f7577f71d667615505f5da139fb10a7fcd2b8a02ee5a0b210ecd107fd47e0f`  
		Last Modified: Sat, 06 Jul 2024 05:22:27 GMT  
		Size: 804.7 KB (804680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb314de983a64142c1f840d9b101d7f2216c1f45e55bc42cc5854c7d7e15f38`  
		Last Modified: Sat, 06 Jul 2024 05:22:27 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8113f4338a697143968f1e1e0ee42614e58968f9203283da026069362b4006`  
		Last Modified: Sat, 06 Jul 2024 05:22:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:4ffaf4e3459249e0147a2303d1bb9d47fc93cd1083eae76056541dece970aec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a9b91fa46910fc5a7dd508dbcdde8f70037a29a7009c9935070902dce49109`

```dockerfile
```

-	Layers:
	-	`sha256:2330eef2a5f09039f900bf26096dcba72efdd0309e475c3c22fd19e20480fbe4`  
		Last Modified: Sat, 06 Jul 2024 05:22:27 GMT  
		Size: 2.1 MB (2132387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07b3668ae9f9438fff7623d881d23cb5a22f2b35589401e67ba7b91f08bb56f`  
		Last Modified: Sat, 06 Jul 2024 05:22:26 GMT  
		Size: 30.9 KB (30906 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:a2d996dda9b647edf5c22318802a1d5a8683f6c2d0e2ee2e97bb0d0e88f84b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72807636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05114c939718b3602a2aadbcaffc71125358fa19833f6f919ed84b779bb636e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:09:22 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:09:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:09:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_VERSION=8.3.9
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:09:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:09:22 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_VERSION=2.2.24
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
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
	-	`sha256:00f9c00b8f6bd62bebca6a18f5b109fb4fb4fda9848fee768c1b2e608f7deb53`  
		Last Modified: Sat, 06 Jul 2024 02:31:39 GMT  
		Size: 12.5 MB (12491133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e868bb01ffa44798f3c72adb6d732b4f18d842ce09220d9d43d2d86c27ce39bb`  
		Last Modified: Sat, 06 Jul 2024 02:31:38 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8280b1fdf6f7904059ae52c4bf3994f1c2a0e71ca048c1a8297c9b82f581777f`  
		Last Modified: Sat, 06 Jul 2024 02:31:40 GMT  
		Size: 20.9 MB (20904322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011f62c9d7101c5c611bfc70fc5b2a4b02176648154753de1da9c167f438d2bf`  
		Last Modified: Sat, 06 Jul 2024 02:31:38 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22725227e1e12bfaabe106d1345e6a825cd119fcd442ceceed97009c7feec12`  
		Last Modified: Sat, 06 Jul 2024 02:31:38 GMT  
		Size: 19.5 KB (19479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca8fb0b7ac5677d22e6561a8527f1d23c63b6a544584c2890701a7b793dceed`  
		Last Modified: Sat, 06 Jul 2024 05:02:52 GMT  
		Size: 31.2 MB (31162421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65e7c91d854b0cdb26eaae1757cf84f854accf04052afacd4768fb3eb608d67`  
		Last Modified: Sat, 06 Jul 2024 05:02:52 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7a90a0c83496bfa410eb14297a60c7295a1823e70f0629cc0c07a10b945bb5`  
		Last Modified: Sat, 06 Jul 2024 05:06:14 GMT  
		Size: 815.3 KB (815287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e191e0d5ff8d863b9451dc2b5be2392fc892b280ae1347bbeb03e485b7d6d0f`  
		Last Modified: Sat, 06 Jul 2024 05:06:14 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e669fdcac1a074f6a1ffb4e629ca8dde57d165604c4381c963dbc380a703579`  
		Last Modified: Sat, 06 Jul 2024 05:06:14 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:9dbcac9d0bc4bfd9348f685e2f8a275016503032fe650d7d86e6524ac7706d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0a404bc4181f4f9fcb56591082dc004e1d0010d5f462eab921de77c9231ff4`

```dockerfile
```

-	Layers:
	-	`sha256:f8c5cf8c958cda18fea28184f2589f0159758d8c27cf728a1a61b54dd24507dc`  
		Last Modified: Sat, 06 Jul 2024 05:06:14 GMT  
		Size: 2.1 MB (2132213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0e3b590d25b4e0e57fe2fc1001399d0e45ddeeaaaea7033694212354a7d5b9a`  
		Last Modified: Sat, 06 Jul 2024 05:06:13 GMT  
		Size: 31.1 KB (31107 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; 386

```console
$ docker pull composer@sha256:8b2fb4366f720946d195a04c9eb9c42f6060638131c6b1d139aa98168b3bd05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49025247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e9f5236d0d2bbb66bfecdf6ba49eb24811a9e5ee09fefc2432597b003c5234`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:09:22 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:09:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:09:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_VERSION=8.3.9
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:09:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:09:22 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_VERSION=2.2.24
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3702ede31b739c37f265c096aaa90041a249a222cf13f8141408974d1da345`  
		Last Modified: Tue, 23 Jul 2024 02:14:27 GMT  
		Size: 3.3 MB (3322587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd32fd053b31656313ffe5c4d6a711c2bdfbac32689ec3ed4eb1993c89d7c5cf`  
		Last Modified: Tue, 23 Jul 2024 02:14:26 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c734d1f76ba06cf1de68095cf88223f8aecf6242e60ae0985e4b555bd937308d`  
		Last Modified: Tue, 23 Jul 2024 02:14:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8809eabb483bc5c67a1bcbe6b092cc84c09e8c07c3f68ceaeeadc70e1273aff`  
		Last Modified: Tue, 23 Jul 2024 02:18:04 GMT  
		Size: 12.5 MB (12491139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2348f8b19e856fcaae860d9ed870cebf7eef570d28f5780f99f5ae40199524b4`  
		Last Modified: Tue, 23 Jul 2024 02:18:02 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9a4477539c1c931a104045a2953ce372b2fff91f6f18eff29a43f29ab9145a`  
		Last Modified: Tue, 23 Jul 2024 02:18:07 GMT  
		Size: 17.6 MB (17646200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a97c1a2ac77d82458ff7a7da9cb4249602dbae72f4f4e563d1f823a260e220`  
		Last Modified: Tue, 23 Jul 2024 02:18:02 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17138e3de77ffcbf8be3fc01aa7174a70720c5f13f8632df6a3a2436bfbf6c23`  
		Last Modified: Tue, 23 Jul 2024 02:18:02 GMT  
		Size: 19.7 KB (19699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1854685bf201f5644935b83f55bb2f29418e0d8dc9762b956cfc5002698d8e2d`  
		Last Modified: Tue, 23 Jul 2024 03:03:34 GMT  
		Size: 11.3 MB (11281309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c5133c5567919eaa82479589099ec2783bbc35b4c642e8edf16b8eaccbb37`  
		Last Modified: Tue, 23 Jul 2024 03:03:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07256a84b37ddb2e11d6d047940f4fa620d5b734fc527471818c1c312c1fa30d`  
		Last Modified: Tue, 23 Jul 2024 03:03:34 GMT  
		Size: 791.4 KB (791366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0be00bdfcabf4a418124b586e11de3050054a9d0db0e05e6af137dfd1a6a79`  
		Last Modified: Tue, 23 Jul 2024 03:03:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185ce862d043cf51509fb13ae258a2d94841cbae381295f091c707539823d4c3`  
		Last Modified: Tue, 23 Jul 2024 03:03:34 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:44a61ca0cf2d624e88b517c2e0056fbedcae82cc2d74e21737b5a0818fa5d274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.7 KB (451652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ba7a925c7489fddd67d9df0121f63904e28b602344cb7554cbc20a75fd4bd2`

```dockerfile
```

-	Layers:
	-	`sha256:9dad2bd51594a59ee36c92594eee0450bf062cf9ad20d12382d98d096a0b7b8e`  
		Last Modified: Tue, 23 Jul 2024 03:03:33 GMT  
		Size: 420.9 KB (420862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:228721b85f751d292a385ba1c84d631b64b08e0adbfb869e6cc256c1ec021190`  
		Last Modified: Tue, 23 Jul 2024 03:03:33 GMT  
		Size: 30.8 KB (30790 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; ppc64le

```console
$ docker pull composer@sha256:3943d397e1d5553cbd922ccd92c0d8dbc20e57fa53116a664f901bab6fc49a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70066106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbab9b0023d58872fc92e0469453e2b35f7c3cdc1567c779652d19b749cc5db`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:09:22 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:09:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:09:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_VERSION=8.3.9
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:09:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:09:22 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_VERSION=2.2.24
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
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
	-	`sha256:2298a0635b24808ca33801fc6591bee31abc336cc00659919d267d6b2dc12024`  
		Last Modified: Mon, 22 Jul 2024 23:44:07 GMT  
		Size: 12.5 MB (12491148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed3c88984fa2f5172e314ab9e3e0ca346b7bbb0164f19c329a25c2cb2542e7e`  
		Last Modified: Mon, 22 Jul 2024 23:44:07 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef5e1842f56be6084283b159caac4469c710d45d7f31b91be17bab97f3f07b0`  
		Last Modified: Mon, 22 Jul 2024 23:44:10 GMT  
		Size: 18.1 MB (18079102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38e3994e9f7899e549c6fa82a28ea860b1c51496f7702058928079c0988e531`  
		Last Modified: Mon, 22 Jul 2024 23:44:07 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b5507da16054d88989fbda5978852e06782f0e38bdea681bc4a9defc50153`  
		Last Modified: Mon, 22 Jul 2024 23:44:07 GMT  
		Size: 19.5 KB (19481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc7288278cb2041d80b23c6b1140b07fb19318630a86f3c48ea4ddda20b3ced`  
		Last Modified: Tue, 23 Jul 2024 08:39:14 GMT  
		Size: 31.7 MB (31677872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b5ebfbfe063156f9e417268095bb6d5ec814d7f06e9dfa235ba25c838a8dbf`  
		Last Modified: Tue, 23 Jul 2024 08:39:13 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12eac33efdcd24c1f914fc6a409ddb408c4ab4fb2439d1be55b164808a1e79b`  
		Last Modified: Tue, 23 Jul 2024 08:44:10 GMT  
		Size: 821.1 KB (821098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b41bc73205482790231badeb37a071e6d3f6c02f307e34d772f4a22872ebdf`  
		Last Modified: Tue, 23 Jul 2024 08:44:10 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2e088c6a1816c6b726732936f348ca62f3fc1978b099cf60b243bbe7e272d9`  
		Last Modified: Tue, 23 Jul 2024 08:44:10 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:696c5276fc3edb2bb5c52b1fd144ffccecccc8fb35b56a074b87adfe722f08ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac00ef6d3a5bd3237138c8b2d838d58a1700ad116f20646a611172494e80f5d4`

```dockerfile
```

-	Layers:
	-	`sha256:5a4c66df28f333facafe68af412a83a563f43f1870c16e93dd7494c155db44be`  
		Last Modified: Tue, 23 Jul 2024 08:44:10 GMT  
		Size: 2.1 MB (2145737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:564479d751e53df52b9f5d76a12634d9056f0aef5b5e2533cf8843043df13b42`  
		Last Modified: Tue, 23 Jul 2024 08:44:10 GMT  
		Size: 30.9 KB (30854 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; riscv64

```console
$ docker pull composer@sha256:6d11226ad6bae036873e9ec72c9f60bdc97eb35a51a7276b584a30cbda00244b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70927149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e374a3d26f59c563727400e82cbf675c7ce12d42d36775ac77d09354e73b1198`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:09:22 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:09:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:09:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_VERSION=8.3.9
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:09:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:09:22 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_VERSION=2.2.24
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75477805297b2e5d3e45445d2b14ef5781642095163a9180372584156228308d`  
		Last Modified: Fri, 21 Jun 2024 03:29:15 GMT  
		Size: 3.4 MB (3390439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f052e2934ece7510f678f44b5c8af4ca01c8c831d77f69244bf017c94d869629`  
		Last Modified: Fri, 21 Jun 2024 03:29:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb6c1f73b878cfca599e88261cc519ca171226efafcdd1238320261b2c41459`  
		Last Modified: Fri, 21 Jun 2024 03:29:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad21bcd5e01b3577ee096334abb0b82ac82b0ad714a3472334b880acded40b5d`  
		Last Modified: Sat, 06 Jul 2024 05:59:20 GMT  
		Size: 12.5 MB (12491140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0ccc4a872dd64ec2b263124dface57c654f9ca9f8c5d7c7d20b7c047b6690a`  
		Last Modified: Sat, 06 Jul 2024 05:59:14 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a946a846a78b5a891be526ae6a8f998392d67c3a9a12e4e6fa34ef064b858968`  
		Last Modified: Sat, 06 Jul 2024 05:59:32 GMT  
		Size: 19.8 MB (19752182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e55d7045ebfe0e593d2ecbcea723c350cde9d067691c1dd8c88032ece45a15`  
		Last Modified: Sat, 06 Jul 2024 05:59:15 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad7a5af7803e4fc91805f727128d733f63e4cfb6eb0293627add140330a9de`  
		Last Modified: Sat, 06 Jul 2024 05:59:15 GMT  
		Size: 19.5 KB (19483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed5eb72e651834ba7a0408714d377898a334877c985c8f916e688284d832227`  
		Last Modified: Sat, 06 Jul 2024 17:54:29 GMT  
		Size: 31.1 MB (31084722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dac5b5f31c5cdb1f08008c952aaa4c1de35abe739e09a58fc7b70f3c1f534c`  
		Last Modified: Sat, 06 Jul 2024 17:54:26 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de98b455d04fccafd36b162ce8649f0ab260772ad222f6606bf1b9445f474afa`  
		Last Modified: Sat, 06 Jul 2024 18:18:10 GMT  
		Size: 813.3 KB (813254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53375dac536a366c1a4ceff6256968279afbe69c2763a38ff3aa59e2051fb8b0`  
		Last Modified: Sat, 06 Jul 2024 18:18:09 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4871e2ce58d2ee3b39c46ae1ccd638ecce5c9e59f6b4258cd1bf614c94170bf`  
		Last Modified: Sat, 06 Jul 2024 18:17:51 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:f61e91288392925e9dbe3947e9cbf30d78ba8b9a1eee655b8a5c9e230780321f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b713c02e687e620313816fe53c7748e25ae0e3835acb680acc2c5121c967b1`

```dockerfile
```

-	Layers:
	-	`sha256:e26e42765bb5e1764bfc8c64c3b766d3b1d2115c20300049f9deba83e0b38b47`  
		Last Modified: Sat, 06 Jul 2024 18:18:09 GMT  
		Size: 2.1 MB (2130239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c097c2f9a04e8ba3453e2c5f833c12d1efd8527260ca1776453b0199fd097a5`  
		Last Modified: Sat, 06 Jul 2024 18:18:09 GMT  
		Size: 30.9 KB (30854 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; s390x

```console
$ docker pull composer@sha256:6ac269ff0af1b79903e1d8f8e5f4d6f3841cb25c2bd615f53846a89c72009d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69158624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c7f75973531585e13f06883b42f74f4617aa30132a786f3434a11838862dad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 11 Jun 2024 08:09:22 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 11 Jun 2024 08:09:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Jun 2024 08:09:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_VERSION=8.3.9
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Tue, 11 Jun 2024 08:09:22 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jun 2024 08:09:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jun 2024 08:09:22 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jun 2024 08:09:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jun 2024 08:09:22 GMT
CMD ["php" "-a"]
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 11 Jun 2024 08:09:22 GMT
ENV COMPOSER_VERSION=2.2.24
# Tue, 11 Jun 2024 08:09:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 11 Jun 2024 08:09:22 GMT
WORKDIR /app
# Tue, 11 Jun 2024 08:09:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Jun 2024 08:09:22 GMT
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
	-	`sha256:ef0798d5d0f94584ef0fd49afb25bb51d262348b1d10f193e292b75236019b40`  
		Last Modified: Tue, 23 Jul 2024 00:58:32 GMT  
		Size: 12.5 MB (12491136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a87fcaab65a2d28ba5531aea62a826c3c223da11c8ca853aca5f13a7e620383`  
		Last Modified: Tue, 23 Jul 2024 00:58:32 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d8b069ed1e3207579871ea6842ba029cce691c77ce2565d35108d0216908fb`  
		Last Modified: Tue, 23 Jul 2024 00:58:36 GMT  
		Size: 17.3 MB (17285732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b473ea99cf2baddaba6cb4d8302f135758ea4d4fa336e9fdee162419b200b209`  
		Last Modified: Tue, 23 Jul 2024 00:58:32 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bbdba5627ce4b62b0bd187d5b667be462350fb4884a28809fe61d19c50bc29`  
		Last Modified: Tue, 23 Jul 2024 00:58:32 GMT  
		Size: 19.5 KB (19486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8e09afbda672e1ab7f873a7e1f92ddf42ebfa454db278199a14ee779589537`  
		Last Modified: Tue, 23 Jul 2024 08:24:38 GMT  
		Size: 31.6 MB (31611532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12a55d5aa26de21723c5332dad990cfba3657088fde888f43a63109d2e30525`  
		Last Modified: Tue, 23 Jul 2024 08:24:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c5621702785901d242d017c8acd71aadc5ce235bbbd30b08c8e4c7f09177af`  
		Last Modified: Tue, 23 Jul 2024 08:30:27 GMT  
		Size: 817.0 KB (817044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d7266d4d411c82510317eed75cb64d6a75ef370ffcf770968ea4fdf03adc2f`  
		Last Modified: Tue, 23 Jul 2024 08:30:27 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad9d73a23e58bb55ddfdc9499e7ff71b012e478ca2f0d86400d5cf89904f1fb`  
		Last Modified: Tue, 23 Jul 2024 08:30:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:a0309ee3110c89afc0ddd8416c9cf7afe06927a1a0a464a27a4304cfffff4b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2175957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626e9435a87be4a41079b28daef478b97a39f1995053c3f1a79df1a550de6252`

```dockerfile
```

-	Layers:
	-	`sha256:2e13f3ced92ac3ce7cd4148b9035e7f735809a64299d28da207489229d694dcb`  
		Last Modified: Tue, 23 Jul 2024 08:30:27 GMT  
		Size: 2.1 MB (2145139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08b859f7a27334225804a31f23c082cedfe6fca9285e6fe9f7a16e3f070d4946`  
		Last Modified: Tue, 23 Jul 2024 08:30:27 GMT  
		Size: 30.8 KB (30818 bytes)  
		MIME: application/vnd.in-toto+json
