## `wordpress:cli-2`

```console
$ docker pull wordpress@sha256:d2fb995d5d42c8e9a9240788a0ef722fb0f1ced3cb2f6cf0e8f73b41a6f610b3
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

### `wordpress:cli-2` - linux; amd64

```console
$ docker pull wordpress@sha256:d166fc29eebff059395fb7cb785018ed7eab10bd0277049cc07474d41f24e2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66913418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6334db94d7f4383af64fa9f9eabcdad97d7243533ab60096cb02484e8bef4525`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Wed, 07 May 2025 07:03:15 GMT
CMD ["/bin/sh"]
# Wed, 07 May 2025 07:03:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 May 2025 07:03:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.3.26
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 May 2025 07:03:15 GMT
CMD ["php" "-a"]
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
WORKDIR /var/www/html
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
VOLUME [/var/www/html]
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 May 2025 07:03:15 GMT
USER www-data
# Wed, 07 May 2025 07:03:15 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aeee7cf76f513aab74dd7cea7e27dc715a6367a0bfb0c76e5ecbb0dd809e4cb`  
		Last Modified: Fri, 26 Sep 2025 21:50:01 GMT  
		Size: 5.9 MB (5928418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41f007bd007fe859211afd8b168c8e606b92a2d72df016849134084518e8c75`  
		Last Modified: Fri, 26 Sep 2025 21:50:00 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a84dd800eed477ebae80f27ec7a0a029dd6f8f010d5f7399032f870235b653`  
		Last Modified: Fri, 26 Sep 2025 21:50:01 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4121d5fa6f4853c93f3d3fdd8d13f9d43919846ca228c1107c232de8fc716`  
		Last Modified: Fri, 26 Sep 2025 21:50:02 GMT  
		Size: 12.6 MB (12601923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1378496bf1b1a8afddce882e1a785328be1ea1c331d9d0b56f407a1b5540b31f`  
		Last Modified: Fri, 26 Sep 2025 21:50:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70fa522446172fd354834911f09bcaf4d9e024a0a1c936f8fa4eeb8c5173ca5`  
		Last Modified: Fri, 26 Sep 2025 21:50:03 GMT  
		Size: 17.4 MB (17416779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acc06b90f50e96b523fe79563106028200cece14333dabfadd472cdbeebf20d`  
		Last Modified: Fri, 26 Sep 2025 21:50:01 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e54e05dbe9ab994a1ae0157f5a491322dd312a9ae6e61fd065e038e5cd81a7d`  
		Last Modified: Fri, 26 Sep 2025 21:50:01 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62e540c6453afd9a95c8ba401141dfd853bdd0f2f5e2494abca0d557dfaaccc`  
		Last Modified: Fri, 26 Sep 2025 21:50:01 GMT  
		Size: 20.0 KB (19951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19c3a1caba4a766b24b338d18661b964e23ff867784d61ffa347391c5846b75`  
		Last Modified: Fri, 26 Sep 2025 22:06:16 GMT  
		Size: 11.1 MB (11076341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c14ce4cea423d8486c5e7e1b8d8dfca2df8f2ade4c924180b2747aa4e2ecfd`  
		Last Modified: Fri, 26 Sep 2025 22:06:16 GMT  
		Size: 14.5 MB (14520421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f46034875694dac01ec909572222c5de7c4dda3f9030e3199bc7c61bec9ac05`  
		Last Modified: Fri, 26 Sep 2025 22:06:15 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5974ab6faf9fb138b54c23a7860e128046ba1d5c9546ec0ae366b541eccd11`  
		Last Modified: Fri, 26 Sep 2025 22:06:15 GMT  
		Size: 1.5 MB (1525003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6ff24aa1d1632241999d44de9f9fec61f7b456fc5077be5d3e3e251452af5c`  
		Last Modified: Fri, 26 Sep 2025 22:06:15 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:07a5d0f94922ef074096a24e5757b8cd4a9a1f205e11342702585804db523014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.8 KB (639797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182cec178aac77712a4e6ef6409f071be4aa983042d83e886f1434a1d29f79a9`

```dockerfile
```

-	Layers:
	-	`sha256:696ca37ad7dfb1e59ac518775c6bfac26093676c894396c7b0daacdf00a2e729`  
		Last Modified: Fri, 26 Sep 2025 22:16:18 GMT  
		Size: 596.5 KB (596494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c7915d5bc99ebe7c430d5bae72aa750599a836ac3400c57a098d7dd0c4ca92`  
		Last Modified: Fri, 26 Sep 2025 22:16:18 GMT  
		Size: 43.3 KB (43303 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:d6a6aa6baba384c79d044c6200473a002e5bd67cf99387c1e4be9e29dc6e1ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61229211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc28b9fc6e564db7bfd65cb5c686b14fcf6f5e57adcebd1141d4b3b3dac7bce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Wed, 07 May 2025 07:03:15 GMT
CMD ["/bin/sh"]
# Wed, 07 May 2025 07:03:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 May 2025 07:03:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.3.26
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 May 2025 07:03:15 GMT
CMD ["php" "-a"]
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
WORKDIR /var/www/html
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
VOLUME [/var/www/html]
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 May 2025 07:03:15 GMT
USER www-data
# Wed, 07 May 2025 07:03:15 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e1b9a13d61cedf95e5d0b08495b2c36f3aa09771175bf02ec2411f44c0d529`  
		Last Modified: Fri, 26 Sep 2025 21:47:06 GMT  
		Size: 5.5 MB (5532135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a88ca30a5157e1c0cb6d0f9f87da04027b947f052c99e965d699cdecc7ab32`  
		Last Modified: Fri, 26 Sep 2025 21:47:06 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ef209f8c955c66b6982bae07bb4691c7629717f55fb85b2d54ce2faf45e2f0`  
		Last Modified: Fri, 26 Sep 2025 21:47:06 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8dff08b66b7c9b685b12132016c5adb76e413a18bd7dc350c941374f5c7ca7`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 12.6 MB (12601915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de516d3786f48a2dc27e34ad97ace25f0b28ca8987433c36e3c600a5bf620ac`  
		Last Modified: Fri, 26 Sep 2025 21:47:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c764bdbb2719406ba9205c6ac50d2be8a51c173d65c96c690f9678c82458010b`  
		Last Modified: Fri, 26 Sep 2025 21:47:09 GMT  
		Size: 15.8 MB (15788394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6e9db79c7fb0c9105dffc0a96c9765ab446db7b080a7b8e524e1333d42ca80`  
		Last Modified: Fri, 26 Sep 2025 21:47:06 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d230f4a017bf9d5cb22611faea5ad38c85ff9c1df9d759e60dd0657edf86e32f`  
		Last Modified: Fri, 26 Sep 2025 21:47:06 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5876a358ff0fba583e707c8908e0db1cc93a4edbe5ab4e258e3e739a41e9fb57`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 19.7 KB (19730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18107a54ca8e20bc2d9cb5489135bffed5327eff525b9553bc1c8595ce82fda0`  
		Last Modified: Fri, 26 Sep 2025 21:59:57 GMT  
		Size: 10.8 MB (10775176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1874b15b1dd752221050a65541a7063fd469e8eb5abb71784be3cf9189b686`  
		Last Modified: Fri, 26 Sep 2025 21:59:56 GMT  
		Size: 11.5 MB (11461268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570f02b9caa60663a8b5b6d99fd6435656f906c6cebaeff2a923adcf87c4ad64`  
		Last Modified: Fri, 26 Sep 2025 21:59:56 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707afca2306d4810e91f2d0551cec0fe116c05ca2c180a7c5761100e5aeee205`  
		Last Modified: Fri, 26 Sep 2025 21:59:56 GMT  
		Size: 1.5 MB (1525007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767e21423a0851a0a29d1bf45cef8b47c1c7b78cd0bd1b1ee3be45736781013f`  
		Last Modified: Fri, 26 Sep 2025 21:59:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:c6c31efba1e95e5848502b0ee35141b62b0707ee24829e0c7f225a4f750ae470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 KB (43252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10ca98c988c9eeaa4a6f71cdf8acf8f395ca438eac403cb310c6b894c6f8f6e`

```dockerfile
```

-	Layers:
	-	`sha256:b2bb3be1dc001b9a83f5a4a2f0455f03444293a583e68c0db368580a24ba7d43`  
		Last Modified: Fri, 26 Sep 2025 22:16:22 GMT  
		Size: 43.3 KB (43252 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:3a0cf17daf28b8a221004510f25a355e23669ced1b81519668ee4750addc4429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60176376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9586464881af2979ecbc02c3ab4b82cc7ef902691260ee379864972afab4c610`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Wed, 07 May 2025 07:03:15 GMT
CMD ["/bin/sh"]
# Wed, 07 May 2025 07:03:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 May 2025 07:03:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.3.26
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 May 2025 07:03:15 GMT
CMD ["php" "-a"]
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
WORKDIR /var/www/html
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
VOLUME [/var/www/html]
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 May 2025 07:03:15 GMT
USER www-data
# Wed, 07 May 2025 07:03:15 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a644537de53c237300603db7df4b52f2ae55dc44d2587b538aaa82290be021`  
		Last Modified: Fri, 26 Sep 2025 21:53:54 GMT  
		Size: 5.2 MB (5180927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39615a8f1115d97f30457cec3b66543b8514a5a5f58981138231ded5479e6fde`  
		Last Modified: Fri, 26 Sep 2025 21:53:56 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dccd523bf43c221b16ba7c90a4be683105f0a06f6457c12e2ac3f62898b1dd9`  
		Last Modified: Fri, 26 Sep 2025 21:53:56 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90774f6dcea55e5a85d773b3a4a2d09bfd4f0fd101c3e669858978418cd498c`  
		Last Modified: Fri, 26 Sep 2025 21:53:57 GMT  
		Size: 12.6 MB (12601908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51063e1417b825d64a8c46377479d1dcb5f32b455b90906555a25dc28ca1abac`  
		Last Modified: Fri, 26 Sep 2025 21:53:56 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b578bbffe8f2a31f24919cfb97bd0924b3431be3197e0362dbefd492fbe217`  
		Last Modified: Fri, 26 Sep 2025 21:53:57 GMT  
		Size: 14.9 MB (14857910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9879d80158811068ba4b2c23499821691a9b6fef5ed5510d6560cc5d7fad56ec`  
		Last Modified: Fri, 26 Sep 2025 21:53:56 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4686321160b3849c17a86377b2d3cc230f4ea70f212e87c0c0526cbd99044a`  
		Last Modified: Fri, 26 Sep 2025 21:53:56 GMT  
		Size: 19.7 KB (19724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172914f94aa48641a4f7496b2e2472deee7ffa6e78116c9061054dd7ec703c68`  
		Last Modified: Fri, 26 Sep 2025 21:53:56 GMT  
		Size: 19.7 KB (19718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a64c46a47d12e913241157857f743dfe78449d02295a9c2ba71914b6290e67d`  
		Last Modified: Fri, 26 Sep 2025 22:04:40 GMT  
		Size: 10.4 MB (10446899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e63b667fbcf2e5ea961a6623349b5fa03e73d573a443a9886781876f8a733bb`  
		Last Modified: Fri, 26 Sep 2025 22:04:39 GMT  
		Size: 12.3 MB (12300319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6171b4b381a336212fc8fe8f40660516c69448d16593efb3d8d585ddda0780ea`  
		Last Modified: Fri, 26 Sep 2025 22:04:39 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b554434473996377af3d7a93fd363eeb911d3ae3ad70c28c563c1afee306ed`  
		Last Modified: Fri, 26 Sep 2025 22:04:39 GMT  
		Size: 1.5 MB (1524995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504ad3938719500522be6db4ee5a8879d559d8f1cb87e6fd236a81cee1f12399`  
		Last Modified: Fri, 26 Sep 2025 22:04:38 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:6160fadae1cda53451ae972834f7b08495606f18b21ccb6b9e6c0af73d70f588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.8 KB (638784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca59ad5a37217e456b8adce7c6e7f18aa710f3ea8bb73fa32097530e64e9bd44`

```dockerfile
```

-	Layers:
	-	`sha256:e53f076dea3efa1cee2675a00321e3b0acd0b64a25af475f6c2f61502512b281`  
		Last Modified: Fri, 26 Sep 2025 22:16:25 GMT  
		Size: 595.3 KB (595318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a3a6c8f893b269b1d0e224580262ca740d7c14e5ad8ab7a3c1de13eb0591b48`  
		Last Modified: Fri, 26 Sep 2025 22:16:26 GMT  
		Size: 43.5 KB (43466 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:4dfe1e45c3f1d6fad5cb17e0f33631416ef44829864809c3c85ee5b86eccfbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67145711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ed0379ab82cfb1bd959df14d6818f7d3390ce7a24b1ae7b8f13aad5f9b5220`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Wed, 07 May 2025 07:03:15 GMT
CMD ["/bin/sh"]
# Wed, 07 May 2025 07:03:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 May 2025 07:03:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.3.26
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 May 2025 07:03:15 GMT
CMD ["php" "-a"]
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
WORKDIR /var/www/html
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
VOLUME [/var/www/html]
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 May 2025 07:03:15 GMT
USER www-data
# Wed, 07 May 2025 07:03:15 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded802c0ea972cc42ed42fb53b88fcaa5f76d964b7759f9288f4e49f787c4491`  
		Last Modified: Fri, 26 Sep 2025 21:46:14 GMT  
		Size: 6.2 MB (6228292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef7dce2a0d63dc890c3cb694c6687abcbb2eeb45b7161636806a220bcae820f`  
		Last Modified: Fri, 26 Sep 2025 21:46:01 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226230ca40d99493e29915e165bd77a8210105fd5bd51d717f75fb6493803dc0`  
		Last Modified: Fri, 26 Sep 2025 21:55:39 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cd4a7fb61d556af5284f3eb0689d983f10392c7d59e04a51283caa081205b1`  
		Last Modified: Fri, 26 Sep 2025 21:51:21 GMT  
		Size: 12.6 MB (12601911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868da1e959daa89f11b6f5dbdc4fac3c8f948c86bc9b64d849e8dc467320586c`  
		Last Modified: Fri, 26 Sep 2025 21:51:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8df0989de1dde9a8258afa78b308706f3ea9b56eff32452ccc0b8b068b7dfe7`  
		Last Modified: Fri, 26 Sep 2025 21:51:21 GMT  
		Size: 17.3 MB (17323798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c73bc3e08224ceee41672ca4d28d022c7ecf2fb49446d2666070568d546bb7e`  
		Last Modified: Fri, 26 Sep 2025 21:51:20 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186171df34bb0288e7f5c4a3e26b1c31dd26ce69131ff8e567d6bbc41cc62bfd`  
		Last Modified: Fri, 26 Sep 2025 21:51:20 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a899f1062ee73a1810e827bea7d0d84b42c63d58d8e81ed48e1a7b756f049e`  
		Last Modified: Fri, 26 Sep 2025 21:51:20 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a99ddb73d1d21d330c3590d91a1c3efa02c74770693d6a4268563cee3d5ee6`  
		Last Modified: Fri, 26 Sep 2025 22:00:05 GMT  
		Size: 11.1 MB (11080155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604d1c012874adbc5e0d4d8673497eaa6b8dd6ce3028d3e33c45db8478bf8246`  
		Last Modified: Fri, 26 Sep 2025 22:00:06 GMT  
		Size: 14.2 MB (14211379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980419f23eab3586c69af9cdd83f9d18d66bc98c2d6ddb08d543d3d1bb3def2a`  
		Last Modified: Fri, 26 Sep 2025 22:00:04 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e275b9dd6269e259a957d468e4652bdeed41736081428b00fd7c4687abf637`  
		Last Modified: Fri, 26 Sep 2025 22:00:04 GMT  
		Size: 1.5 MB (1524990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcca80cf0e6ed01c6f091ff858e9e7f1e763708dc3ccff66ce97d75645e53ab`  
		Last Modified: Fri, 26 Sep 2025 22:00:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:b2ac28bf08a272f569866dd316cc8317f24f43190b13c5fb78f3a943b5ffaf51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9229fc6a961d181cde4de76e9d5eccd1b294df2f703a096db177635c548a33c`

```dockerfile
```

-	Layers:
	-	`sha256:ab5d49e28da306d68e6c6bef57632115d35f251400cefb9e57a7c920d483c13b`  
		Last Modified: Fri, 26 Sep 2025 22:16:29 GMT  
		Size: 595.4 KB (595354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b1998b692848da6f5d39017bac65c5a5008700dcf70f5101595072c9077da2`  
		Last Modified: Fri, 26 Sep 2025 22:16:30 GMT  
		Size: 43.5 KB (43515 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2` - linux; 386

```console
$ docker pull wordpress@sha256:937a4197a6f07a70119d6a7bd1debbd78a4ab89f702df6fb19aa1f66fba4c346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66041899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb531c4a9d081196c237c1507bc08926abcf924a71af6421d5cd508c5f69ddf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Wed, 07 May 2025 07:03:15 GMT
CMD ["/bin/sh"]
# Wed, 07 May 2025 07:03:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 May 2025 07:03:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.3.26
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 May 2025 07:03:15 GMT
CMD ["php" "-a"]
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
WORKDIR /var/www/html
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
VOLUME [/var/www/html]
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 May 2025 07:03:15 GMT
USER www-data
# Wed, 07 May 2025 07:03:15 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdced6eceaed50f02defb1a7339429426dda4701a88924ca1a03e911e27f6571`  
		Last Modified: Fri, 26 Sep 2025 21:50:10 GMT  
		Size: 5.8 MB (5794056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691ab2febd6a70b857ce1556185e64535bbd0656e104c6daf8315fc0446fddf9`  
		Last Modified: Fri, 26 Sep 2025 21:50:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0263354f752368eba9207e4c6eec26b353fcaeb927f878cf195bf92cb5edb105`  
		Last Modified: Fri, 26 Sep 2025 21:50:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abc497c8c65be72d09dadd83c3dabd905b209df7d7471c193bdfc4f490c2c27`  
		Last Modified: Fri, 26 Sep 2025 21:50:11 GMT  
		Size: 12.6 MB (12601923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bff974dd7075320f91424bb59578d360cd09182e71379b073a2277e5e833b9e`  
		Last Modified: Fri, 26 Sep 2025 21:50:10 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed686819c401c2c1112e070c07e2efeabeeccb217ad709e88bb1595ada9214e6`  
		Last Modified: Fri, 26 Sep 2025 21:50:12 GMT  
		Size: 17.8 MB (17827157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af391ebe760b23e7fab756d4b70c5b7860bd7b2bd6e34e2e246f9efc922ab50c`  
		Last Modified: Fri, 26 Sep 2025 21:50:10 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8af37e99f884887f41a0ee1fd0470324ecc6352cc34866c89bbf6c0bc93470d`  
		Last Modified: Fri, 26 Sep 2025 21:50:10 GMT  
		Size: 19.9 KB (19931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968122d392a13d447e79f357c948cd15c8686c2f2e1957ba26615ada11c90068`  
		Last Modified: Fri, 26 Sep 2025 21:50:10 GMT  
		Size: 19.9 KB (19928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63e1f846330bbf7fef385becc9faa4c8e5365f4cd2c50de9334dc24e1a4907b`  
		Last Modified: Fri, 26 Sep 2025 22:07:02 GMT  
		Size: 11.3 MB (11274816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb06aa1e7d034c896e6de3346c06a261017c8bb59a105de664baa634730df9c5`  
		Last Modified: Fri, 26 Sep 2025 22:07:01 GMT  
		Size: 13.4 MB (13359166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af5346cff705acae2ee74705ace1ffd6f72c96b223cc031b5d284a622b674d0`  
		Last Modified: Fri, 26 Sep 2025 22:07:00 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93b71f9b3f8d178f0a4f9ccff071aa47b8e2fb6b91e5859d3d91b3d72ba489e`  
		Last Modified: Fri, 26 Sep 2025 22:07:01 GMT  
		Size: 1.5 MB (1524974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501f2bb294370b7c5375dd38aa2aef94e9ee26750eb5a1f50d960510759a2dad`  
		Last Modified: Fri, 26 Sep 2025 22:07:01 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:e47bdf894327c3ba454c9bfaa450e8b8b327636410c749f5b5f9a8472939ce08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.7 KB (639692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc21f6ee57a47dfcec199e56a8ebd7961a714f17b213c5337046501f028c33e`

```dockerfile
```

-	Layers:
	-	`sha256:9878b3dede26f7d9c4a736c4326fa7b6ed02f57bc91042a3bc0b05f71ae3e8bc`  
		Last Modified: Fri, 26 Sep 2025 22:16:34 GMT  
		Size: 596.4 KB (596449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9b7ab3359f6754f84bbaafdee83e7fc632c1123dd7e352c8ec0db18cfab6e7`  
		Last Modified: Fri, 26 Sep 2025 22:16:35 GMT  
		Size: 43.2 KB (43243 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2` - linux; ppc64le

```console
$ docker pull wordpress@sha256:b50fed43e51f99e4c179808dfcba8ef998c5ac9c012c65fc13fc98cad93362c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68400949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc975324b2cb3d6c82828a9ee2a6244953e3d2af060e942f6fbc8d9c6355686`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Wed, 07 May 2025 07:03:15 GMT
CMD ["/bin/sh"]
# Wed, 07 May 2025 07:03:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 May 2025 07:03:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.3.26
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 May 2025 07:03:15 GMT
CMD ["php" "-a"]
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
WORKDIR /var/www/html
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
VOLUME [/var/www/html]
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 May 2025 07:03:15 GMT
USER www-data
# Wed, 07 May 2025 07:03:15 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21cfadffc066033bb3b2fb968e591ebbf95e2cc63d5efec774453f70aac4f9a`  
		Last Modified: Fri, 26 Sep 2025 23:11:15 GMT  
		Size: 12.6 MB (12601928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1c9397d85dd5a6f1894ceb18b3f66da3683fde1099e158db3048f1c9f2c9b0`  
		Last Modified: Fri, 26 Sep 2025 23:11:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc7f8201bb97cb8ac219a01bec1241cef5660d7d0af234f9b1680b1fea05d90`  
		Last Modified: Fri, 26 Sep 2025 23:11:15 GMT  
		Size: 21.1 MB (21065628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fc1c67eaedaf3c1ffc9cf5210a065d822b0e347e8fb7b8d11659b51ec80231`  
		Last Modified: Fri, 26 Sep 2025 23:11:13 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a721ebaa994023dfd2e01dd07a37c241599a10898cbb3866a3dd0321ebfaa6f`  
		Last Modified: Fri, 26 Sep 2025 23:11:13 GMT  
		Size: 19.8 KB (19752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a2a25cb84cba39114a3e6741b720c6c576153230e5af64cf160e0339ad425f`  
		Last Modified: Fri, 26 Sep 2025 23:11:13 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e1721e6e05f5348fcb0646b4659591088cf2b67e3c4dd2db2104017a6bdeb`  
		Last Modified: Sat, 27 Sep 2025 01:39:18 GMT  
		Size: 11.7 MB (11689373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48a96a1d6469b2f7109093d4e85963d7a5a6bf5425e3f4cd5e95e8ddfc1f3b6`  
		Last Modified: Sat, 27 Sep 2025 01:39:17 GMT  
		Size: 14.1 MB (14136281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcf0e276c92661c0bc8eeba5ff1af46ff890f11502c0328d847f2b681eb6e36`  
		Last Modified: Sat, 27 Sep 2025 01:39:17 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259470882987f31d6467f4c032f53ddd96cd27c77a3f060c9c822bca1e8f3674`  
		Last Modified: Sat, 27 Sep 2025 01:39:17 GMT  
		Size: 1.5 MB (1525007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8deca672101c2b2732e713b40c749eee596834f530b5ac2c0e163b8d32ac717`  
		Last Modified: Sat, 27 Sep 2025 01:39:17 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:705fa59df709d02cb1178f8ff2ec4f714bcfa30f2122bedfad14174e1adae6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.7 KB (636736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29a3bc143ddb7339b630ce695e9def1f8bfe5c680ff2c9a598c789deb77ee78`

```dockerfile
```

-	Layers:
	-	`sha256:bac70a1c3fedef5127c5c501997bd5f09ed66c97bf5f3f1abc5c721e47e2f3bb`  
		Last Modified: Sat, 27 Sep 2025 04:14:56 GMT  
		Size: 593.4 KB (593357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a16502050fecde8a2af9b348fe963a99706cf3c2d50e448dea274121c75cd6`  
		Last Modified: Sat, 27 Sep 2025 04:14:57 GMT  
		Size: 43.4 KB (43379 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2` - linux; riscv64

```console
$ docker pull wordpress@sha256:68596bf02f18134858f190eb4cef49042e7d5fd38773a807b9b70b3f8ef1e5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64266886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a8769fce3103723b471ac158ef690116d7d1637c9c61fb2f2440cc63d09fb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Wed, 07 May 2025 07:03:15 GMT
CMD ["/bin/sh"]
# Wed, 07 May 2025 07:03:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 May 2025 07:03:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.3.25
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 May 2025 07:03:15 GMT
CMD ["php" "-a"]
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
WORKDIR /var/www/html
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
VOLUME [/var/www/html]
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 May 2025 07:03:15 GMT
USER www-data
# Wed, 07 May 2025 07:03:15 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96000ef7021911e67902fd12f051a526237f6a40c66c9589b2b5db98f38d845`  
		Last Modified: Fri, 29 Aug 2025 08:42:41 GMT  
		Size: 12.6 MB (12604754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173261600f62a02225c3dd6df60f7d0a44148dbb7c1bf44389ea5f88029aab29`  
		Last Modified: Fri, 29 Aug 2025 08:42:40 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b9657dbaa54f4e1b0584aeddfebff06b8bbe2583e324ad3718f5aaa2e860a8`  
		Last Modified: Fri, 29 Aug 2025 08:42:43 GMT  
		Size: 19.5 MB (19526062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdac6025118200a3b5c10111cce7a28b380a2aa25164d6c306da22d364b91d33`  
		Last Modified: Fri, 29 Aug 2025 08:42:40 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec06af79a33a09cd79af53ada1cf54209e8a2f560dd8c1aaa01bee22a082ba6`  
		Last Modified: Fri, 29 Aug 2025 08:42:40 GMT  
		Size: 19.7 KB (19742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416025736ff387249b72de8b1361ae2bdba8c1268a5c8b2ea09ec1b200882f03`  
		Last Modified: Fri, 29 Aug 2025 08:42:41 GMT  
		Size: 19.7 KB (19734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d8e5e4c98d4c012a6d1a8762bf224e15a791d3f978686fcd85b54a153904f4`  
		Last Modified: Sat, 30 Aug 2025 05:34:35 GMT  
		Size: 11.6 MB (11571378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79f9bf08a47665ac338761079519f7fa774766835063964ce0109b2b0a5d5e7`  
		Last Modified: Sat, 30 Aug 2025 05:34:34 GMT  
		Size: 11.9 MB (11888272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45920590da218b44158c4f32286cc3d8e330e83f616db884f32289c6099667f0`  
		Last Modified: Sat, 30 Aug 2025 05:34:33 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d6bae994002954fed9e010a18d24136080a713f406f5dd4f88abf6fa97c647`  
		Last Modified: Sat, 30 Aug 2025 05:34:33 GMT  
		Size: 1.5 MB (1525010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377508bd99af6b7cf75045d40a3f65e11081e39f6eb04aa129d987f265a3e1d0`  
		Last Modified: Sat, 30 Aug 2025 05:34:33 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:fcdcfd2ff73dc3cacfc8655c72bed5c78c043b4f6a8e268f9a05642e18ce9d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c0d6f851e6c4d3a9e324841250b2dcc362b16e89857245f6b2d123478a9bfb`

```dockerfile
```

-	Layers:
	-	`sha256:1c04036ba8d200a24ab2251a0649c61db7215c5cf58cd63d8d442cd35abe0ddf`  
		Last Modified: Sat, 30 Aug 2025 07:14:34 GMT  
		Size: 592.1 KB (592109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b76aaba090c53906976c8c0956a7ee53c63eaa471d76d42a5f9c343930704f71`  
		Last Modified: Sat, 30 Aug 2025 07:14:35 GMT  
		Size: 42.1 KB (42135 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2` - linux; s390x

```console
$ docker pull wordpress@sha256:bcd7b5a3d565359500cf7a180d09c8a93b22e454b8ef12990ca13fc9b312f3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68026648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8827a350639dd2649bd89379c5d2a14b41efc9363255c7f595f2aa05483590c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Wed, 07 May 2025 07:03:15 GMT
CMD ["/bin/sh"]
# Wed, 07 May 2025 07:03:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 07 May 2025 07:03:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.3.26
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 07 May 2025 07:03:15 GMT
CMD ["php" "-a"]
# Wed, 07 May 2025 07:03:15 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 07 May 2025 07:03:15 GMT
WORKDIR /var/www/html
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 07 May 2025 07:03:15 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 07 May 2025 07:03:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 07 May 2025 07:03:15 GMT
VOLUME [/var/www/html]
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 May 2025 07:03:15 GMT
USER www-data
# Wed, 07 May 2025 07:03:15 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2149689de406e21c39f1da3fa3d9788fda15f8300744f3cedaa8a558d9745e4c`  
		Last Modified: Sat, 27 Sep 2025 00:40:20 GMT  
		Size: 12.6 MB (12601914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17097d343a1adb55100bc03bbbdbeb0a0806e36ecbd3a26baaf26d1377d0d746`  
		Last Modified: Sat, 27 Sep 2025 00:40:18 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080bce12427d8ee32dd0fbcd1173d47d178cd08d7cc4f71684499d2c74bfa28c`  
		Last Modified: Sat, 27 Sep 2025 00:40:20 GMT  
		Size: 20.3 MB (20250629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc68ef85c879af8e20517522d38cfa6e60a1af66127cd59466f9c5b6bc225687`  
		Last Modified: Sat, 27 Sep 2025 00:40:18 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304d94d67eef41f69a122d3f1f1f567c45af7b583a858a88cd96ceef23db9c56`  
		Last Modified: Sat, 27 Sep 2025 00:40:18 GMT  
		Size: 19.8 KB (19752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2ce5b3d25f7b73cad5d1653def575a53345c35bbb12ca99ba93ccd6bc9d640`  
		Last Modified: Sat, 27 Sep 2025 00:40:19 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7265e845d773a5771dabdb8333e6855ba57122f50dec26bf1e4e8d1d4019e7`  
		Last Modified: Sat, 27 Sep 2025 01:23:56 GMT  
		Size: 12.5 MB (12452205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cb2c8861e00dc55f8c41e297dc8456413790d8ca670fd0c083a1785d45fead`  
		Last Modified: Sat, 27 Sep 2025 01:23:57 GMT  
		Size: 13.8 MB (13827626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84f24cdf1e100bc081442949aafc43249549aec793a8ef6028c9c41361615d0`  
		Last Modified: Sat, 27 Sep 2025 01:23:55 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0911e2ee137e3fca584e186e0178ecf933a7377f2d832b945e993d8b88286d4`  
		Last Modified: Sat, 27 Sep 2025 01:23:55 GMT  
		Size: 1.5 MB (1525008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a018f42333af11be8881ebfb0fef98bb3e22169b165a568ce55457c5183304`  
		Last Modified: Sat, 27 Sep 2025 01:23:55 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2` - unknown; unknown

```console
$ docker pull wordpress@sha256:3ae5809aa355ffdbc85015607a3835f8182338a1e74a0319a4d5c7833e830e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.6 KB (636602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc84d7461b497ae1e04f73b8421a36723fbc10a0e026bc25cfcfffdd076b9a2`

```dockerfile
```

-	Layers:
	-	`sha256:f610fcda20120e0000401c5582e3c85429c74a2e79a35a64a56e459e43668249`  
		Last Modified: Sat, 27 Sep 2025 04:15:02 GMT  
		Size: 593.3 KB (593299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56002e964d0a5708be384aca07c2a0bfffe640b7aa7eed7b0baa234deb55366f`  
		Last Modified: Sat, 27 Sep 2025 04:15:02 GMT  
		Size: 43.3 KB (43303 bytes)  
		MIME: application/vnd.in-toto+json
