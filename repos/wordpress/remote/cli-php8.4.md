## `wordpress:cli-php8.4`

```console
$ docker pull wordpress@sha256:6aa6b0c3ca4ce4944db0c9e56587f164356e13f1085bafbb08706d8e64011fec
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

### `wordpress:cli-php8.4` - linux; amd64

```console
$ docker pull wordpress@sha256:191ba07e1f7dd2c60d6c1ed07147cec244c422850bdf4e84035cd19b82d87797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70556198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2be229f3d00a5a96355f89f39758b86848e6919b768bd3946301445245e7bf`
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
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.4.13
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:01c2a936c44a3f90ca9bb77c75706af43b3d2f44ed6ede4e171329a78a790db6`  
		Last Modified: Thu, 25 Sep 2025 21:18:05 GMT  
		Size: 5.9 MB (5928419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e20bee4789b3efba3eb9880aeaaf4c13e6263cd79978da3db73d0c25127be8`  
		Last Modified: Thu, 25 Sep 2025 21:18:04 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103731ea806d2baabba81246429d8da0b3c89d8ad9856bf92415acd5f9c80d15`  
		Last Modified: Thu, 25 Sep 2025 21:18:04 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f34de792613dd7edf3c6766483248c2fe987230e18957bec472a65d5023ec4f`  
		Last Modified: Thu, 25 Sep 2025 21:18:05 GMT  
		Size: 13.7 MB (13667225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34ce04f95166a53d64e0a20ba204ef7b91ef4c3507f5e200fb6ef60eed0a24f`  
		Last Modified: Thu, 25 Sep 2025 21:18:04 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e85efba01306816714aefb1d018a4f07a989049e5ea7fec8bc3cf2e9ea732ca`  
		Last Modified: Thu, 25 Sep 2025 21:18:06 GMT  
		Size: 20.0 MB (19953079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3fa80949cbcc4888a1e2cb3f866086f5a7fc49dbc12df17e6db2ea06b1a0d4`  
		Last Modified: Thu, 25 Sep 2025 21:18:04 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fe723748b5fa36ef1dc7d2400ff6536108dff6ce8d3baa2e175a82b9156cd5`  
		Last Modified: Thu, 25 Sep 2025 21:18:04 GMT  
		Size: 20.0 KB (19957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585a1c45dbded911fac84d7d7b4cc920931f87d41bc5353ae28a4bbc65f7356d`  
		Last Modified: Thu, 25 Sep 2025 21:18:04 GMT  
		Size: 19.9 KB (19944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59847c131056157d45ca80c03e3fd65c908ef613834d975f5b362b1e9c2ba526`  
		Last Modified: Thu, 25 Sep 2025 22:12:58 GMT  
		Size: 11.1 MB (11076364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1585eedac2081547d937a29e8cf4ec4be8d3b5404f6757b1277f042f0241467`  
		Last Modified: Thu, 25 Sep 2025 22:12:56 GMT  
		Size: 14.6 MB (14561586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00f883c94ca72fc9b76d9b82f4d8ff5ae4b589216d3981cd4ec10356c179c77`  
		Last Modified: Thu, 25 Sep 2025 22:12:55 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d325b9b31d9406a6a1c9ff2b6552ecca13a91567651281b80025cb6b9f020db4`  
		Last Modified: Thu, 25 Sep 2025 22:12:55 GMT  
		Size: 1.5 MB (1525000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedabccc4d6b215b762031a165ffc2118d69e338c5280ff7ad0db50597f152d5`  
		Last Modified: Thu, 25 Sep 2025 22:12:55 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:744b6669ecb82ac0dc984731540fb8cec663c144529c292e0ae21e9b21511aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.4 KB (637356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b8a90e2e862ce173ade72b511a238266e979ed3f9256f5aa40691079e31429`

```dockerfile
```

-	Layers:
	-	`sha256:2aaf5f72dec5cf87310acb185fb28bd7fddd88aab40d4355cdd48bc8a46aad11`  
		Last Modified: Fri, 26 Sep 2025 01:16:26 GMT  
		Size: 595.3 KB (595274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3b750b72befe8bd0c5ca47466fcdd1c5d6a69cbd13274a22511099e6d07b71`  
		Last Modified: Fri, 26 Sep 2025 01:16:27 GMT  
		Size: 42.1 KB (42082 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.4` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:346d0a26ef650adc900e7473bbfef78faa87bcc53c5bd4132298710ec081a2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64608129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96cc8fdde531fd1a02c6af1206bc5e5027f2f482e2e63fe0186075b023790c2f`
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
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.4.13
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:0fd09a08e7ae23c77a346f98490dc9a93aa7619b29e0da6004f45067b309f868`  
		Last Modified: Thu, 25 Sep 2025 21:24:16 GMT  
		Size: 5.5 MB (5532146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ca2b81b6487deabfda220be61cddbf420c57d23eadfd158c8e507e436298bf`  
		Last Modified: Thu, 25 Sep 2025 21:24:16 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2d111b1e5dd7470e5c2bbea737ee759887649d96bd552d10e916c97db5abce`  
		Last Modified: Thu, 25 Sep 2025 21:24:15 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2582584a0acae70db7f889e20dc84c4119374967dc732f38631574cbdf48ec`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 13.7 MB (13667211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c98c83b217968bd586f2d78bf5419a8f85f0687781ec5849db4a081a234283f`  
		Last Modified: Thu, 25 Sep 2025 21:24:16 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cc377747602b8b554f2259c0c3af06454fe925206218ca22735faa88090d5e`  
		Last Modified: Thu, 25 Sep 2025 21:24:18 GMT  
		Size: 18.1 MB (18061226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f599a6afaf9545b123598fb95102ae946c30ad36c2e4f9d6e32a75e38b4153b1`  
		Last Modified: Thu, 25 Sep 2025 21:24:16 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47803ddc2db992bf692b562a08f786e8b8d7c3e5aac1221e2ae3564edc4c86c5`  
		Last Modified: Thu, 25 Sep 2025 21:24:17 GMT  
		Size: 19.7 KB (19733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8a0481bd982dd27026ecf9bec57d20e786b1f0580456611cee2c74b934b294`  
		Last Modified: Thu, 25 Sep 2025 21:24:18 GMT  
		Size: 19.7 KB (19730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f361c97f535ffbf8d21a3940a02aa232e432698eeff241a0436c13aea972d2f`  
		Last Modified: Thu, 25 Sep 2025 23:06:35 GMT  
		Size: 10.8 MB (10775178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bb8f196268093c1add257fc506caff28c7a12903651ab77de89be4460b75bf`  
		Last Modified: Thu, 25 Sep 2025 23:06:34 GMT  
		Size: 11.5 MB (11502048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ad73abff3de842b00522afdb44b4b61fd5413e62cbddc942087b71c5ab3bd0`  
		Last Modified: Thu, 25 Sep 2025 23:06:33 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1c168a14e240730d02274fe4c1e92491a1b5a253fb2eaba417caf4fb2f6b26`  
		Last Modified: Thu, 25 Sep 2025 23:06:33 GMT  
		Size: 1.5 MB (1525003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beae36dc58f628db3c71310512e74c7434910d6bfd53e0d0230bc919740c456e`  
		Last Modified: Thu, 25 Sep 2025 23:06:33 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:16b16b7d0d709e7852cffbd6d5deb7becf453da29709a52498cea6ecf7d5b6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 KB (42000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807c78ce296b7e39ef26a86eb457a67ba3a05afd12da24d7fd8391165a3f7ad6`

```dockerfile
```

-	Layers:
	-	`sha256:8cf6877f9fafdbe9358b62bb102d91f0419f6f4e49eeb0433860dcf35d028a38`  
		Last Modified: Fri, 26 Sep 2025 01:16:30 GMT  
		Size: 42.0 KB (42000 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.4` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:446e5df57a222e3230b7fa129c27516f4c78fac528a2f85aa3058f4ba41ea256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63462694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61e4b9c3d0b686c3e5b82853368ff1a72a3a442f90ffbb9771ef58336473e82`
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
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.4.13
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:c0ef01fcfdd81544962f52d1296ff7005ef278a0a5371204d8be529ad6dff7d8`  
		Last Modified: Thu, 25 Sep 2025 21:24:10 GMT  
		Size: 5.2 MB (5180930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2f09e837701e70a2c802ed277086e62090638c577442184ed7833eaa6a2553`  
		Last Modified: Thu, 25 Sep 2025 21:24:08 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785795fec154feea6a5a87ef118bc10303547523c70c312098aaace4b6759ab8`  
		Last Modified: Thu, 25 Sep 2025 21:24:08 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b4562f9188b70feacf2ed27be01a27d2c63497c40132611eb5a8ed637eb0a7`  
		Last Modified: Thu, 25 Sep 2025 21:24:09 GMT  
		Size: 13.7 MB (13667207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e22a95aaf38d25c9cf9b5fd68f3cb5ee8b6e894f3c143aad26de024ef1afee3`  
		Last Modified: Thu, 25 Sep 2025 21:24:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3362f22ea6fbee659e43f98af9fbf4147b20771fba0d73d00cb3976c8086f626`  
		Last Modified: Thu, 25 Sep 2025 21:24:10 GMT  
		Size: 17.0 MB (17046725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f640effe716c26ce15e6574f6e26e4566c86b3306fc66dcad66e17fb1103d`  
		Last Modified: Thu, 25 Sep 2025 21:24:08 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc6d31f2e4c375f33378f56b58a952e46b391be5f76b26d6a9eed865668812`  
		Last Modified: Thu, 25 Sep 2025 21:24:08 GMT  
		Size: 19.7 KB (19726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13877332dc17fb5f31c0918a0950987759b9f5cc822da2df7c5201130f1612b0`  
		Last Modified: Thu, 25 Sep 2025 21:24:08 GMT  
		Size: 19.7 KB (19719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1152dd09ce7bdec2372258b3e37f984421d37d2fd2ab8194c8bc38ac636b76`  
		Last Modified: Thu, 25 Sep 2025 22:17:57 GMT  
		Size: 10.4 MB (10446888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e768b741007cf7e6802ef4db8481097a234a425f0c5770ad4bad41c4344fd64`  
		Last Modified: Thu, 25 Sep 2025 22:17:58 GMT  
		Size: 12.3 MB (12332531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b904e1293828e9163d0d4e909fc160bfe761878db62e913f97aa73c6b6c4b1`  
		Last Modified: Thu, 25 Sep 2025 22:17:56 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1e94624b71e524d5a996d830fff8f6a6b371e160372e005500aeb11c8851a`  
		Last Modified: Thu, 25 Sep 2025 22:17:56 GMT  
		Size: 1.5 MB (1524996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457946d08a25116edf44805a9a2679359b4dd0d2e3beab805611800ce1d2398`  
		Last Modified: Thu, 25 Sep 2025 22:17:55 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:0c32318b5b99158ef4a46527a580f86704878955f83023c545fd503eec63ecd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.3 KB (636281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc99dd344dddfb5931b284f3b58072cec07bfec5bfa29f5522e1ebc29f21a7b5`

```dockerfile
```

-	Layers:
	-	`sha256:dd6490dcfb1abe806c7200a88266102636b9816f82ad3d9dab3252f9b91a6010`  
		Last Modified: Fri, 26 Sep 2025 01:16:33 GMT  
		Size: 594.1 KB (594066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f2d4bfa70f497a19712adcc3e9a19421bed749fc7975054e7edfeb097a0dd0c`  
		Last Modified: Fri, 26 Sep 2025 01:16:35 GMT  
		Size: 42.2 KB (42215 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.4` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:93f6c533ffc2f0db1c6c370356468e75a6a03b979591d87c0c7c20ce728827d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70420498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0346d1d7757188733ba0cae9ce9068e83045f9d840cb5647a68f64aaa21f4874`
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
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.4.13
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:ba8c7b2e9c217784e61b3c0ddb6b4e26fdb133bf2f34e672bd485cb10dd58757`  
		Last Modified: Thu, 25 Sep 2025 21:16:16 GMT  
		Size: 6.2 MB (6228299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde80131a1962dbd6d57b20933c4648d46cb0bb76e4ad6b54de65c2d6227749d`  
		Last Modified: Thu, 25 Sep 2025 21:16:16 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd787753b28919747a6ca2ac47ca1f5bae696309b63f8be4da507cf6681439`  
		Last Modified: Thu, 25 Sep 2025 21:16:16 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73fdb35f594ed257b49c4a666fc7dfb05289b41771ead420baa3c20c25c986a`  
		Last Modified: Thu, 25 Sep 2025 21:16:17 GMT  
		Size: 13.7 MB (13667214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48193100f3dd3d5c046113859b2ab492b66451f5faa0f4b2e7c9f9f200bd023b`  
		Last Modified: Thu, 25 Sep 2025 21:16:16 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f47452b946469b77ef895a0c46efaca1b0957aad7c7f568728c81aa4bbe859a`  
		Last Modified: Thu, 25 Sep 2025 21:16:22 GMT  
		Size: 19.5 MB (19501217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c20e27e5283c45c9d98786db88a169b3d6a0967f50f91d19b372d3eb47c28f9`  
		Last Modified: Thu, 25 Sep 2025 21:16:16 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0fc3a77a24e631ed41af821f3dab1a0b4d9a3e811cd1ce25ec3c988b203b85`  
		Last Modified: Thu, 25 Sep 2025 21:16:16 GMT  
		Size: 19.7 KB (19748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394c37dc426f092c33723bfe5af85ca3b1dcde4616898abcefc61270b98213a3`  
		Last Modified: Thu, 25 Sep 2025 21:16:17 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c570741eab6a54c25ac2d80b29d4e78da90ab91b3176c172ce9acc879b6d1c0b`  
		Last Modified: Thu, 25 Sep 2025 22:12:59 GMT  
		Size: 11.1 MB (11080192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9ba0fe4f9c3367f71a89181bcac4e8da74b50b5ddf85b191a34b04a15c5cba`  
		Last Modified: Thu, 25 Sep 2025 22:13:00 GMT  
		Size: 14.2 MB (14243411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0d16e32d8644460bd96af2c30a542f1242217efaccaad6c8e0e307e4577295`  
		Last Modified: Thu, 25 Sep 2025 22:12:59 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97789377d929abd5b7c1ad009f9c097312393e729883ae8c0a22621545de2b8`  
		Last Modified: Thu, 25 Sep 2025 22:12:59 GMT  
		Size: 1.5 MB (1524985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11f5c73e45993ad9041a218c634d61c077f726055976666922d4ca990bebce5`  
		Last Modified: Thu, 25 Sep 2025 22:12:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:ca032556e94f5ed12d1e826dd936968e99e3b995a7637a72614e2160db919b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.3 KB (636333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92729b0e3b7096d418871afbae6a985b78e2300729807bdb21a009dd9027562c`

```dockerfile
```

-	Layers:
	-	`sha256:e5a295a4fb546423d62c06218b4bc3cff2e4fcb08929891347c47f9fa3bb00d9`  
		Last Modified: Fri, 26 Sep 2025 01:16:38 GMT  
		Size: 594.1 KB (594086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:736132e0de15dcde5a175b8e6d3dec263282e858a91fa2f7b1a979ae24e4c78b`  
		Last Modified: Fri, 26 Sep 2025 01:16:39 GMT  
		Size: 42.2 KB (42247 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.4` - linux; 386

```console
$ docker pull wordpress@sha256:18d9f2c1682d7522c3ecac3b2141d723529963df874621cdcfb419f6f3bc4365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69797915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171e95e72bcd47ced24b78a036ae842fc9be11bee9031a67aded884d9681fb99`
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
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.4.13
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:332bbff38a1e31cdb20e66cd96b6a5b08d6387b1d3d9b058c12db5ffd401b33d`  
		Last Modified: Thu, 25 Sep 2025 21:19:00 GMT  
		Size: 5.8 MB (5794092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fce9b7b48fe4d9091443c377dece5d044c9d041ed44cf3b4e58af1583102f5`  
		Last Modified: Thu, 25 Sep 2025 21:18:59 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534d94fbedd306099ec13c6fa95796a0e3c7edb14e786fea7c962e9d57939e82`  
		Last Modified: Thu, 25 Sep 2025 21:18:59 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065783a28d08e93267bef06fdae9d8136d2b2ef95c7dd9937951c88b1761376f`  
		Last Modified: Thu, 25 Sep 2025 21:19:00 GMT  
		Size: 13.7 MB (13667218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418bed6d3ee75d62fd239cee84136cf186c3dd8e7970b735d30cfb7d6b0f3fa4`  
		Last Modified: Thu, 25 Sep 2025 21:18:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0797cadb17bdd7b3693738f2a6572e161695f6a3d3336e82dba36b360b0fd3b9`  
		Last Modified: Thu, 25 Sep 2025 21:19:04 GMT  
		Size: 20.5 MB (20481834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cd29a4a0ac3d8310bc66a3d3ede08b40bfb2d9567023c8f1c391cedc586d1f`  
		Last Modified: Thu, 25 Sep 2025 21:18:59 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f9b8cf276fc5686128892f5695aa8d72c5db4f84366dfc128b99ffbefcef12`  
		Last Modified: Thu, 25 Sep 2025 21:18:59 GMT  
		Size: 19.9 KB (19931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba92da4e721cb04cda9898bb953d8405540f7fc004957407bb1772de783bc45`  
		Last Modified: Thu, 25 Sep 2025 21:18:59 GMT  
		Size: 19.9 KB (19923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba3b9f3c1a1afe55bbc577ee339133c2fbc2e23fa5420c1fe11ca09f4cb0b9d`  
		Last Modified: Thu, 25 Sep 2025 22:12:58 GMT  
		Size: 11.3 MB (11274822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddbaef27d198b84d4569060000f82d56b873db768eedec62e57e274a67eef90`  
		Last Modified: Thu, 25 Sep 2025 22:12:59 GMT  
		Size: 13.4 MB (13395173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618082817a4d4fca65ae75b28761ce5330e2c7dffdd226ae31b31a97719ac395`  
		Last Modified: Thu, 25 Sep 2025 22:12:58 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7a6b1fce14a805319e230863573be1373b319d8640ab015cd1185d6feec7b5`  
		Last Modified: Thu, 25 Sep 2025 22:12:58 GMT  
		Size: 1.5 MB (1524981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0e4b6961797b06fe4ed5984a986628e4a6d0574bc61dee77493be68e115ec9`  
		Last Modified: Thu, 25 Sep 2025 22:12:58 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:f7cf5fd14e87d706b58182f25d02a73eabad1dcf116038601eae7b819be70990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.3 KB (637292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c23a54fcc1ff8fd9af3b0aeef942fbba1d2ace944b52af121119795a2feab2`

```dockerfile
```

-	Layers:
	-	`sha256:85577ccda24e5c29bbf00bb11c0d50383a9de90d68f74eaf8a7ed83f0e587ef2`  
		Last Modified: Fri, 26 Sep 2025 01:16:42 GMT  
		Size: 595.2 KB (595249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:795a603e77b9ca2594312c8694e3fc7c2833f1c9d9343b3120acaa00de893f9d`  
		Last Modified: Fri, 26 Sep 2025 01:16:43 GMT  
		Size: 42.0 KB (42043 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.4` - linux; ppc64le

```console
$ docker pull wordpress@sha256:46ba11c458caa0fe606d07d0db2fead075517fb4631114815bc718549fbae1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72096090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec2e7f056665272c3177cec183b5a7343f8cb44d8694f737f0e074ef93e3d1b`
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
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.4.13
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:b2d165415cc65159456128153815546067ca89254c2ee16739d9a593915c2bbe`  
		Last Modified: Thu, 25 Sep 2025 21:50:59 GMT  
		Size: 13.7 MB (13667229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf9d58c2d24e175afe73c83186c70a54653d4a7a9e169b42a187588df2f087e`  
		Last Modified: Thu, 25 Sep 2025 21:50:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c6b86280f0d78ca867fdc85683b4bd147d316f6690434860270cded233fe23`  
		Last Modified: Thu, 25 Sep 2025 21:51:00 GMT  
		Size: 23.7 MB (23658979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a03266532d2f40547f2998637ec30ab8daead8d5647cda1092bf759010e726`  
		Last Modified: Thu, 25 Sep 2025 21:50:55 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68735b727384e36cb229e8a569527bed6d29607ef0fcc184b9ec6245142bbaaa`  
		Last Modified: Thu, 25 Sep 2025 21:50:53 GMT  
		Size: 19.7 KB (19739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a327693df1b9b6206d9f570299a84275c02003ba38d4a91e11c142da596913b`  
		Last Modified: Thu, 25 Sep 2025 21:50:53 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d402bd14acb14abd534182de71670ae108ffeb0564bf085d2a161198f9b67526`  
		Last Modified: Thu, 25 Sep 2025 22:24:53 GMT  
		Size: 11.7 MB (11689374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a4df2d0e82b8802737ca3c5d625183f04d44fb2eb797cf18640faf7798c52e`  
		Last Modified: Thu, 25 Sep 2025 22:24:53 GMT  
		Size: 14.2 MB (14172784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64d460a9139e1bfe587f08d0b42d325b9c858a67d96dca1b467a224cc00fb2a`  
		Last Modified: Thu, 25 Sep 2025 22:24:52 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbc678f2d13c7c7a1429148d0888aa9ab7589a4715c13dd2685ed9afe09f85a`  
		Last Modified: Thu, 25 Sep 2025 22:24:52 GMT  
		Size: 1.5 MB (1525003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c07e5de0e2b2b638fa100942153493133207d5b7cee15016166de9160048e3`  
		Last Modified: Thu, 25 Sep 2025 22:24:52 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:f458fd8a6ac5a0ff1ee708b756940eda38590d0354e6dbf0a32a86be496f2b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a97fc2de157ff16dc2b4030572d3cc3770ece81710dc2bca3881998e25f532`

```dockerfile
```

-	Layers:
	-	`sha256:07ecb7f0e3675dbd1706fcfb0d7667c0b48ce57b9295e29f7a97d45963a0904f`  
		Last Modified: Fri, 26 Sep 2025 01:16:46 GMT  
		Size: 592.1 KB (592113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a2a4c3fdb3b8cb4bcbaae07f5644c1fb3410b0d92d305438289c8357a796368`  
		Last Modified: Fri, 26 Sep 2025 01:16:47 GMT  
		Size: 42.1 KB (42135 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.4` - linux; riscv64

```console
$ docker pull wordpress@sha256:a27728f31255261b378ca6dde508d7a71de3dc8f0e21a64cc15d9d3afc27aec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67824895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247ea81e87a30683813447a75fcaff3c61e9250303f59c990a45875fca7c61ba`
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
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.4.13
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:ce54772840e390ce79b2bd312dffccae5a0404b88de7d2cec073f06bfc4a7447`  
		Last Modified: Fri, 26 Sep 2025 06:57:14 GMT  
		Size: 13.7 MB (13667214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f6b22cf755134f26369ac0039e67fee0e571a02ceb8a94e09289af33125353`  
		Last Modified: Fri, 26 Sep 2025 06:57:12 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac0365b3ab37d3f9b715bd780ad485c95ad15ed5c5b1c3bfd8970387dd36daf`  
		Last Modified: Fri, 26 Sep 2025 06:57:18 GMT  
		Size: 22.0 MB (21981498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b317aeae2dc6ed4a866738e3dcf9f1437efcbb8375680cb0494c81ae062b0a`  
		Last Modified: Fri, 26 Sep 2025 06:57:15 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf49bc5c019b48fa352706ee9f2a45f3f399db6053ebef12e34dc331889673`  
		Last Modified: Fri, 26 Sep 2025 06:57:15 GMT  
		Size: 19.7 KB (19742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f239dc1f19e52fdc0efc9ea8ed3770da45c53b5f01033f7ed075a4ca9389f8`  
		Last Modified: Fri, 26 Sep 2025 06:57:09 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9b395b32889f27c99b48c03d1a4b8eed7784233551a6bd40642aecd87a1689`  
		Last Modified: Fri, 26 Sep 2025 22:16:28 GMT  
		Size: 11.6 MB (11571410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6756aac351c5d98a5e6a9a94bdd32cdaa59b4f2f7f3354d07896917e04f1760b`  
		Last Modified: Fri, 26 Sep 2025 22:16:28 GMT  
		Size: 11.9 MB (11928357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df04b31673eb7305d1f3cad257f47f2be00262f9b5612f53d517503e27edebc9`  
		Last Modified: Fri, 26 Sep 2025 22:16:27 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9403d7649fc088591c9062a7dbc0ef3f38343c25fbfd576f07546a554befd`  
		Last Modified: Fri, 26 Sep 2025 22:16:27 GMT  
		Size: 1.5 MB (1525010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc4d054a792d114db0210d995653c54d87c236d167c1463289a4fe342643380`  
		Last Modified: Fri, 26 Sep 2025 22:16:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:198aae35a6425682880d9a6dd1789f06d3a44d151081cd63923943b2e30c9d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0173ffe2bc541318500b80f795be97ec8c82d75ef235344f51558d386054d80d`

```dockerfile
```

-	Layers:
	-	`sha256:5560797be78f8d9610540b05d1e1c68f62eab5a30d444f43d386e1a492b087a2`  
		Last Modified: Sat, 27 Sep 2025 01:15:08 GMT  
		Size: 592.1 KB (592109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:046d9e21b36db4225898c2d71aac9cd8bbb14778ec8b97134662012b7445a4bd`  
		Last Modified: Sat, 27 Sep 2025 01:15:09 GMT  
		Size: 42.1 KB (42135 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-php8.4` - linux; s390x

```console
$ docker pull wordpress@sha256:5a0ac7968cf918e2d26ada53e9b24e28809e698f0c87b1c59927a08d32cf838f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71610627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e01b559d0914f6c039d3f58748a1f21de90d20b94f59f64d9a03609abbdbad0`
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
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.4.13
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
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
	-	`sha256:71a3d587fe45527c5fb9d0f6c3e87577a24ab838aa52feae75c98a13d113ba79`  
		Last Modified: Thu, 25 Sep 2025 21:48:21 GMT  
		Size: 13.7 MB (13667205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777aa7a56f2ffb6e0181fc8c56485409ee3e9cdccb2244fa89a1fb4aee0d3d31`  
		Last Modified: Thu, 25 Sep 2025 21:48:19 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6e447a71c18dfb923b3d4658f94697f99b4f8f9a7b92299e4546daf0e926f1`  
		Last Modified: Thu, 25 Sep 2025 21:48:21 GMT  
		Size: 22.7 MB (22734313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e163e1f49f7cbea36f0daedf566336c2669b7cfe583f6db78f875a6017afa`  
		Last Modified: Thu, 25 Sep 2025 21:48:19 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554b90114c9d70edcb59ea26af2028ec3598be22240434bfba9bf6372499b22d`  
		Last Modified: Thu, 25 Sep 2025 21:48:19 GMT  
		Size: 19.8 KB (19755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac8d5741ab97dd8cd75dd42c45280daab21984e353e1710a0e09c13fd204c39`  
		Last Modified: Thu, 25 Sep 2025 21:48:19 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a87edb285cc5e3e1a978ef09e70a0ec8c4b3368ab50adeb2b9f05e64366e83`  
		Last Modified: Thu, 25 Sep 2025 22:20:14 GMT  
		Size: 12.5 MB (12452192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6df624e04d4049e910edda9f125991c05878c5fc4d1c6a330a0fd3a1e57c0e`  
		Last Modified: Thu, 25 Sep 2025 22:20:14 GMT  
		Size: 13.9 MB (13862637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b499224d705c0f48e68ae25174b959a4935d31f5c838c1e706ecb67e2621dc34`  
		Last Modified: Thu, 25 Sep 2025 22:20:13 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb6b2e9bb6929450554acb13e9b9db8ce25945ed538102cf7a3bf0f4d660b12`  
		Last Modified: Thu, 25 Sep 2025 22:20:14 GMT  
		Size: 1.5 MB (1525001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22205f5ab11d6b48683828e305b2b0f4145abcb22359e8192ea1509ad778cf42`  
		Last Modified: Thu, 25 Sep 2025 22:20:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:218ebd541aff42284a96ab97baf50ba9e03eb24c945a193caa9679bd1ca10f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b34cddf16d3d6f28c6724ca9bec8cedb3a6cd5322ef0e3a89d760b414f1645`

```dockerfile
```

-	Layers:
	-	`sha256:fc20649a2ee7a301c09d250b0923cfb23b9c9f3b2a8b6c026a551e76bfc091ad`  
		Last Modified: Fri, 26 Sep 2025 01:16:53 GMT  
		Size: 592.1 KB (592079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9461099f8f1b36d87288d08ddee164552752c833e254d263c07a7809b2c0bac0`  
		Last Modified: Fri, 26 Sep 2025 01:16:54 GMT  
		Size: 42.1 KB (42083 bytes)  
		MIME: application/vnd.in-toto+json
