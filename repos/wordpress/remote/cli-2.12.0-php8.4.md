## `wordpress:cli-2.12.0-php8.4`

```console
$ docker pull wordpress@sha256:4700b6929401fe4b8a1fa9512f8c44c6ea468bf1d36695eddaa4205c26640b32
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

### `wordpress:cli-2.12.0-php8.4` - linux; amd64

```console
$ docker pull wordpress@sha256:67770b7924a60948293972877e711e3cf78f7fc2c1189b09bc9c9af76bd5b3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72343933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15076b80d18f6c6ff3963869e4ddbd696274ae568fb2d5db9b56830c97093d13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:18:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:18:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:18:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:18:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:18:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:18:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:18:06 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:18:06 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:18:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:18:06 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:24 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:20:42 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 15 Apr 2026 21:20:42 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 15 Apr 2026 21:20:42 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 21:21:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:21:27 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:21:29 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 15 Apr 2026 21:21:29 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 15 Apr 2026 21:21:29 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 15 Apr 2026 21:21:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 15 Apr 2026 21:21:29 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:21:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:21:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:21:29 GMT
USER www-data
# Wed, 15 Apr 2026 21:21:29 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf854b8c91e4ffb62a3ee12cfb7e690628876e65b5aa9089ecb42ee7876812d`  
		Last Modified: Wed, 15 Apr 2026 20:21:31 GMT  
		Size: 3.6 MB (3587500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8d60de6fb544315f80501715359e13b2fa42dfdeb2db613c9733cb11d29d39`  
		Last Modified: Wed, 15 Apr 2026 20:21:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fbf9d0d88198ef9e40a6a2d2f918bb5c8ec0405a2704d6f282db4224b12768`  
		Last Modified: Wed, 15 Apr 2026 20:21:31 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c4648ca40f3a0d476d0002112e9f9eb1db044918d55cc5d86a19fa0c0eb97`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 13.7 MB (13709880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef527a10ba902c1f9fd3713fa41a826be8008c35bc9055b322ac4bb89adb5eb`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037b8b2e7ae521ba1fa346558196f0aa2e3344993550a5cb1ac53728e9b179d2`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 20.2 MB (20183070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f646b4cf0206cb50174a1c70541b7a3869cf2a1d482e618a64c71e537f9bd8`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e23d160d0a2964493580ab71792adffc8bcc0c6d16dc684f90b3142cb7f884c`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 23.4 KB (23398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13d8fcb1fc2eb5ec8955b5813bddf93cf73bb8ad69c0107f6b9e881e7de75e7`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 23.4 KB (23417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc3d3432e9131a4d44e46a1c2697e8d5b552d8d2fad9718ad15c38295409704`  
		Last Modified: Wed, 15 Apr 2026 21:21:38 GMT  
		Size: 11.2 MB (11154403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f34caaa48626ad2f4895aa8462979210cfd4adf98848750a4c9aac3fc8309e`  
		Last Modified: Wed, 15 Apr 2026 21:21:38 GMT  
		Size: 18.3 MB (18257567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a45fd2ae7798296d576e296680aa142de2bcfb5527a7c5e173943a47d7cf64a`  
		Last Modified: Wed, 15 Apr 2026 21:21:38 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d4be5fa01bd8f112ae1e9f6eb181322acb2751ec8d7c6c61e1d4f7603fb65b`  
		Last Modified: Wed, 15 Apr 2026 21:21:38 GMT  
		Size: 1.5 MB (1535562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f337887e8e0ba27310cb016b37eb835846c824e6ac375eb29666fb7558d836ab`  
		Last Modified: Wed, 15 Apr 2026 21:21:39 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:b5066ea49c3a1254a84c87dd671f2aaa5b9876f52d7ab403149164ea38d45307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.2 KB (681196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2edd558fb6cba3c2fd9f2a9ec7cb864cd99085e59e01b4d1cd0a3a620889274`

```dockerfile
```

-	Layers:
	-	`sha256:6921c1cb22c528fd7bd28a91b9f23c30aec36e6f6a8c358ed39cdcb6102d178e`  
		Last Modified: Wed, 15 Apr 2026 21:21:37 GMT  
		Size: 639.1 KB (639094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f71a054c985670bcef20fc70bdcc50cccadd03e52defb4a8a4b8df56b5c863f3`  
		Last Modified: Wed, 15 Apr 2026 21:21:38 GMT  
		Size: 42.1 KB (42102 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.4` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:1db33983ed2ef8eec45524b326f4d26ea040cf6d830bae1ce8072446f5c6b13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66411304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60160c23fe051663461b67e2758a5dd386a935e3cd0ae02cbd114105aef07191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:19:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:19:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:19:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:19:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:19:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:19:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:19:30 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:19:30 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:19:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:19:30 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:19:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:19:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:22:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:22:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:22:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:22:34 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:20:24 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 15 Apr 2026 21:20:24 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 15 Apr 2026 21:20:24 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 21:21:44 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:21:44 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:21:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 15 Apr 2026 21:21:46 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 15 Apr 2026 21:21:46 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 15 Apr 2026 21:21:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 15 Apr 2026 21:21:46 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:21:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:21:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:21:46 GMT
USER www-data
# Wed, 15 Apr 2026 21:21:46 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f52c3596cc98e6e76848bec19e4c9e0484156481920b0f4e447e3daa7652213`  
		Last Modified: Wed, 15 Apr 2026 20:22:39 GMT  
		Size: 3.5 MB (3543060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cbd0262f527ba21feb3f4d5daebf8d7dabbe2c4ae2d89ad6b8922204d8891c`  
		Last Modified: Wed, 15 Apr 2026 20:22:39 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b7c749ab9f0b1aafd747d658ab8401622f2f6fb87bb8a66862b6a7d5df9530`  
		Last Modified: Wed, 15 Apr 2026 20:22:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5ddeccdca3545464c520d1fadeae10962b1e39776c0d6aa2145631e13cb777`  
		Last Modified: Wed, 15 Apr 2026 20:22:40 GMT  
		Size: 13.7 MB (13709880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eebceec1aacf2cccb7f9cbd4aad1b530397b9cfac2fe99d3589f8e65a680504`  
		Last Modified: Wed, 15 Apr 2026 20:22:40 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b39051b9b9bf66f84fed76055c2fe42894c84f8668faca3a52b821f5eccbc73`  
		Last Modified: Wed, 15 Apr 2026 20:22:41 GMT  
		Size: 18.3 MB (18260312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2f46ff476d58def7b2ba3b7878da29c91a439646f86562fd369689b705ca62`  
		Last Modified: Wed, 15 Apr 2026 20:22:41 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680068604d143e0d4ca2db21bd20bf13757eb2f7973c4ad40c3932da3a697935`  
		Last Modified: Wed, 15 Apr 2026 20:22:41 GMT  
		Size: 23.2 KB (23209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2018600af1eb3fa6eab8ac2f79c78957aede219bfdfad8c309a5f7e6c1b6b4f`  
		Last Modified: Wed, 15 Apr 2026 20:22:42 GMT  
		Size: 23.2 KB (23222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091ae87e7a31f465d59596d9c800c0474f2131b3d5c7caa64529899f5703af17`  
		Last Modified: Wed, 15 Apr 2026 21:21:52 GMT  
		Size: 10.9 MB (10882814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec2a5b2520f3a6f4eefe71bf6b0fbde2b3f89d076ab05611eb6a406901e7494`  
		Last Modified: Wed, 15 Apr 2026 21:21:52 GMT  
		Size: 14.9 MB (14856403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbf2d6ea475a96e3b6a88b8c725d5e155af718b1f644f7261e3279730547a01`  
		Last Modified: Wed, 15 Apr 2026 21:21:52 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3ca25e25d396f2d9f0db1bfa5da2561cc5c697591ec4a0418d1021f4a1345`  
		Last Modified: Wed, 15 Apr 2026 21:21:52 GMT  
		Size: 1.5 MB (1535599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3fb3642024c76e9d9ad1a1dd3d36c5ff6b9cc6c42ec675fce5622efcb51abd`  
		Last Modified: Wed, 15 Apr 2026 21:21:53 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:20cfe1a6e087eb17185d6a0d67bca494f3caa28672115cbe0cbf8e60b725529e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 KB (42019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e969392b70c9cdd89dbca017fb0c4ffbce9e85df90ce32ec08c98aae3b40f11`

```dockerfile
```

-	Layers:
	-	`sha256:5b6d0447cd297ccc041ee5bd84f02e64a512f492c77594f2c25439f8fb106895`  
		Last Modified: Wed, 15 Apr 2026 21:21:51 GMT  
		Size: 42.0 KB (42019 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.4` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:58fe8db617460959066a35a0fa7ca747d8e887cdbc3ff203a061624927d41c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64981873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf99fd5dedb36cfba630771e3f2b9ee7b4842ee5e037a7e77cd9e83a579b2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:19:20 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:19:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:19:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:19:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:19:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:19:20 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:19:20 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:19:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:19:20 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:19:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:19:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:22:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:22:26 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:22:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:22:26 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:30:06 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 15 Apr 2026 21:30:07 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 15 Apr 2026 21:30:07 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 21:31:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:31:29 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:31:31 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 15 Apr 2026 21:31:31 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 15 Apr 2026 21:31:31 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 15 Apr 2026 21:31:31 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 15 Apr 2026 21:31:31 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:31:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:31:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:31:31 GMT
USER www-data
# Wed, 15 Apr 2026 21:31:31 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cea23af5397642d8ae1876dc604658a1579495dbfdebfaf82a61d8d2f4ab05`  
		Last Modified: Wed, 15 Apr 2026 20:22:33 GMT  
		Size: 3.3 MB (3343378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4bc49b2c915039b4a2d18c1efbd2086b2f24c749d502d7ff8f310b591038fc`  
		Last Modified: Wed, 15 Apr 2026 20:22:33 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddfca79851bb6bc8753e1443a95657d5668d41b625435cfa5f718604b846b6d`  
		Last Modified: Wed, 15 Apr 2026 20:22:33 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056cbe0e2683d67eae4ac47c4c1a4e3fd46dc6655758110670f06ba5e39ec89d`  
		Last Modified: Wed, 15 Apr 2026 20:22:33 GMT  
		Size: 13.7 MB (13709892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6de7c0e4368351e1972a2f99cfe720cec697be5b1c658ef3a3ccd3fe9ddeb28`  
		Last Modified: Wed, 15 Apr 2026 20:22:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7c47a185ff7a1481ead244b70a34034ee8e67cd5d54e5c41a7cc244e1f8a9a`  
		Last Modified: Wed, 15 Apr 2026 20:22:34 GMT  
		Size: 17.2 MB (17218805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c1c13627655a7f733826993ac29f0eb01a764eab2a4b6f94d646e688ba6b64`  
		Last Modified: Wed, 15 Apr 2026 20:22:34 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc6dd6ec2c95a5afa4a096974f448d8488c846aa4b78d7278a670d554dab166`  
		Last Modified: Wed, 15 Apr 2026 20:22:35 GMT  
		Size: 23.2 KB (23212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb549c80b425422beca0a2044b9ed9da6ebef0e69ab5ace040fe796001d381d4`  
		Last Modified: Wed, 15 Apr 2026 20:22:35 GMT  
		Size: 23.2 KB (23230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9514acb4637f98509b73138a160268b7ba36a166018448fff26ffb0814cafde`  
		Last Modified: Wed, 15 Apr 2026 21:31:40 GMT  
		Size: 10.5 MB (10536241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e018d34eae9db2b8fad7081210d2fefbd31240c7b0487b42e37558876122efed`  
		Last Modified: Wed, 15 Apr 2026 21:31:40 GMT  
		Size: 15.3 MB (15303470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9598a599089898dffd12f9736d1707258e1885b51892f452518e2b6dfe17e5c`  
		Last Modified: Wed, 15 Apr 2026 21:31:39 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef6139c4b555d76f5b1bade34c335e0ca793521b1840c372ebe7a0419fe0c8c`  
		Last Modified: Wed, 15 Apr 2026 21:31:39 GMT  
		Size: 1.5 MB (1535577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e23773564747e2937a568dea66ac72c2b9c2e97cf8226e2d0595fd00b77c009`  
		Last Modified: Wed, 15 Apr 2026 21:31:40 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:184cb1a35e79a141d1ee49c850e7d9dd6a657a5994ba64f07e4fcb61cdc2b434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.5 KB (679469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b319908a341e0bede01d0fe6681d18942cdbf1574b63ea981c412314e33dd4fb`

```dockerfile
```

-	Layers:
	-	`sha256:6c36bf947d42163706e34637715e5414eeaadf02a4a61dabeeaa7b35da8b071a`  
		Last Modified: Wed, 15 Apr 2026 21:31:39 GMT  
		Size: 637.2 KB (637236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6bc30f6eab682627a870ee7e7de659f802bb7c37428aca07fe1cadbc4865f41`  
		Last Modified: Wed, 15 Apr 2026 21:31:39 GMT  
		Size: 42.2 KB (42233 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.4` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:00c9d05b25e8f651f26385c330ed8a0771571f55a9617b97f95cc3c74fc5c93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71001885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33f2fd9ea41fa0af73ccf862910868d3252022a76860c7c532ebaa8bff26bfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:16:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:16:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:19:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:50 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:19:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:19:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:19:50 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:35:54 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 15 Apr 2026 21:35:54 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 15 Apr 2026 21:35:54 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 21:36:53 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:36:53 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:36:55 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 15 Apr 2026 21:36:55 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 15 Apr 2026 21:36:55 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 15 Apr 2026 21:36:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 15 Apr 2026 21:36:55 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:36:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:36:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:36:55 GMT
USER www-data
# Wed, 15 Apr 2026 21:36:55 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df262ced427efd0970a0ab672c603c196c63b2e2dfdb5dcdd431e0ce883cbe9a`  
		Last Modified: Wed, 15 Apr 2026 20:19:58 GMT  
		Size: 3.6 MB (3596159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a445eaa91ff3934ecd659dab2a62af3cb112d6d5656f8b0dada0f9f8b1f56dab`  
		Last Modified: Wed, 15 Apr 2026 20:19:58 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87afe6b0de91284408c7001749f46a65292ea649bcb4ffad3c1114556650d75d`  
		Last Modified: Wed, 15 Apr 2026 20:19:58 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855961660c825301f444bfc13d8eb54a56f4f4a4a1c2be4cf28ce2c9ffdfbb10`  
		Last Modified: Wed, 15 Apr 2026 20:19:58 GMT  
		Size: 13.7 MB (13709883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee88d4650cc4edc5587a4642e8c636882e7cafa529a0d77924dc0cb9bf9a9153`  
		Last Modified: Wed, 15 Apr 2026 20:19:59 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbacd56be3a326466de78dd234e58369687161ee2c81990fe59e92328d3e39d7`  
		Last Modified: Wed, 15 Apr 2026 20:19:59 GMT  
		Size: 19.5 MB (19545608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb52d6ff0296e3a156d33f705093b2890fd8ad4dfa48991ee71fe9e395a4f0ef`  
		Last Modified: Wed, 15 Apr 2026 20:19:59 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377c1293650ab6825bcc1022282fca6e6cd6986024b5d5a3b1f72e8ac917dc7b`  
		Last Modified: Wed, 15 Apr 2026 20:19:59 GMT  
		Size: 23.2 KB (23213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7596035c5cfcb9e84d850fc79c7ae0cafac804f3b7644f0b112219ecd5bc78`  
		Last Modified: Wed, 15 Apr 2026 20:20:00 GMT  
		Size: 23.2 KB (23226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81a4e5f0a3fc2d80dfa64313881b17c35b02786484e917b4eccdfe5ea3a51f1`  
		Last Modified: Wed, 15 Apr 2026 21:37:04 GMT  
		Size: 11.1 MB (11098220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d464c60d5750dde8502c31aa06e0f3fad23a8b324aeea94985e5227ae5c301c`  
		Last Modified: Wed, 15 Apr 2026 21:37:04 GMT  
		Size: 17.3 MB (17265154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375b187093aee1a56248687a743693856902a8b3a063b8dedd4cabd3766f7489`  
		Last Modified: Wed, 15 Apr 2026 21:37:04 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c702a76301f953884c14f031d37e967b529cd361a4bc93bbb51590747f99a10c`  
		Last Modified: Wed, 15 Apr 2026 21:37:04 GMT  
		Size: 1.5 MB (1535610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0191a03e5593408ef02a6310a61e971d50672421729e363b522ad5fa92eb8c`  
		Last Modified: Wed, 15 Apr 2026 21:37:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:8610334e854dff69de33d19b109aa6141292ef6ad0ac92d9352a794db6d1ffbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.5 KB (679522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93afb5f4f207f8d343f0f17d6a413b82b364961212eb1eee56ccc5927896aa7`

```dockerfile
```

-	Layers:
	-	`sha256:966a42025fb1401306fb0c6d9db4aac79c9d4010965e89407a8d336128470127`  
		Last Modified: Wed, 15 Apr 2026 21:37:03 GMT  
		Size: 637.3 KB (637256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7f262f446c02e78ddfc9f0e1dbe4bb5c03d390dd57b96afcfbb808385b68150`  
		Last Modified: Wed, 15 Apr 2026 21:37:03 GMT  
		Size: 42.3 KB (42266 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.4` - linux; 386

```console
$ docker pull wordpress@sha256:c57a7df2d2f43ebf9bee9e4b863a3c5cde136614f8062d43e6ddcac114c54f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71851141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5c3e0ffb0cc1cc6695b139527e32c8f43f4d0549aca220d0b92d8fd666f372`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:21:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 22:21:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 22:21:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 22:21:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 22:21:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 22:21:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 22:21:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 22:21:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 22:21:11 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 22:21:11 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 22:21:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 22:21:11 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 22:21:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 22:21:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:24:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 22:24:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:24:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 22:24:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 22:24:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 22:24:47 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 23:15:13 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 15 Apr 2026 23:15:13 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 15 Apr 2026 23:15:13 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 23:16:06 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 23:16:06 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 23:16:08 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 15 Apr 2026 23:16:08 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 15 Apr 2026 23:16:08 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 15 Apr 2026 23:16:08 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 15 Apr 2026 23:16:08 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 23:16:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 23:16:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 23:16:08 GMT
USER www-data
# Wed, 15 Apr 2026 23:16:08 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f09af65fb4ba7d67e97f171cac39f633a9de1f19e89a545faf7ff1c81ad6641`  
		Last Modified: Wed, 15 Apr 2026 22:24:55 GMT  
		Size: 3.6 MB (3625730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8672baf2b8a0da01cca8e06e38f2d5dec9915656033cadc6cca932f8aa0e8b44`  
		Last Modified: Wed, 15 Apr 2026 22:24:54 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a462c7ae9472b92880c70050c2a9e7d83f7e6bf14bb0123f55a978eb1f135c1`  
		Last Modified: Wed, 15 Apr 2026 22:24:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718796863b0bf768aeba4e86e665aafcfcd3c6029941b57b8f2c01f23b62c659`  
		Last Modified: Wed, 15 Apr 2026 22:24:55 GMT  
		Size: 13.7 MB (13709865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183d9a5126d27ea9d3a21095e7d126a54cd5a2c6b5ccc2c53e7bd95208a1c6d5`  
		Last Modified: Wed, 15 Apr 2026 22:24:56 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade3a2f0808448bd23e065a641a2997d0c192f6901ad51c37949c593ef03e6af`  
		Last Modified: Wed, 15 Apr 2026 22:24:56 GMT  
		Size: 20.6 MB (20580535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a07497f0d9c82bd93151bc8ceb776457eed66d23787ffb83791c2fbf859234e`  
		Last Modified: Wed, 15 Apr 2026 22:24:56 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de7c73112110c9be8c21c47c3ce289e67b722c05e112e4b9c16edf598fc5b75`  
		Last Modified: Wed, 15 Apr 2026 22:24:56 GMT  
		Size: 23.4 KB (23394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02376ba60f356c365aa1d2e4c11af5c24745bf14756afe38315a15696556b36d`  
		Last Modified: Wed, 15 Apr 2026 22:24:57 GMT  
		Size: 23.4 KB (23411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d5ea2d1c4ead90c3580d7e96c168655fd2274d765352a344bca1b1e0452d4f`  
		Last Modified: Wed, 15 Apr 2026 23:16:17 GMT  
		Size: 11.3 MB (11339151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5548df0b91e1e25744f1fd31e507d2c2bfb31dfca961d7413c49b527f025115d`  
		Last Modified: Wed, 15 Apr 2026 23:16:18 GMT  
		Size: 17.3 MB (17318110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59b378dd755d45b555e0b8fd62ba4bf7c72e5732f9e4ac271f1a5dc18d9e7ce`  
		Last Modified: Wed, 15 Apr 2026 23:16:17 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c6b9e0df30061bd46c5162cbd0095071414e4d630b586a45b7e5a7c146ca30`  
		Last Modified: Wed, 15 Apr 2026 23:16:17 GMT  
		Size: 1.5 MB (1535566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b427e21064ddcfc1fc608b684f044a41366f4938f5fbc6a98480f8b0e1e555f`  
		Last Modified: Wed, 15 Apr 2026 23:16:18 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:8c1cae35fc075c71bbc06e7eaf39a5e30f662979cc9608aa8c087530c6feed6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.1 KB (681131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78324b0ac14602f1ed657ec57e54d50907625a6b32c0519aa32dcd1740e529b`

```dockerfile
```

-	Layers:
	-	`sha256:c9c44c366a4f1abfcd74d247bb698f8682df8d1248ac734eee2f9364fa02b24e`  
		Last Modified: Wed, 15 Apr 2026 23:16:17 GMT  
		Size: 639.1 KB (639069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f808c20958fdcb18570250bf34550d1c6e5615f0f9c28ef6f0d5347de76e18f9`  
		Last Modified: Wed, 15 Apr 2026 23:16:17 GMT  
		Size: 42.1 KB (42062 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.4` - linux; ppc64le

```console
$ docker pull wordpress@sha256:82da5ab4327fb31a6ea70182edba0cbb40702e432078e46e84d3531d7d641cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74035420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3c24e84dff90dd4ff423cc50cc69eef2817e0af325608bc21220ae169fa18c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:20:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:20:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:26:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:27:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:32:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:32:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:32:04 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:32:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:32:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:32:06 GMT
CMD ["php" "-a"]
# Thu, 16 Apr 2026 00:02:00 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Thu, 16 Apr 2026 00:02:02 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Thu, 16 Apr 2026 00:02:03 GMT
WORKDIR /var/www/html
# Thu, 16 Apr 2026 00:03:47 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 16 Apr 2026 00:03:48 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 16 Apr 2026 00:03:51 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 16 Apr 2026 00:03:51 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Thu, 16 Apr 2026 00:03:51 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Thu, 16 Apr 2026 00:03:51 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Thu, 16 Apr 2026 00:03:51 GMT
VOLUME [/var/www/html]
# Thu, 16 Apr 2026 00:03:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:03:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:03:51 GMT
USER www-data
# Thu, 16 Apr 2026 00:03:51 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59216db1edcf64b90905df63416f821bfacdba590544dcdb3c340ea538567c`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 3.8 MB (3767095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dbb332183b4f53eb48b10e61f11a67b23c5647a6901cf35be6037e209a0f51`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd758015c67cd7fae70202df89f7e42a01ff424cadf0cd92070805333b28821`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0370fd1370a54392f3444f77669b0c6655267b3ae193cf4de50a9871836636e7`  
		Last Modified: Wed, 15 Apr 2026 20:32:23 GMT  
		Size: 13.7 MB (13709879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5dbe897696d0b00e89cb8cca0978c45cfac755af8488d2743b4d1d0e8349b9`  
		Last Modified: Wed, 15 Apr 2026 20:32:22 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddb3e394091a57c181bb949c289fa6bda5548180029bab9ac0120f921ac30c8`  
		Last Modified: Wed, 15 Apr 2026 20:32:23 GMT  
		Size: 21.2 MB (21173647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2b81747657ff9a7780b2aafac6fa95ddc910d2d5d17b2e6294728ea11702b2`  
		Last Modified: Wed, 15 Apr 2026 20:32:22 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202c9432e7aea2b74ff6ae470971572cbcb8eecb2f3b8304dca3f6bf1cad0335`  
		Last Modified: Wed, 15 Apr 2026 20:32:23 GMT  
		Size: 23.2 KB (23231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b442f703de40b01764ade33b292e6a19780730cd7e741c17cfe03622a378b56e`  
		Last Modified: Wed, 15 Apr 2026 20:32:23 GMT  
		Size: 23.3 KB (23252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7555a311037f423310cfcbcce5a85b6956a201783061d959fb86eb1963db27`  
		Last Modified: Thu, 16 Apr 2026 00:04:11 GMT  
		Size: 11.8 MB (11817772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df75de6aa881ac048d6695dd29024bea7517055c63504a6cc7c373b86e5d336`  
		Last Modified: Thu, 16 Apr 2026 00:04:10 GMT  
		Size: 18.1 MB (18149012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0912fa4d67a4479153ffa2f11e739fdfa07b548197c0cb3b4545c33592367d11`  
		Last Modified: Thu, 16 Apr 2026 00:04:09 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1281b9992a2b332f5ea64682419359082a4db808b1e800ab292c980d38435dc7`  
		Last Modified: Thu, 16 Apr 2026 00:04:09 GMT  
		Size: 1.5 MB (1535654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea683057f08f7eb619a8a813d99d6e2b9f59261b1935d8110623cee84449e5d`  
		Last Modified: Thu, 16 Apr 2026 00:04:10 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:ddd55fcfd2c8f483845064ef85b8c3b82d675fed9a8a986bc41c5188e00d3ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.4 KB (679387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f76278eaa2b9c865fb6aa7b62f6f74a144755a3d52f937d9c063d80063bb95`

```dockerfile
```

-	Layers:
	-	`sha256:d30102f41c61bf8bc4e909a325e7566259fd03c9c7674127065e23a9b3dbbeb7`  
		Last Modified: Thu, 16 Apr 2026 00:04:09 GMT  
		Size: 637.2 KB (637233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3217d7f6e1acae37bacdd9ab205984d87806254b3c10da0c645cb1956121ec8c`  
		Last Modified: Thu, 16 Apr 2026 00:04:09 GMT  
		Size: 42.2 KB (42154 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.4` - linux; riscv64

```console
$ docker pull wordpress@sha256:6b3322da6ea29781ab9877716b7e82112355c63080292145389a275260f8b8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72225846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c4426d365918accf7a8e02f2566f4b3b86b6f4f1779a902ebaf65775fbba84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 09:13:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 09:13:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 09:13:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_VERSION=8.4.20
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 10 Apr 2026 18:58:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 18:58:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 19:57:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 19:57:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 19:57:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 10 Apr 2026 19:57:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 19:57:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 19:57:13 GMT
CMD ["php" "-a"]
# Sun, 12 Apr 2026 06:40:39 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Sun, 12 Apr 2026 06:40:39 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Sun, 12 Apr 2026 06:40:40 GMT
WORKDIR /var/www/html
# Sun, 12 Apr 2026 06:55:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sun, 12 Apr 2026 06:55:48 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sun, 12 Apr 2026 06:55:57 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Sun, 12 Apr 2026 06:55:57 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Sun, 12 Apr 2026 06:55:57 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Sun, 12 Apr 2026 06:55:57 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Sun, 12 Apr 2026 06:55:57 GMT
VOLUME [/var/www/html]
# Sun, 12 Apr 2026 06:55:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 12 Apr 2026 06:55:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 12 Apr 2026 06:55:58 GMT
USER www-data
# Sun, 12 Apr 2026 06:55:58 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d64a68485fdb9ab2ec4159ac3e04e0bb79d9f1d037e580e928ca2b9604180f`  
		Last Modified: Wed, 28 Jan 2026 10:13:59 GMT  
		Size: 3.7 MB (3741000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b030c1b113432578231e8fe7c8a1bc913f2dc5dcba512e805fa9ab07768c9bd4`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a0e9bcb36b34307b4eada1f50c1cd4244d43d19ee57d962818dcb0ff0b110`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfdae87dce600eeda7208c98ae006cd061e7aa5aea7598748846f26db985a32`  
		Last Modified: Fri, 10 Apr 2026 19:58:24 GMT  
		Size: 13.7 MB (13709976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f61ec46e0eb851487ff35e9478305799f2d18216836fbf785f14606af80786`  
		Last Modified: Fri, 10 Apr 2026 19:58:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716fdc113cdf826c7dee1d30bfde5a40b99d10baa0e52a1816a1c5a126746e76`  
		Last Modified: Fri, 10 Apr 2026 19:58:25 GMT  
		Size: 22.5 MB (22507346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773a7d0a7b6d8453e8c1d92ada35692630fe6e633455b5521810141769074e73`  
		Last Modified: Fri, 10 Apr 2026 19:58:20 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d822e42b3e86a4a637876d96dfa4376da8806038f22a2eacdd897d9cac05b2e`  
		Last Modified: Fri, 10 Apr 2026 19:58:22 GMT  
		Size: 23.5 KB (23463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a24c4cd301221dac924b71a26ec7fca65c72b1c9fe27a48f8a35a341fa74f5`  
		Last Modified: Fri, 10 Apr 2026 19:58:22 GMT  
		Size: 23.5 KB (23478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ef6b9536840c9bce3c0705e7b577a906277dad289ff7b2e0f17273a265fca`  
		Last Modified: Sun, 12 Apr 2026 06:57:25 GMT  
		Size: 11.6 MB (11599222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b5584fe9856ff48bbfab4428e4bc3c2ac8766e0d8db90ca64488421b3d02a9`  
		Last Modified: Sun, 12 Apr 2026 06:57:26 GMT  
		Size: 15.5 MB (15495241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc63ea4a6c7382e11a8f2565b8659ae1f016b2a0cd1d6e3f0b5d8eee46dd508`  
		Last Modified: Sun, 12 Apr 2026 06:57:22 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9aaa55829799cd32953e3f66d436eff266710f09cc86c38343babfaf0ab46a`  
		Last Modified: Sun, 12 Apr 2026 06:57:22 GMT  
		Size: 1.5 MB (1535870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090581d788735b52c08957b4a8becb113cd7c8028ce24edd4e21d5d14c520082`  
		Last Modified: Sun, 12 Apr 2026 06:57:24 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:2afbb12574919ad4f7e91dc8ceade7cb8f0a51589ef241fe84a040474a305e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.4 KB (682360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852706ff556a2a4875d3c072112607ffbdc2e32a4830e6d6314f700a5a54ec28`

```dockerfile
```

-	Layers:
	-	`sha256:9bdb4611fa01396d415e391204b80bc1edc15869107d8c93b91b339c68a3d1fe`  
		Last Modified: Sun, 12 Apr 2026 06:57:21 GMT  
		Size: 640.2 KB (640207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d80529a3337cce761a62e20720f59ee0e4c7a4812e6f2ec7976882650b1cb719`  
		Last Modified: Sun, 12 Apr 2026 06:57:21 GMT  
		Size: 42.2 KB (42153 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.4` - linux; s390x

```console
$ docker pull wordpress@sha256:4684b2e3396ffc91e018f1d127b33698492f4840935cecdd51578d02ea4706ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72879668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0813223b1213cf2bf72b46986add1e64f584240935f29bf712f4e4d9d7bd3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:18:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:23:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:23:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:23:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:23:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:23:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:23:19 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 23:45:16 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 15 Apr 2026 23:45:16 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 15 Apr 2026 23:45:16 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 23:46:38 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 23:46:38 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 23:46:41 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 15 Apr 2026 23:46:41 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 15 Apr 2026 23:46:41 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 15 Apr 2026 23:46:41 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 15 Apr 2026 23:46:41 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 23:46:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 23:46:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 23:46:41 GMT
USER www-data
# Wed, 15 Apr 2026 23:46:41 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816b342f273c114d9278090832c6b271fa133343c6cc14c8db27aad0433c7e9d`  
		Last Modified: Wed, 15 Apr 2026 20:21:11 GMT  
		Size: 3.8 MB (3786986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40fd55f34e09a431ffb1541581fb4b2fad1c949d00d3718c054f6a585dedbbe`  
		Last Modified: Wed, 15 Apr 2026 20:21:11 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93e9efb3f33cff64fedaa7b934bccba27be41ab8437362ef089937721401080`  
		Last Modified: Wed, 15 Apr 2026 20:21:11 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adefa755b1cbede3245ba350573476b4438d2c3a375101c6553fcde8df5d943`  
		Last Modified: Wed, 15 Apr 2026 20:23:33 GMT  
		Size: 13.7 MB (13709892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c4adca3f5704531af4fde0978117a15a124923c7e965172a5d0bb1d9fd326e`  
		Last Modified: Wed, 15 Apr 2026 20:23:32 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3fe975d2e7ee22d027f6cb371742b70417d113a3c4b642d4e325e6f997ddaa`  
		Last Modified: Wed, 15 Apr 2026 20:23:33 GMT  
		Size: 20.0 MB (20024391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6b699a856ad8e3ec5380afba1c88a64d5fcd405183aeb1d541dca320aacc88`  
		Last Modified: Wed, 15 Apr 2026 20:23:32 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b4eea721c590e7779db5d3c81b3c3e869ccc57a726614803d4229d5c05de1c`  
		Last Modified: Wed, 15 Apr 2026 20:23:33 GMT  
		Size: 23.2 KB (23224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e2fa219a0477dd0795e0ab6c77ad7b12615ca62aabd7d95d9416d03cb20786`  
		Last Modified: Wed, 15 Apr 2026 20:23:33 GMT  
		Size: 23.2 KB (23247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba5c1648104ed49cf6603dfea6d56e1d7109d4df3f830724f8f95db008f5ce7`  
		Last Modified: Wed, 15 Apr 2026 23:47:00 GMT  
		Size: 12.5 MB (12527226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a60ed1f37597a5e7091e54a78bc41b1ef28535c1d375a4149d00a8c16f70c`  
		Last Modified: Wed, 15 Apr 2026 23:47:01 GMT  
		Size: 17.5 MB (17517592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a864718e1bdc0d5d62a1af61560b40d901b23a0cb258f2230ff7a3ec23928466`  
		Last Modified: Wed, 15 Apr 2026 23:47:00 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c77e24a92982632967f194cd7421286f66d8875fb084897618631682139ec2`  
		Last Modified: Wed, 15 Apr 2026 23:47:00 GMT  
		Size: 1.5 MB (1535628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5747f518973b77e34586b199d1513e6dd8daa5f15204bf27600ee4042e66917b`  
		Last Modified: Wed, 15 Apr 2026 23:47:01 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:c95038f1a07ef1df71d8359d283835250083dbbbb977bed17f933435abc409bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.3 KB (679301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0bd595d5908293982d7bb41aa79de9d998a866f639d233548121385077ef1a9`

```dockerfile
```

-	Layers:
	-	`sha256:7495d170fcdd93aceb250767e5b9db539f38f6a01bf010310f2d624bdc3e548f`  
		Last Modified: Wed, 15 Apr 2026 23:47:00 GMT  
		Size: 637.2 KB (637199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:273c288f6f6114c305003dc8cf1f415967b595de00b48aa22cba8962ac01327a`  
		Last Modified: Wed, 15 Apr 2026 23:47:00 GMT  
		Size: 42.1 KB (42102 bytes)  
		MIME: application/vnd.in-toto+json
