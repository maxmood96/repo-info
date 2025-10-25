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
