## `wordpress:cli-2-php8.4`

```console
$ docker pull wordpress@sha256:eecad0b15da1823afb6d4e62d5c50cf4c8971649a55fea8cc57f32d8ae06dcbb
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

### `wordpress:cli-2-php8.4` - linux; amd64

```console
$ docker pull wordpress@sha256:76da9c0560454298e37a8004d1331c9f2345a53398d0a27aad1f54eae3813f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68104460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe73855faf2db57fcc2ab4e7deca6e39f0d4a4f8be9c4aa5e68b4cd6e4942a6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:55:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:55:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:55:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:55:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:55:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:55:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:55:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:55:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:55:35 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 20 Nov 2025 19:55:35 GMT
ENV PHP_VERSION=8.4.15
# Thu, 20 Nov 2025 19:55:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 20 Nov 2025 19:55:35 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 19:55:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 19:55:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:58:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 19:58:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:58:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 19:58:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 19:58:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 19:58:30 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:14:44 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:14:44 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:14:44 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:15:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:15:29 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:15:31 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:15:31 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:15:31 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:15:31 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:15:31 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:15:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:15:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:15:31 GMT
USER www-data
# Tue, 02 Dec 2025 01:15:31 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229a3e1a6c1bc39367a33a230874315337bfb39759a8557524b9353e3bbeb85d`  
		Last Modified: Thu, 20 Nov 2025 19:58:47 GMT  
		Size: 3.5 MB (3463766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d690adaaea67f1a00eba760c8d6f9f380b2e37cbbf4a927448d539ae024de646`  
		Last Modified: Thu, 20 Nov 2025 19:58:46 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0511c4f647ff9a4868905a3465b3fe88402d711a3cf1e35deca2f206e9875bf6`  
		Last Modified: Thu, 20 Nov 2025 19:58:46 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f25306ed21c6523677a8c944dc1f7d4b1052f6de0d4fa40ea01aba7517aca`  
		Last Modified: Thu, 20 Nov 2025 19:58:53 GMT  
		Size: 13.7 MB (13673896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aeb5f2482d0160923c0ab54a840253cb7a9409e27933e274d2ba72cb83a45c`  
		Last Modified: Thu, 20 Nov 2025 19:58:48 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb653f084880b946f5a94bd81a273cef4029853704417bc8e16835c9dd11cf00`  
		Last Modified: Thu, 20 Nov 2025 19:58:50 GMT  
		Size: 20.0 MB (19959126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846f37e4fad72486dbb539eb2d6fd6915f08e92613deee5e6aba6b08aaf278c4`  
		Last Modified: Thu, 20 Nov 2025 19:58:49 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e9e2657a698a552bd9857addaa3aadb7f7bf3ddf2a69c3717cf3f14af45a16`  
		Last Modified: Thu, 20 Nov 2025 19:58:49 GMT  
		Size: 20.1 KB (20083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38da0a06cef7ec9b42851ea60d5899fa2f56a181985c9c11dfe8589fa4616da`  
		Last Modified: Thu, 20 Nov 2025 19:58:49 GMT  
		Size: 20.1 KB (20078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96291ef7a7ec325a2a344e479bc8db8539cd22d026c2894b768318c54ff591d0`  
		Last Modified: Tue, 02 Dec 2025 02:45:53 GMT  
		Size: 11.1 MB (11076285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7db01ebe1a9bdccda6f3e255642fe4943ecfcda7b8c9acc79b96abb7575bf9e`  
		Last Modified: Tue, 02 Dec 2025 02:45:53 GMT  
		Size: 14.6 MB (14558676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0b62c69c1137294a46919de7ac04fd13cc2c47fbbadb2fc1ba3438cc9d7319`  
		Last Modified: Tue, 02 Dec 2025 02:45:51 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59697de6239fb1d8adf8afbb73cedf1aafb156fcd91eea27b494202bca28238`  
		Last Modified: Tue, 02 Dec 2025 02:45:52 GMT  
		Size: 1.5 MB (1525156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df590567e082a6853c73c98e3e2538765cd6516b43d2c67e7f901d2878ceac0c`  
		Last Modified: Tue, 02 Dec 2025 02:45:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:143d94b3ac0958497cb836561eb138cd10c3f625b02850881af5cae12e89092a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358bcdc2a2dc86e25a69b94600e2e57cbcde7c4924b3fe1efe8ca95fc5f16d70`

```dockerfile
```

-	Layers:
	-	`sha256:c0872005a6ec87d7d5e84b5807169ce84e6f55b4aeb73b0456cfac422cf856d9`  
		Last Modified: Tue, 02 Dec 2025 02:34:33 GMT  
		Size: 597.9 KB (597887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aafa8693da64313e8d4f6875d97a5604bec4af11b660bcbb46895caf5785725`  
		Last Modified: Tue, 02 Dec 2025 02:34:34 GMT  
		Size: 42.1 KB (42102 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.4` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:fbad5b082096ffc5ed3307719f7145b0ed4cad22b38fce9946ae5bf8ab095b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62516306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc9798de667e91c8ce045559c8715f2a5669e7efe2ef9f011a0a1bedaf35f38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:49:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:49:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:49:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:49:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:49:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:49:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:49:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:49:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:49:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 20 Nov 2025 19:49:24 GMT
ENV PHP_VERSION=8.4.15
# Thu, 20 Nov 2025 19:49:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 20 Nov 2025 19:49:24 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 19:49:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 19:49:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:52:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 19:52:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:52:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 19:52:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 19:52:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 19:52:25 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:12:28 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:12:28 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:12:28 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:13:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:13:48 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:13:50 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:13:50 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:13:50 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:13:50 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:13:50 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:13:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:13:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:13:50 GMT
USER www-data
# Tue, 02 Dec 2025 01:13:50 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5062dc408f0879fc10f221d4938ce6231f2610813c82c6915a9c7e9d88ec34de`  
		Last Modified: Thu, 20 Nov 2025 19:52:42 GMT  
		Size: 3.4 MB (3428327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685db01c20ce6cfabafd4178e21f2bbe321428a1f73966016134121b47dcda68`  
		Last Modified: Thu, 20 Nov 2025 19:52:42 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee543cb64ed8e191a7ba52f566db0982fd8b549031408cb8e5f151c02c3b5351`  
		Last Modified: Thu, 20 Nov 2025 19:52:43 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad05d9b3383549e63097fb5a9917837f907f94af6c284c02948dc19b6b188669`  
		Last Modified: Thu, 20 Nov 2025 19:52:44 GMT  
		Size: 13.7 MB (13673899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085f355f55e903fc53036e93cfaf2801ae6380a3e450a436d20c810e05c5a1a6`  
		Last Modified: Thu, 20 Nov 2025 19:52:43 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba4f34cef7aa1181c212ace3e99a15056a8f523d11d7444af4e19647a33b66a`  
		Last Modified: Thu, 20 Nov 2025 19:52:45 GMT  
		Size: 18.1 MB (18061217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bab12779ccd9e5f267938d5e5f7b3f605d9d6497d7a93f2357c8cb6da197bc3`  
		Last Modified: Thu, 20 Nov 2025 19:52:44 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb455e8d6fb2ad515748f45fe7167b9fc0661bce4044e9bfc0673c76be9094a`  
		Last Modified: Thu, 20 Nov 2025 19:52:44 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42df69742d399cbcb6787958ed831864625c4f6fbd274f31725fd8cb03ce5252`  
		Last Modified: Thu, 20 Nov 2025 19:52:44 GMT  
		Size: 19.9 KB (19862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210b9f1d89837725a2b24a5e29b1d388f0dc1ac7b27c17c7e9651483fafdcc19`  
		Last Modified: Tue, 02 Dec 2025 01:14:18 GMT  
		Size: 10.8 MB (10776178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24682555c5737eb02e1894806aa9582d585df760b696d151c705c48de77305e4`  
		Last Modified: Tue, 02 Dec 2025 01:14:19 GMT  
		Size: 11.5 MB (11502793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2e8960e43e258ce2c54d9a8aae6dc80791525e3758f064901b1b895948b8a4`  
		Last Modified: Tue, 02 Dec 2025 01:14:18 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3723c6c131c1dd037efacf5ffacd769739ce65fa06a478ac9c11896dbdab2358`  
		Last Modified: Tue, 02 Dec 2025 01:14:18 GMT  
		Size: 1.5 MB (1525138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778ac8a525a2f859346dac6462c0cd3767b1f4e8eda5b3c3a4ea8cc63a0b6898`  
		Last Modified: Tue, 02 Dec 2025 01:14:18 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:bec24e1da47163fe79e1d17c47348f8e27e2f12b86f55201045b217674082335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 KB (42019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def0645c0a763dda33acd93a15d47952a676eb96d51d8d288268658f4b8e1c20`

```dockerfile
```

-	Layers:
	-	`sha256:a9cf15456bb249dbfcb712151a664dfb1e5bee96b3a7318306235a1a72da7eb0`  
		Last Modified: Tue, 02 Dec 2025 02:34:37 GMT  
		Size: 42.0 KB (42019 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.4` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:4ca66fbf0c5cb026ed6c8976878148194ff5fea902d04c3be8ef6fbb8c3d4544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61541179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8548c7511cba2bf0e7c381d2c282935616a660baede5056851e41bb4bf1aef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 20:11:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 20:11:05 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 20:11:05 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 20:11:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:11:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:11:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:11:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:11:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:11:05 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 20 Nov 2025 20:11:05 GMT
ENV PHP_VERSION=8.4.15
# Thu, 20 Nov 2025 20:11:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 20 Nov 2025 20:11:05 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 20:11:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:11:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:14:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:14:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:14:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:14:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:14:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:14:06 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:16:47 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:16:47 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:16:47 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:18:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:18:10 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:18:12 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:18:12 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:18:12 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:18:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:18:12 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:18:12 GMT
USER www-data
# Tue, 02 Dec 2025 01:18:12 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e998fcc3affaf16ff3161f2cc97de159183045d71cdb688f2da680fefc8a6dcf`  
		Last Modified: Thu, 20 Nov 2025 21:01:16 GMT  
		Size: 3.2 MB (3244401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a604b985e14692032785bb0608a474a7ed3116958821344c63bc48a0ec77f658`  
		Last Modified: Thu, 20 Nov 2025 21:01:15 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d8ea969554daf7a434c2738a67951010ccb1aba04ade716f0838e5cf1a03fa`  
		Last Modified: Thu, 20 Nov 2025 21:01:16 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd97ba09d39ee8a138f1096130e96c8caa1b2614f82cff507fb4008f3b3cb6d`  
		Last Modified: Thu, 20 Nov 2025 21:23:34 GMT  
		Size: 13.7 MB (13673889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc62708e29bdb65d0f58231e3cd93428e95306856e08e146677da00b5cc820`  
		Last Modified: Thu, 20 Nov 2025 21:01:15 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8165f336ea8a215f84e4403a88d0caa63437cb060a328c5822606c5387c01a69`  
		Last Modified: Thu, 20 Nov 2025 21:23:33 GMT  
		Size: 17.1 MB (17052568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6909f906d9a1a02942efa5bc1382a043c111138cd607d14c5658ba9295ba9feb`  
		Last Modified: Thu, 20 Nov 2025 21:01:16 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3aa98306d0411aad398c0cd81bec6ee101fc320bdd735f3b37f5025346882ba`  
		Last Modified: Thu, 20 Nov 2025 21:01:15 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1084442b4060ad2fff0b3a75ec780f6204b5672b86166991765b38815f97c166`  
		Last Modified: Thu, 20 Nov 2025 21:01:16 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddb58d21ce9d3f82555555baddc2a36fa02ad1c8e449cd1edd35bb8d56d98e3`  
		Last Modified: Tue, 02 Dec 2025 01:18:31 GMT  
		Size: 10.4 MB (10447537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db993a3f9903b3ccd4635544505a4fb42caf16922cc9921785892a326406554d`  
		Last Modified: Tue, 02 Dec 2025 01:18:32 GMT  
		Size: 12.3 MB (12331456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d790326e836a72e7e9f09156291622472af7e8906deb100a66733bfa97de986`  
		Last Modified: Tue, 02 Dec 2025 01:18:30 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3978c864a7e5ff2038df90bcd66647c7b1cba083c414e72852fca8a9f36caf94`  
		Last Modified: Tue, 02 Dec 2025 01:18:30 GMT  
		Size: 1.5 MB (1525124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7350500d99eb8b14f1d0713516315dc2017a0fd2dc7af999adba930fd54d07a5`  
		Last Modified: Tue, 02 Dec 2025 01:18:30 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:ea0715dd9ce3498dcd3bd9fc86e0f112d5ab16ddef6b7a166f512b56d602adc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99f6e462efb442c035fa43dde0211f04cf54172d697f60b211bc701c079de65`

```dockerfile
```

-	Layers:
	-	`sha256:e3752b6a7e75550467285b15adb6556a424a1418015f58393964c87ece798c24`  
		Last Modified: Tue, 02 Dec 2025 02:34:41 GMT  
		Size: 596.7 KB (596679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f3147f02eee67f5205e3001f8fb8c46e38711c04743fc3be8ddd56bc610efd`  
		Last Modified: Tue, 02 Dec 2025 02:34:42 GMT  
		Size: 42.2 KB (42233 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.4` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:dd8ec5f588516b049815720e27924c17a2c9dc8bd75f1a57b52749302e69cea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189e2237372f099b4011ff7106d37beb69221255b1467c34505b53d290ce2e11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:57:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:57:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:57:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:57:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:57:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:57:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:57:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:57:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:57:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 20 Nov 2025 19:57:40 GMT
ENV PHP_VERSION=8.4.15
# Thu, 20 Nov 2025 19:57:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 20 Nov 2025 19:57:40 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 19:57:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 19:57:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:01:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:01:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:01:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:01:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:01:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:01:18 GMT
CMD ["php" "-a"]
# Thu, 20 Nov 2025 20:39:20 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 20 Nov 2025 20:39:20 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 20 Nov 2025 20:39:20 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:40:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 20 Nov 2025 20:40:30 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 20 Nov 2025 20:40:32 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 20 Nov 2025 20:40:32 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 20 Nov 2025 20:40:32 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 20 Nov 2025 20:40:32 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 20 Nov 2025 20:40:32 GMT
VOLUME [/var/www/html]
# Thu, 20 Nov 2025 20:40:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:40:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Nov 2025 20:40:32 GMT
USER www-data
# Thu, 20 Nov 2025 20:40:32 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040243aa29cedcb107d7111b4af58d15c8e38287555d0f57218ff445772d824a`  
		Last Modified: Thu, 20 Nov 2025 20:01:50 GMT  
		Size: 3.5 MB (3466804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fa47c10ac875bb21fe410c6b8ea6d8f0902496e2b292ba88a8f27d8363f904`  
		Last Modified: Thu, 20 Nov 2025 20:01:48 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094c70b86975ea2d2ebb882c7a70ce186e2a98659a1c1b23d4ad2988983a03a2`  
		Last Modified: Thu, 20 Nov 2025 20:01:49 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ba7d3b2a887d7d7958e5c31dff3aa8d48234ff12cf8949f7a2b5ff6bcb4bd8`  
		Last Modified: Thu, 20 Nov 2025 20:01:51 GMT  
		Size: 13.7 MB (13673884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d87d78339003f7ecd72a3a7fa6ed9bb5a7619ea8a1910ebed95480e081a52f1`  
		Last Modified: Thu, 20 Nov 2025 20:01:49 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e09745f556cd60a826055b202f4dbe211b83ac989d3e2710b78c7cd787777c`  
		Last Modified: Thu, 20 Nov 2025 20:01:52 GMT  
		Size: 19.5 MB (19506296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a32ee3cc976abeff36fb2ea635207fc56b19d42f751923ea22966fbf9dfb31`  
		Last Modified: Thu, 20 Nov 2025 20:01:50 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d188b6c862dc031f75fe3c0c26593b60319283e6dd986737b1b0bd65f55f978`  
		Last Modified: Thu, 20 Nov 2025 20:01:50 GMT  
		Size: 19.9 KB (19860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969daa97271350a9eefaeecb91bf3c4702356c64c4bd99a52588a7dd5f9963ae`  
		Last Modified: Thu, 20 Nov 2025 20:01:50 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c64f7732dd196ad9c2c2df5f22af5ebb7e611de1efd627ede1779a08ebda35`  
		Last Modified: Fri, 21 Nov 2025 01:17:24 GMT  
		Size: 11.1 MB (11080271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7b378d4160f0a2bf865b1d8a7790c055adf82ab0ccbfe9a2e3b75b44ab5349`  
		Last Modified: Fri, 21 Nov 2025 01:17:27 GMT  
		Size: 14.2 MB (14242657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064ad00afff22cc519540260c8fafb00d98443c6628310d127c5bc621fe43e6a`  
		Last Modified: Thu, 20 Nov 2025 21:26:59 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa88781bf3e4603030289546ebf69f0f130730898c739f95c4fc7fc6a9e69dc`  
		Last Modified: Thu, 20 Nov 2025 21:26:59 GMT  
		Size: 1.5 MB (1525140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccf8b9f54166e88ca4b97497428e9b06d481b07b706c4fa3b8eafab9cfde265`  
		Last Modified: Thu, 20 Nov 2025 21:26:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:d2a33f3a59b567f01e97bb8c360bc339836ae7c9e0f17fff985ea585ed0c347c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27be86241c0a157033e9dd54459c49b142955f997cc5f77ec8d83bbc23f4982b`

```dockerfile
```

-	Layers:
	-	`sha256:9a4520143e4cb4af3fe0d5806067cfa386ca9b5a3e65752858d8d5bb95a549e8`  
		Last Modified: Thu, 20 Nov 2025 23:28:57 GMT  
		Size: 596.7 KB (596699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acf2eb62a9060980b439396d67b27987fcd1a507c493a8c6319a5310085c1ee3`  
		Last Modified: Thu, 20 Nov 2025 23:28:57 GMT  
		Size: 42.2 KB (42204 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.4` - linux; 386

```console
$ docker pull wordpress@sha256:497f465ee5926ac4f668d4bfe245130c81a731b0a2ab2275b67fd32d114ab162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67547536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ac869490ac0976413ff35cb8edbb272a3bb853c89002092bfbc71a3533b543`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:59:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:59:11 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:59:11 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:59:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:59:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:59:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:59:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:59:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:59:11 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 20 Nov 2025 19:59:11 GMT
ENV PHP_VERSION=8.4.15
# Thu, 20 Nov 2025 19:59:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 20 Nov 2025 19:59:11 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 19:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 19:59:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:02:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:02:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:02:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:02:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:02:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:02:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:10:27 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:10:27 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:10:27 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:11:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:11:15 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:11:16 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:11:16 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:11:16 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:11:16 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:11:16 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:11:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:11:16 GMT
USER www-data
# Tue, 02 Dec 2025 01:11:16 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357bf80fc60bb4c26b75496bda5419ca44787cdd4b54acc8e127032d7f5087f5`  
		Last Modified: Thu, 20 Nov 2025 20:02:39 GMT  
		Size: 3.5 MB (3522979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1389bf7e37ca1d877560cec7def2084c172a73cb30dc6d0aea59ed31ad01fe89`  
		Last Modified: Thu, 20 Nov 2025 20:02:38 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7d1b9e80a6e3d1ee53fa0911717df6f4823e9fa294b8c9f7e2c56276fb7caf`  
		Last Modified: Thu, 20 Nov 2025 20:02:39 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06afb0dd4814c9bcd9be8eb8a288ca250ca846a6582cf6581b8ec3b58b1c51e7`  
		Last Modified: Thu, 20 Nov 2025 20:02:42 GMT  
		Size: 13.7 MB (13673864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6822dbff2d66bb9d1d5e263c032424931dc40f008154c605fd6c025d31241d`  
		Last Modified: Thu, 20 Nov 2025 20:02:42 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5fd92aaa1244370d6cecbe88dd16bf6da1a270bdefae99cb481b376f3456e1`  
		Last Modified: Thu, 20 Nov 2025 20:02:41 GMT  
		Size: 20.5 MB (20492292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc44d0def01bc9fca2d65890c7f33ebfa1cb18d0aff7e21c54b080bf14c8aeb`  
		Last Modified: Thu, 20 Nov 2025 20:02:39 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd7b6a799efed09b66496a441f10b5a3186185ee6f21dca461305baa9390ef5`  
		Last Modified: Thu, 20 Nov 2025 20:02:39 GMT  
		Size: 20.1 KB (20050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36822c7b23e21734d814c9e8b50a523a14d69e28908c1cc2bcc48857842ff264`  
		Last Modified: Thu, 20 Nov 2025 20:02:39 GMT  
		Size: 20.0 KB (20047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34915d7dc67de899f5d7c243bc396554bc522a2718b2d2a5a4fc723f7c60e9f3`  
		Last Modified: Tue, 02 Dec 2025 01:11:45 GMT  
		Size: 11.3 MB (11274954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082184ec4968af6a5fae5a9850c1a6cb0fcc22bf78d17ebecfbcad1bba58528f`  
		Last Modified: Tue, 02 Dec 2025 01:11:46 GMT  
		Size: 13.4 MB (13394343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836b073fca02b432779e64ac2ad89383669811a1e43634911d5f0dba6d7eb05e`  
		Last Modified: Tue, 02 Dec 2025 01:11:43 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d7e9144ef41f94c0f73474814b3a5d8a15153855d5b1cecf21b705e0d67b22`  
		Last Modified: Tue, 02 Dec 2025 01:11:44 GMT  
		Size: 1.5 MB (1525131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e42a8bac7aaf45af6e7f32a7702470340f7a184e2737299c7d5af99e830fc`  
		Last Modified: Tue, 02 Dec 2025 01:11:44 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:9346ae46856ade26a25e067d0206d0a395282edb7f946e6620661cc49f4bf091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.9 KB (639924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4ad73ba46052e186f38320970bbeae1ec8dfb48d37aeec9b2728ead0b35738`

```dockerfile
```

-	Layers:
	-	`sha256:62803f20b53933411be381b2023ddc25c4ee50ebc48806b46a75465717dd220b`  
		Last Modified: Tue, 02 Dec 2025 02:34:48 GMT  
		Size: 597.9 KB (597862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0b9475c5401bdbaa136ba7a76fd18046231fd6df4f23041cb7233594ee2f5ef`  
		Last Modified: Tue, 02 Dec 2025 02:34:49 GMT  
		Size: 42.1 KB (42062 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.4` - linux; ppc64le

```console
$ docker pull wordpress@sha256:e019bfded46b31deaa1bacbfabfeb59abdc8137e5bcd6775955e76fb4acdd50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69316271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f2bf6429ca1ad20aaecb2009c5148683813b524ac1ec50aa70b6275b5377a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 00:51:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Oct 2025 00:51:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Oct 2025 00:51:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Oct 2025 00:51:44 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_VERSION=8.4.15
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 20:47:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:47:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:50:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:50:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:50:49 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:50:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:50:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:50:51 GMT
CMD ["php" "-a"]
# Thu, 20 Nov 2025 21:44:38 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 20 Nov 2025 21:44:39 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 20 Nov 2025 21:44:39 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 21:46:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 20 Nov 2025 21:46:13 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 20 Nov 2025 21:46:19 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 20 Nov 2025 21:46:19 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 20 Nov 2025 21:46:19 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 20 Nov 2025 21:46:19 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 20 Nov 2025 21:46:19 GMT
VOLUME [/var/www/html]
# Thu, 20 Nov 2025 21:46:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 21:46:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Nov 2025 21:46:20 GMT
USER www-data
# Thu, 20 Nov 2025 21:46:20 GMT
CMD ["wp" "shell"]
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
	-	`sha256:16c5a8f25c4e8eab95191d7f6db3c14c7fa870f8338f629d6de75837c0cd2a3d`  
		Last Modified: Thu, 20 Nov 2025 22:06:10 GMT  
		Size: 13.7 MB (13673890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca9262f4dca801daecd8c570d6f6bf0f321b0c3aa574dd36a710b32d81e719b`  
		Last Modified: Thu, 20 Nov 2025 21:41:57 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a142eeaf3749f4e9af0b2a8f1cb071eeb9f6f35a9effc1db0ba97352b5c12c`  
		Last Modified: Thu, 20 Nov 2025 22:06:12 GMT  
		Size: 20.9 MB (20863492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0616b74da9fedc13172f15301c5acfbcde83f76ec3f8cdc375918d5d973fcf2`  
		Last Modified: Thu, 20 Nov 2025 21:42:29 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81855667b66cb0de30effb9df8f71805bd7005410b5504653341d6179e8d0608`  
		Last Modified: Thu, 20 Nov 2025 21:42:28 GMT  
		Size: 19.9 KB (19876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130282b7939e3f3abc5502d925c20c64eeaa8ae866ecc44e6ab40230897f89b2`  
		Last Modified: Thu, 20 Nov 2025 21:42:29 GMT  
		Size: 19.9 KB (19874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262cb71029db2439beda81cbf33303ce12526299c5a083b26586772972c37c4c`  
		Last Modified: Thu, 20 Nov 2025 21:46:51 GMT  
		Size: 11.7 MB (11690228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3d9f4df5563f29bb5f366e144e308dc6d7264684ba39b5d2ee8452c3eed5e5`  
		Last Modified: Thu, 20 Nov 2025 21:46:54 GMT  
		Size: 14.2 MB (14171910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6694ab5cf3b61902efcb476965b2c473ea7710aa4e9d1b85c4568c9ef4bc6a98`  
		Last Modified: Thu, 20 Nov 2025 21:46:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453224e705a3bc6ffe99dadac8719fdb121b52b2632af91af6668a13d1677cd5`  
		Last Modified: Thu, 20 Nov 2025 21:46:50 GMT  
		Size: 1.5 MB (1525129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914b7f82605fb2c23e0d9e4fb05ff6379cc3e19ba17358caaaded817ed46789f`  
		Last Modified: Thu, 20 Nov 2025 21:46:50 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:00fa414d381b79805f348150642311c7d71456fc5d670aaa7332c06803b740d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 KB (636818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef105b3e4c8291a32edce900fac18c25ffdeaa9c51eb9b90b743a2077da25e27`

```dockerfile
```

-	Layers:
	-	`sha256:df9ac6421cfc8d06af24e04323eb9c6d21dd2af58afdf7b7eec707efaf90641c`  
		Last Modified: Thu, 20 Nov 2025 23:29:05 GMT  
		Size: 594.7 KB (594726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6e732e09246eb02dc730366a33dd5f3582dc913865f8a7641d0184dace0438b`  
		Last Modified: Thu, 20 Nov 2025 23:29:06 GMT  
		Size: 42.1 KB (42092 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.4` - linux; riscv64

```console
$ docker pull wordpress@sha256:4fe5a86041aac4588431bcb841ac91bfe4f7cffd3f56235aa8824327afb208df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65236200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2d3ef92e7720ffe903d7772d5d7b141a78d200df17351fd421dc786a6e1da6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 05:22:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Oct 2025 05:22:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Oct 2025 05:22:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Oct 2025 05:22:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Oct 2025 05:22:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Oct 2025 05:22:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_VERSION=8.4.15
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Sat, 22 Nov 2025 06:10:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 22 Nov 2025 06:10:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 22 Nov 2025 07:07:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 22 Nov 2025 07:07:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 22 Nov 2025 07:07:27 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 22 Nov 2025 07:07:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 22 Nov 2025 07:07:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 22 Nov 2025 07:07:32 GMT
CMD ["php" "-a"]
# Sun, 23 Nov 2025 03:29:11 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Sun, 23 Nov 2025 03:29:12 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Sun, 23 Nov 2025 03:29:12 GMT
WORKDIR /var/www/html
# Sun, 23 Nov 2025 03:44:18 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sun, 23 Nov 2025 03:44:19 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Sun, 23 Nov 2025 03:44:29 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Sun, 23 Nov 2025 03:44:29 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Sun, 23 Nov 2025 03:44:29 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Sun, 23 Nov 2025 03:44:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Sun, 23 Nov 2025 03:44:29 GMT
VOLUME [/var/www/html]
# Sun, 23 Nov 2025 03:44:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 23 Nov 2025 03:44:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 23 Nov 2025 03:44:29 GMT
USER www-data
# Sun, 23 Nov 2025 03:44:29 GMT
CMD ["wp" "shell"]
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
	-	`sha256:331170c4328036a3269b793e5fd9ac752d80feb44103a984ea324988b0db1df4`  
		Last Modified: Sat, 22 Nov 2025 07:08:45 GMT  
		Size: 13.7 MB (13673887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2a8a76b8fe94dfb64b674f64bb4173189f79d3b177f92ff910f6a2cd067311`  
		Last Modified: Sat, 22 Nov 2025 07:08:42 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d398131a8b8b3c8c0dbefad5dc63410d37792a565403072e46746d6864e62e09`  
		Last Modified: Sat, 22 Nov 2025 07:08:44 GMT  
		Size: 19.4 MB (19380428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd637506d8e18ef3c74275f21eda516b02d8623e9a9146037fb01025fe77032`  
		Last Modified: Sat, 22 Nov 2025 07:08:42 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fecb0a61f649615d608d9f51bc9a99c2efae0eed556f989b77304dc2a29178e`  
		Last Modified: Sat, 22 Nov 2025 07:08:42 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751aad56cbbfd04d3122faa2f71bf90aaaa4bb3224d3ccd2bc9d134f7bc0ec35`  
		Last Modified: Sat, 22 Nov 2025 07:08:42 GMT  
		Size: 19.9 KB (19860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47b567289e4ec9bd8dde72c28be8cce48ff328860aedba1289ee07f5559f239`  
		Last Modified: Sun, 23 Nov 2025 03:46:06 GMT  
		Size: 11.6 MB (11571123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39c2820b4656857c33c9f96d3552dd1382e0d93d2f8d419ed80979a15803e48`  
		Last Modified: Sun, 23 Nov 2025 03:46:06 GMT  
		Size: 11.9 MB (11925419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f852e2e53be17f85b8580b7a5dea13948544c39d3486e63067daf429299a00d7`  
		Last Modified: Sun, 23 Nov 2025 03:46:05 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a752616258155359728d10215b5b22a86c51a2a3f08082bbf53ff2f7ceaca4c9`  
		Last Modified: Sun, 23 Nov 2025 03:46:05 GMT  
		Size: 1.5 MB (1525142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9385ad833aa01df8104d9e3ce27646bdb8d6a1f890f43b48e48ddc5e4c6d1798`  
		Last Modified: Sun, 23 Nov 2025 03:46:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:fa62b83caa3af99102b5c2b6d3157c63e8801f95cbcf31cc2efa749a8220f176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 KB (636814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c9bef7b93411fc54eb133a39c294723be5ce27cc2ac63442b692cf91effe35e`

```dockerfile
```

-	Layers:
	-	`sha256:d345028d9659b9dd8aedcf055e8c327d6cc98ed4f2aadd9750e7d849a36e2d79`  
		Last Modified: Mon, 24 Nov 2025 00:14:29 GMT  
		Size: 594.7 KB (594722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:400a679096bf4988509c6c23aad3ea5a74be75a41612423662c88dbb64b0e579`  
		Last Modified: Mon, 24 Nov 2025 00:14:41 GMT  
		Size: 42.1 KB (42092 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.4` - linux; s390x

```console
$ docker pull wordpress@sha256:0785bfbfe48927158f9491e71e04aa7009575465f462f5702d34f274caac7332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68869940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d23838623edfe6c62cd0a260cf1fb8fa16fc79bf2134901ec9dd8b816ce035`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 20:07:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 20:07:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 20:07:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 20:07:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:07:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:07:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:07:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:07:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:07:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 20 Nov 2025 20:07:47 GMT
ENV PHP_VERSION=8.4.15
# Thu, 20 Nov 2025 20:07:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 20 Nov 2025 20:07:47 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 20:29:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:29:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:34:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:34:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:34:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:34:10 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:34:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:34:10 GMT
CMD ["php" "-a"]
# Thu, 20 Nov 2025 21:29:43 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 20 Nov 2025 21:29:43 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 20 Nov 2025 21:29:43 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 21:31:22 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 20 Nov 2025 21:31:22 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 20 Nov 2025 21:31:26 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 20 Nov 2025 21:31:26 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 20 Nov 2025 21:31:26 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 20 Nov 2025 21:31:26 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 20 Nov 2025 21:31:26 GMT
VOLUME [/var/www/html]
# Thu, 20 Nov 2025 21:31:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 21:31:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Nov 2025 21:31:26 GMT
USER www-data
# Thu, 20 Nov 2025 21:31:26 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4b2ff0842c178e1087be78ce7fd9398e218ab3073b14df552c39751910aff3`  
		Last Modified: Thu, 20 Nov 2025 20:25:24 GMT  
		Size: 3.7 MB (3692751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64042f4c00639ff2bff63c33afc688c6925e0d013d64d2047303f209d99a1d1`  
		Last Modified: Thu, 20 Nov 2025 20:25:32 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc27a2ba216e3112820154e14072605aef9af1bf9567b41460e5ff99890c35`  
		Last Modified: Thu, 20 Nov 2025 20:25:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ea3786495e80087d47f4f757f10ce1fa39bd542d9560e03368cc3afbc84efc`  
		Last Modified: Thu, 20 Nov 2025 20:34:38 GMT  
		Size: 13.7 MB (13673914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccac8427cde6349c48f36fc91c1ad15e5a81264a05d8bebab4f0f147ab30c08`  
		Last Modified: Thu, 20 Nov 2025 20:34:37 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c201ec37542775027c380700bf7fbe001d2beae3cf2470fc602bb23e12f4ab9e`  
		Last Modified: Thu, 20 Nov 2025 20:34:39 GMT  
		Size: 20.0 MB (19977523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f9670f4064380358161d8d059efa19eab6c027a598f8088636f3f40cbb5393`  
		Last Modified: Thu, 20 Nov 2025 20:34:37 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f59050d2e7fbdbcab47141856e85fcbadab095d69ae86bdc9f028d06a0c5bb`  
		Last Modified: Thu, 20 Nov 2025 20:34:37 GMT  
		Size: 19.9 KB (19882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a501f405b5a2100a0fec119437952a0d5838ebb6341f6c7d3e75055e205f2e3`  
		Last Modified: Thu, 20 Nov 2025 20:34:44 GMT  
		Size: 19.9 KB (19877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30f9afe7d3f6ee214e1ddecd4806c92dd5fd86f44d1be7c6502d9f9210bc2f6`  
		Last Modified: Thu, 20 Nov 2025 21:31:52 GMT  
		Size: 12.5 MB (12452439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd4c525250d30f099728d1cee05749c7285fdf3545bdcc2d44072f8cc8155fa`  
		Last Modified: Thu, 20 Nov 2025 21:31:53 GMT  
		Size: 13.9 MB (13854174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4178989ca62f3b524b5ff876bc371e1befec40fc45b97e338941872580725b2b`  
		Last Modified: Thu, 20 Nov 2025 21:31:50 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5af42b66aa7e980d86883e5a1e09738e3b90d73d80248460fd6a55596be259`  
		Last Modified: Thu, 20 Nov 2025 21:31:50 GMT  
		Size: 1.5 MB (1525179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94639151a20db1a2639d3d42e5afc6e6a5729b8d2917bfc4e313ed3a4c50a5ab`  
		Last Modified: Thu, 20 Nov 2025 21:31:50 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:253e66ed46d80083cb63f4f95962e1c0fd0c469d2518478fc61440c112b84396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.7 KB (636730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656b9501d710cee4cf76c438a9a4b817000a00f0b1e5f472dfc4075a98205641`

```dockerfile
```

-	Layers:
	-	`sha256:d6a0e1784815d506920f4cc45fb4d873289efe7a793b04adeb746b26b62b3b6c`  
		Last Modified: Thu, 20 Nov 2025 23:29:13 GMT  
		Size: 594.7 KB (594692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:935bd5e347a5beade3086c981a52d7352eaf7fcb1392dc216e993c2751a24126`  
		Last Modified: Thu, 20 Nov 2025 23:29:14 GMT  
		Size: 42.0 KB (42038 bytes)  
		MIME: application/vnd.in-toto+json
