## `wordpress:cli-2.12.0-php8.2`

```console
$ docker pull wordpress@sha256:d0b35ad0088144986a98030610be002ee08c4d78b5c2c02cb88c789672f1013f
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

### `wordpress:cli-2.12.0-php8.2` - linux; amd64

```console
$ docker pull wordpress@sha256:8c7cd263a762755a5a37bca56343b0bde43de43ec16cd2f9715bb2eeee254e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66151190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606ef955cbc1f7b11452f5273580e8a8538af0d2457e1abcacaffeb1d155a650`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.2.29
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904fa379072fa40900cd00ec333f798fa379a3e0b89c80f6117f58d99f7b9407`  
		Last Modified: Thu, 03 Jul 2025 23:09:19 GMT  
		Size: 5.9 MB (5944407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee7af3ce7e55827f1ba002ac30c6072d5a337280e174118eb35eba80a579945`  
		Last Modified: Thu, 03 Jul 2025 23:09:18 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c40de23117d560a935a542a947c6bb1d06dbb2309234ba0e564f5c48a8c055c`  
		Last Modified: Thu, 03 Jul 2025 23:09:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1390974142152336cb67139a3401b94b0b7222e1c26dea286aacb2ec80783cf9`  
		Last Modified: Thu, 03 Jul 2025 23:09:19 GMT  
		Size: 12.2 MB (12183858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecab1abb78a571726dc2197b1199d8d7ad78749910662b2f9cd7dcf64a3de066`  
		Last Modified: Thu, 03 Jul 2025 23:09:18 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508937adbe8b0e2c15cbfde7871fb537c6d3f05366ae82bd64e54d1800d93263`  
		Last Modified: Thu, 03 Jul 2025 23:09:20 GMT  
		Size: 17.1 MB (17069658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c328b0848ffe9ad055e34bf22a59afcc834f82bc25824d5f54c125a3db1427`  
		Last Modified: Thu, 03 Jul 2025 23:09:18 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090258dbec727a0d334ffcc8ba6df46132df577cae72bd76e6a49cd70ab45052`  
		Last Modified: Thu, 03 Jul 2025 23:09:18 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052aff0e68bd704cec365ba264163e902d0dcc83310cd2200781909c31a43bb9`  
		Last Modified: Thu, 03 Jul 2025 23:09:18 GMT  
		Size: 20.2 KB (20202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9403e57483d335f028369985ba8f4165f615b9f9b5385f9e40650a077317f70`  
		Last Modified: Fri, 04 Jul 2025 00:12:50 GMT  
		Size: 11.1 MB (11070139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fe91485c91a36b5ddc3c74b628d32e34b4872002b4e0327b3a03ccbaa4676a`  
		Last Modified: Fri, 04 Jul 2025 00:12:54 GMT  
		Size: 14.5 MB (14515628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0e20531fb8ec67dc275f2315e6bd204541dccd46482ad8dc15a68a12e3cd64`  
		Last Modified: Fri, 04 Jul 2025 00:12:48 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c99238404a8dfaa784d72f5ad118e76c06e8c9e81a5909b4087190a32234c8`  
		Last Modified: Fri, 04 Jul 2025 00:12:50 GMT  
		Size: 1.5 MB (1525306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9a62c8642ca1495c8768c9b162ee35e60bdbfad66d159d717b39e40593a858`  
		Last Modified: Fri, 04 Jul 2025 00:12:49 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:4c0c4c286b4461b353b80034911acf5aa7758083246973b686ac0abad2400127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.3 KB (644343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef23c36c3f777cf6b5122837066b13b585585c2dec4531d5aff80a978882859d`

```dockerfile
```

-	Layers:
	-	`sha256:326622080809400a2f9159882a9ff1481be04488777c292f6dbf691fc68463c4`  
		Last Modified: Fri, 04 Jul 2025 04:19:58 GMT  
		Size: 601.0 KB (601040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b19698147d7969ff41974387c1c5fc50c9bfc7c7aeb468e1da1eaf7f6b0f7db9`  
		Last Modified: Fri, 04 Jul 2025 04:19:59 GMT  
		Size: 43.3 KB (43303 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.2` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:cc81888e988ad10461c94ac5a61d839f796bb0ec76404ab0cb69263a02999af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61489019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fa1dae1c8e5dbc123a3e5ef8c767fcfa1a938b79590ee1ee8841ae8c4427f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.2.29
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4ee62282ba45798eee9dfb091af41d630a8873a7e39fc99ca0dc4c7b645c5d`  
		Last Modified: Fri, 04 Jul 2025 00:01:14 GMT  
		Size: 12.2 MB (12183814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfde8895d2000b76b62727c74d397d749171b40510989774c2704b02550bcaa`  
		Last Modified: Fri, 04 Jul 2025 00:01:13 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f092cc9fa23546959e22a5970c5cec6b50a74ab646d6e6a69623c0c2a0fb3b`  
		Last Modified: Fri, 04 Jul 2025 00:01:14 GMT  
		Size: 18.6 MB (18583735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fc8f5516fd29a5ce298660e24116ca8755fecbd6db620a70b5b34a5d8e2fbc`  
		Last Modified: Fri, 04 Jul 2025 00:01:13 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e358221a0e8b23fcd86b48a218f9d409b2852f0c5a8db96c5a41f129699ca9ad`  
		Last Modified: Fri, 04 Jul 2025 00:01:13 GMT  
		Size: 20.0 KB (20001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ad467ca34b64b6f5c3becd0ad5f7ca103f6bad54bec80ec5f46656337ea088`  
		Last Modified: Fri, 04 Jul 2025 00:01:13 GMT  
		Size: 20.0 KB (19998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7861f067e0ca833ed0c3e35e31f0ab0c6a05f5843375ec5b6dfc71c5c3c0a982`  
		Last Modified: Fri, 04 Jul 2025 01:01:02 GMT  
		Size: 10.8 MB (10763620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811c4fc63c6122ba8d96a65eee2b05e6d76c40df6639d7050c4d42c1a3676e63`  
		Last Modified: Fri, 04 Jul 2025 01:01:04 GMT  
		Size: 11.5 MB (11454205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dfc7e622008411e9b76ae6f0863de224fce6860a1db1e35ea557c1fe161912`  
		Last Modified: Fri, 04 Jul 2025 01:01:01 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8efbebd8097a329c57d8ee7e9cf399e0a16510557362be111b8cf0bf9f6c2ab`  
		Last Modified: Fri, 04 Jul 2025 01:01:02 GMT  
		Size: 1.5 MB (1525299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba41fd999f87598d4897d979c19a16c2c21a6def155d7935dfca60954386086`  
		Last Modified: Fri, 04 Jul 2025 01:01:01 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:e4a7968cf49c4693f2e739f9553283bb97a065434fae9d6ec927247130906726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 KB (43248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a58ff02b3fe1621ba35fb0cc4817d12360dd3f154c6732ad52b917ec718ee8`

```dockerfile
```

-	Layers:
	-	`sha256:ab2cb41a183b1f804b91813fb2aa523dffac43f2e6e43bfc2331f6b075c8d1ac`  
		Last Modified: Fri, 04 Jul 2025 01:16:28 GMT  
		Size: 43.2 KB (43248 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.2` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:e14673146624b30edb23848af7b18517d52d0b6dd16158251cf10c5cec3f5276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60384716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc8f1497d6b8fcf01db17d026ef5d7b5fa2f7286076b9eb89f1a26a3f930d75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.2.29
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4850115fc99ef58d39ccdb152543870aa3fb14704b172d3fe472cccc1bff3e63`  
		Last Modified: Fri, 04 Jul 2025 01:46:01 GMT  
		Size: 12.2 MB (12183844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c82773d0467f11623ac0b360c9c4c5d03baa46594c5e11a459225ee229583b5`  
		Last Modified: Fri, 04 Jul 2025 01:46:00 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dae361e162d5c13d4efa304e6366055c6b2ccc8f5870eb0e6be79f66508d0a5`  
		Last Modified: Fri, 04 Jul 2025 01:46:02 GMT  
		Size: 17.4 MB (17430982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746e96e72096a37d235419fd0990889caabb451622b86b56dd7e0cf82516fe38`  
		Last Modified: Fri, 04 Jul 2025 01:46:00 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c6fa6b6abd4f4f7773a9d4bf6458b8dd3a5cbf68a3f2416731f1f9be4641ee`  
		Last Modified: Fri, 04 Jul 2025 01:46:00 GMT  
		Size: 20.0 KB (19994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ecb4e836188af59db18c5e290249c517936da2ea0c6662304b00cac6545841`  
		Last Modified: Fri, 04 Jul 2025 01:46:00 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6109cbba6e652bf6cf4a017ad73b1acb4f9e162f31ab662d379716451d69fd`  
		Last Modified: Fri, 04 Jul 2025 03:16:50 GMT  
		Size: 10.4 MB (10440436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d8c089db6c9e939bafe3adfb81f5cb2cf427bd8e9692ad0b23a57f4b33cb88`  
		Last Modified: Fri, 04 Jul 2025 03:16:51 GMT  
		Size: 12.3 MB (12292564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043c4f3ca7aafc7b5121d70ea65e544f6c9ece3cf2ac87ef102ce62d17f5a9f6`  
		Last Modified: Fri, 04 Jul 2025 03:16:49 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66030e9ac9cc28239a9d983467e31298605d1c688eecc723e3ea80ceffac03a`  
		Last Modified: Fri, 04 Jul 2025 03:16:50 GMT  
		Size: 1.5 MB (1525302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b9bf051d4c4a80e28acb60496dea68977ecb4994e01a6159b178a29e7bebc4`  
		Last Modified: Fri, 04 Jul 2025 03:16:50 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:d7c8b6d68e8efb30b349b41a9ef10a64e9977ea4f25e5b313835361a45f82991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.3 KB (643327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf3b27ac2011a1ea019341bd0b2ba377061428290cafcf6d8ef8a1ad635cfeb`

```dockerfile
```

-	Layers:
	-	`sha256:1a219af5a883439c119ec3fcc3f3b85fe4ef81106c701b643f5a37562124d71a`  
		Last Modified: Fri, 04 Jul 2025 04:20:04 GMT  
		Size: 599.9 KB (599864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85c57bc6557e5b6053691b0626ad1e3aaa9000a483f93c8772c51530a6c570ad`  
		Last Modified: Fri, 04 Jul 2025 04:20:05 GMT  
		Size: 43.5 KB (43463 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.2` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:49a53c6c19af6011526b9e2cce465b27c6da5e74dbb811c8221fb4036de60c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66390419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa6849f0fe99a723606eb4f80ad524ec1eaa4d3a7cb2dd1932634928771546a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.2.29
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73985aec8f2b878dbb559825b96bc42ecedc3f93d14e5f1b9a6ca2e1816299c`  
		Last Modified: Thu, 03 Jul 2025 23:26:01 GMT  
		Size: 6.2 MB (6231904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2edf112b2c5bea025053bf307e764ef87252d3b53a912374edb00c6b9cda47`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cb39859ac9004e783043bb75563ecfc6db5970ab2b1965a10cfec3c797d10`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85fad52315a324b6bcfa1bdfec74689faea510d6e706671c4d567af30b341d7`  
		Last Modified: Fri, 04 Jul 2025 01:22:47 GMT  
		Size: 12.2 MB (12183852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4e6f8300e0c16a72f565392f4be992fa53deabe8bde22f3ed0f7a10f5242c`  
		Last Modified: Fri, 04 Jul 2025 01:22:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff41e3d59ab930752d59e187fd98debf4914962d6efd35504f05d9d0f2b82ea`  
		Last Modified: Fri, 04 Jul 2025 01:22:47 GMT  
		Size: 17.0 MB (16989238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb078a67166ee6e8a7c11162d7160d94eb844ef745ff334537e74634438999a3`  
		Last Modified: Fri, 04 Jul 2025 01:22:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f83fb74e10c3cf045465b2c850981332451285363ecaa5fd61dfe343eaea4d`  
		Last Modified: Fri, 04 Jul 2025 01:22:45 GMT  
		Size: 20.0 KB (20009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6756ff7d80eb45bd8ae6721b25db992da0df7a3bf95bd8b0b7db0d0b9271d87`  
		Last Modified: Fri, 04 Jul 2025 01:22:44 GMT  
		Size: 20.0 KB (20001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2752a4ee13c0263c02a2c357c48048cc2b756d158d5c12261259a907da7a481a`  
		Last Modified: Fri, 04 Jul 2025 03:54:25 GMT  
		Size: 11.1 MB (11074425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01513c579a248cdfa063fd92c4fc0bbfaa765ff9fd050e7abb08b7c694ffe5b`  
		Last Modified: Fri, 04 Jul 2025 03:54:25 GMT  
		Size: 14.2 MB (14204789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea279f918fe1232abd9c46a88f99538621c9ec89f95d2d34862b8b36ec619ed`  
		Last Modified: Fri, 04 Jul 2025 03:54:24 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ada2130028e928ae412c107bb89ed81d5d6da66c473189b717a760390e7602`  
		Last Modified: Fri, 04 Jul 2025 03:54:25 GMT  
		Size: 1.5 MB (1525313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea80fb8c9a7f12013f3e840f494edd06791f68832418cb06929d114b0ea70da6`  
		Last Modified: Fri, 04 Jul 2025 03:54:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:7dc335001110d1552b2be204383c3465646e86ddb01132583b632b05c4e0d0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.4 KB (643415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1911dde715f121a7016d1e7b1a949d376ab6f18ec5bf5a0908895e57fbd24f40`

```dockerfile
```

-	Layers:
	-	`sha256:6502ea96ac14f75e17727dd5057347935281cbbb819e0b2bcc1d15abb328562d`  
		Last Modified: Fri, 04 Jul 2025 04:20:08 GMT  
		Size: 599.9 KB (599900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afec56abbb38de2cd371b7881af6ed7844657cad37f45d050e38755ed85ee52c`  
		Last Modified: Fri, 04 Jul 2025 04:20:09 GMT  
		Size: 43.5 KB (43515 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.2` - linux; 386

```console
$ docker pull wordpress@sha256:05c47e7ac1f877f0d7a7c61ff9d9c763aec456dc0ddc5e8f7a76f61875e30bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65323258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfae430fc5f6342932546b4e9b73de3b53069c1bbb210b9c6dcec13b9fb76dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.2.29
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4900832a3fd04a668c28403f5a3c51ae4e55237e71933b6238d18f86149f430a`  
		Last Modified: Thu, 03 Jul 2025 23:10:22 GMT  
		Size: 5.8 MB (5806963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fcbff0b80310e1e52eb0ad278ff1ba76a69006aff1d50d13f5ebe53172b6b1`  
		Last Modified: Thu, 03 Jul 2025 23:10:21 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a6ee27c9d70aafb2e7b517792dfa420b7fe98a7b67dd8f4531452c75a27e05`  
		Last Modified: Thu, 03 Jul 2025 23:10:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8105112e947a1e41c1977c41e9e1b8d80422c1e49ae36cd91832da5e45526927`  
		Last Modified: Thu, 03 Jul 2025 23:10:22 GMT  
		Size: 12.2 MB (12183832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06172a03596c89bccb36b643bddc487880f569e27ef0449354b75a2fc84ce3c9`  
		Last Modified: Thu, 03 Jul 2025 23:10:21 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab1bccce7fc09030c2529e8ca0163367058687c023afb5956e5f2ce6a3bc2f8`  
		Last Modified: Thu, 03 Jul 2025 23:10:23 GMT  
		Size: 17.5 MB (17506207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b813a3b526e6d2df7e0f580f15e2321f79ed4cf805af170f0227b21eb0bad689`  
		Last Modified: Thu, 03 Jul 2025 23:10:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d425aad731b620baa5fc2463f5342a2c981c922ecd88384ff1e09755128b35`  
		Last Modified: Thu, 03 Jul 2025 23:10:21 GMT  
		Size: 20.2 KB (20198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b8336b7404238f9cc1903500ed983e26a0cd7b1a0f9bbe8da4c3e53f13403`  
		Last Modified: Thu, 03 Jul 2025 23:10:21 GMT  
		Size: 20.2 KB (20189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b31ef99312f9ce0dca1d84f652245b75fc181a9c939348ae1bb30d022b825e`  
		Last Modified: Fri, 04 Jul 2025 00:13:11 GMT  
		Size: 11.3 MB (11271229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916491f2dfd6745a93c66262997a686df4b0df06b26b66863825307131909d1a`  
		Last Modified: Fri, 04 Jul 2025 00:13:10 GMT  
		Size: 13.4 MB (13368384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662648a5e9a99fba0c51cf8b391a5f21ea154331f692deeded2789bf47f44c99`  
		Last Modified: Fri, 04 Jul 2025 00:13:09 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362371d1b2a2211d69c9ca297e4db08f168b0423e23cebb0dd7d37bd64838656`  
		Last Modified: Fri, 04 Jul 2025 00:13:09 GMT  
		Size: 1.5 MB (1525282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ce79c0764447939c6893affd84f08f21bbcc80a7482a8ef10502ff36f5ea47`  
		Last Modified: Fri, 04 Jul 2025 00:13:09 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:55df5acb265ac11b1f42009770c975f2f83f3dbd674fad2a9abdb4b6c1a2d141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.2 KB (644238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04b6807d081f2b862af6a6ddd9ca13f11bd98eb51a6ddde1344fc6224df0542`

```dockerfile
```

-	Layers:
	-	`sha256:42fb349701b231b3686123f2ebbc9b02f2a50c2ee854d6c1c8f609cb73ca1262`  
		Last Modified: Fri, 04 Jul 2025 04:20:12 GMT  
		Size: 601.0 KB (600995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a315dda7f42866b911d21951b63dd2d4202bda85782b6a286be7e6a9dc5df39e`  
		Last Modified: Fri, 04 Jul 2025 04:20:13 GMT  
		Size: 43.2 KB (43243 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.2` - linux; ppc64le

```console
$ docker pull wordpress@sha256:a63912e32a71247a752cef61301b92fc0c0aed79745e3c3b3dc0610d70905c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67160630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3785a57984d2b88c7de32c4209e9988bf697a426af13de978645ef7dd30d3a19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.2.29
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790bf6906a4b16496902e6eba7e88ec69093d118faf89d335c5a519a51ddfab6`  
		Last Modified: Fri, 04 Jul 2025 00:32:28 GMT  
		Size: 12.2 MB (12183838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ac38a5597c0dc1fb42cdffbb60a8ce5c075565d6be2c890245e0f08ad7c0af`  
		Last Modified: Fri, 04 Jul 2025 00:32:27 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c68c82b9669a40e0181804b5dc0158913ed0be47668827b6891de397802c3a8`  
		Last Modified: Fri, 04 Jul 2025 00:32:27 GMT  
		Size: 17.9 MB (17911890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0602bf8a9ce965dc2d736e1a36268c77cd097365b371ebadbbd55cf84b5d4d`  
		Last Modified: Fri, 04 Jul 2025 00:32:26 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a90409f7877bc113c869bce5b935f5b7b6dabc89cb89d133b542dc250391dd7`  
		Last Modified: Fri, 04 Jul 2025 00:32:27 GMT  
		Size: 20.0 KB (20005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4278910a314b01eaa8bb9893bd6d63e3fbe7b49569615bb525305949e34e6a33`  
		Last Modified: Fri, 04 Jul 2025 00:32:27 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f123520574b0621e09a565df87f9c65a0ae7606ebfa78f3ad3a047617ee215e`  
		Last Modified: Fri, 04 Jul 2025 02:17:48 GMT  
		Size: 11.7 MB (11677625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c537436d29ae33c2a10fdbc6f7b1d3439793519842593d634d70f18ceb244ca`  
		Last Modified: Fri, 04 Jul 2025 02:17:50 GMT  
		Size: 14.1 MB (14139909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ed9a6f287540069454bac1228e686403419c161843a29bec13ca858dc58b23`  
		Last Modified: Fri, 04 Jul 2025 02:17:48 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8722d61fcfb7881a349d10d2fe24ac3429b9fdcc532cf1a890fb1611642878`  
		Last Modified: Fri, 04 Jul 2025 02:17:49 GMT  
		Size: 1.5 MB (1525297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfa08b68e6a0f73fa762522c4ffe4e3921f6007d291afbda5f6f4aabfbf23eb`  
		Last Modified: Fri, 04 Jul 2025 02:16:48 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:bf97969fad3f300d14e1088ac8f66532c188348b480f35495e4218973f21af51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.3 KB (641280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a24a32635703b4fc56483bacfd9b1423c9e05a6a12d24718d3798e4ce52455`

```dockerfile
```

-	Layers:
	-	`sha256:965ac5fe2f64ada997557d26dff3e88328500f7d37152f17489ee7bfd98e0b83`  
		Last Modified: Fri, 04 Jul 2025 04:20:17 GMT  
		Size: 597.9 KB (597903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b192caaa1decb05aea094df6b1527e7ab68634f26f2dd28341368453cc1afd86`  
		Last Modified: Fri, 04 Jul 2025 04:20:17 GMT  
		Size: 43.4 KB (43377 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.2` - linux; riscv64

```console
$ docker pull wordpress@sha256:214031b90b055e567438764460984e2496d83f8ac923f2a5849829853c03ac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63655775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ecff71349c320fc787c94212ac492cadab8752ed9687ae9407b58a437b14833`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.2.29
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c7222bbb28334b2afe139d1d92397d4be65c490f9bee5e6fcbf9d97d6279d3`  
		Last Modified: Fri, 04 Jul 2025 10:35:06 GMT  
		Size: 12.2 MB (12183843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557410c9f7cf55cb21958cba80b21371ef0cf8a6cb3dcf740205adf22747e07`  
		Last Modified: Fri, 04 Jul 2025 10:35:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7e76a1aa3da675d08a18e08b64f3d8ec74d53da3439d3fa2eccf891ed81d02`  
		Last Modified: Fri, 04 Jul 2025 10:35:07 GMT  
		Size: 19.4 MB (19375722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfc697621ad52169356808b30bb7bd8a2a1e5d6a852eab9f809a95a1cdef531`  
		Last Modified: Fri, 04 Jul 2025 10:35:04 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a835b3716ef04e2a90ab87bea4da172801e514179284ca1ec8862fd8d4587460`  
		Last Modified: Fri, 04 Jul 2025 10:35:04 GMT  
		Size: 20.0 KB (19999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e626409b7187ba48df30b302dda14d0d314a2cc5b2dec2294d6c4a71a549465`  
		Last Modified: Fri, 04 Jul 2025 10:35:04 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191d6e9c78756318afc41227bd4b283e77555b1af3109f0f7dd10fadd9ca6cd8`  
		Last Modified: Fri, 04 Jul 2025 21:05:27 GMT  
		Size: 11.5 MB (11527851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b861536963550a4655100a38e5fd6064b537d4b61523ddcfbfca1f8abc44fec`  
		Last Modified: Fri, 04 Jul 2025 21:05:27 GMT  
		Size: 11.9 MB (11880930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6657d19000a6840e7e31f9a14e9717447c569945aee94a707f6b7ad879686f`  
		Last Modified: Fri, 04 Jul 2025 21:05:26 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84523b6ae33e8ce87477e744701e9ad7561d483e79ce930ed8a58d07584f22e2`  
		Last Modified: Fri, 04 Jul 2025 21:05:26 GMT  
		Size: 1.5 MB (1525310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfc3676985967e2156b0f78c37309f6058c11fbb4e7f3a4252c4ca6001a4dc`  
		Last Modified: Fri, 04 Jul 2025 21:05:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:3ddcfd9d83565149dd0293db82d00af2795d13de3daed2211c0746265ff98575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.3 KB (641277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71cbf132df0c34a0cf563e4adb2d13ad4b9eabf917084b17b140199960aa2d1`

```dockerfile
```

-	Layers:
	-	`sha256:367b4b7c08645f2be0ab1572eaabb0d8c8438c31bc7470dabf778e5a2f07cc24`  
		Last Modified: Fri, 04 Jul 2025 22:14:30 GMT  
		Size: 597.9 KB (597899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63211b1f6e73cda7dea8285c7e1ff2511beb3d444b03b349277c43f47b79aa2b`  
		Last Modified: Fri, 04 Jul 2025 22:14:31 GMT  
		Size: 43.4 KB (43378 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.2` - linux; s390x

```console
$ docker pull wordpress@sha256:b5484152d391749f208d96eb0aa7fe27d7b0806c5b8777474910f594f4f296ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66735966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83770fd633b583edb96ec6d2e76e93d47b1fd594f6307403331b972568d30eea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 07 May 2025 07:03:15 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_VERSION=8.2.29
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Wed, 07 May 2025 07:03:15 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 07 May 2025 07:03:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 07 May 2025 07:03:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617af236d5ad95f5074829e2b22833cf0dbb14e4f4f1c63d84d242cbeedbd52f`  
		Last Modified: Fri, 04 Jul 2025 00:34:26 GMT  
		Size: 12.2 MB (12183857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00a9fd00815af9531706206a2f7d257a42885f8596f83748f7f19f6f2b8b902`  
		Last Modified: Fri, 04 Jul 2025 00:34:24 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8ca8a2ded44213ff66ef1aa1cbceb8e3ba2b3208c84440266dbab274b25e75`  
		Last Modified: Fri, 04 Jul 2025 00:34:25 GMT  
		Size: 17.1 MB (17147475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fa5e45ed0a8310e0a6527900b82d4de2d1458a3613e9ddf3f791942b81eec0`  
		Last Modified: Fri, 04 Jul 2025 00:34:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b67834330130c00c922ddd3356dc9fdd41be2924e13bddea3454514e50dce22`  
		Last Modified: Fri, 04 Jul 2025 00:34:24 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f60d71df41a7982ec9a99b0dc2b8b81df06a94ba6b4fbde2790c9813bfa7e29`  
		Last Modified: Fri, 04 Jul 2025 00:34:24 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a424c69504cb13ea600d204ccd7fc11d4b1b111b15bf5aa7efdde33817bc048`  
		Last Modified: Fri, 04 Jul 2025 01:55:17 GMT  
		Size: 12.4 MB (12425139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e857005abe12b6d5bbbe0c95184f925cfc0910b9295e6db2eba4fdb8ae173d29`  
		Last Modified: Fri, 04 Jul 2025 01:55:17 GMT  
		Size: 13.8 MB (13829168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350b613dbef99fbb6ee22f0293665b190595a064d16745acd5929a9453cfb950`  
		Last Modified: Fri, 04 Jul 2025 01:55:16 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e4dc2e00895b229cd5e4015532ff664fdb47593bb7727d19a31524e980cab5`  
		Last Modified: Fri, 04 Jul 2025 01:55:17 GMT  
		Size: 1.5 MB (1525298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d654eaddba1c210677541e45f710a28cd5d8c1c4e9110cc0fbf2d22eedf636`  
		Last Modified: Fri, 04 Jul 2025 01:55:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.2` - unknown; unknown

```console
$ docker pull wordpress@sha256:cbd9f7198f45782c6bc32230fbb247533ffa95155fd01bbfc2e652fe4142f1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.1 KB (641148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113baadcb181ed035acafd3ac2ad43426fab7941188dd7a1895da660dbb558e8`

```dockerfile
```

-	Layers:
	-	`sha256:a8457b3f00b5dc69503e7e10cf89e2abe8b6f88d9b25989f2c05f88b6c14a14d`  
		Last Modified: Fri, 04 Jul 2025 04:20:23 GMT  
		Size: 597.8 KB (597845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a12791b16e5e2af6cf39381ce87d5e69af9bc7dfd2e6e1235d63a36729b4a57`  
		Last Modified: Fri, 04 Jul 2025 04:20:24 GMT  
		Size: 43.3 KB (43303 bytes)  
		MIME: application/vnd.in-toto+json
