## `wordpress:cli-2.12.0-php8.5`

```console
$ docker pull wordpress@sha256:35b6b3486d29500979c6089d5de4ac197ef46a03ba45b79af4c5af73efc5edd1
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

### `wordpress:cli-2.12.0-php8.5` - linux; amd64

```console
$ docker pull wordpress@sha256:4c00357cd7d3c60ad24d6e634c39ad825a05e0879b2114d2220c759e4cf8513a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78545728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b86adc5ea695c03d1402bb6b89954a1fe54b5080886593eb5ed554699dd952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:53:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:53:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:53:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:53:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHP_VERSION=8.5.7
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 10 Jun 2026 20:53:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:53:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:57:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 20:57:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:57:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 20:57:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 20:57:04 GMT
CMD ["php" "-a"]
# Wed, 10 Jun 2026 21:15:32 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 10 Jun 2026 21:15:33 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 10 Jun 2026 21:15:33 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:16:22 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 21:16:22 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 21:16:24 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 10 Jun 2026 21:16:24 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 10 Jun 2026 21:16:24 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 10 Jun 2026 21:16:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 10 Jun 2026 21:16:24 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 21:16:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:16:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:16:24 GMT
USER www-data
# Wed, 10 Jun 2026 21:16:24 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eec522a523cd8996ce78e3a99e19af531a6e82199d7b3d922ea42dc16bbf6ab`  
		Last Modified: Wed, 10 Jun 2026 20:57:12 GMT  
		Size: 6.0 MB (5975963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03b878ed4b0c32142a9debaf795074fcfb7f97bada684da3d7970499ec8250c`  
		Last Modified: Wed, 10 Jun 2026 20:57:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9306d8986c54d88716638e932c65895c9da939b93ab385534c278e380995edd`  
		Last Modified: Wed, 10 Jun 2026 20:57:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dc19e1c0bad58da34b8c12b696f0caea74deeba6ad71224f02800d8a2d4129`  
		Last Modified: Wed, 10 Jun 2026 20:57:13 GMT  
		Size: 14.4 MB (14421890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f765cbf69390ee21751a543244a5de8e0a9e8e547a695f88be0216c2b71dcfa`  
		Last Modified: Wed, 10 Jun 2026 20:57:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399909e7c420dbfdb84d4ab87c20c5d80b5c27539ba5a922fa1b16d3c94ec684`  
		Last Modified: Wed, 10 Jun 2026 20:57:14 GMT  
		Size: 22.8 MB (22803596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbaa2b5042ebbbe740a84b544ecce389d952c2cddfa157cdaf601defe284c363`  
		Last Modified: Wed, 10 Jun 2026 20:57:14 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd40180fcb180475e23c54359836d65693599e62ab311e0496a420e1b160bdd6`  
		Last Modified: Wed, 10 Jun 2026 20:57:14 GMT  
		Size: 23.2 KB (23244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753456da197d5262368c288abfe214f96e8bab0b3635fe96e8afede3b9b4fa39`  
		Last Modified: Wed, 10 Jun 2026 21:16:33 GMT  
		Size: 11.7 MB (11704753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86895b88a0a6f7e0ed67c211448426d057017be4d2989d6a3c7f2433d202e9f6`  
		Last Modified: Wed, 10 Jun 2026 21:16:33 GMT  
		Size: 18.2 MB (18208807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f8b155a5c0060d68ea451d8095dde8bc628d808f1af95eecc0f2ea2d8e57a4`  
		Last Modified: Wed, 10 Jun 2026 21:16:32 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c653c0b8ba598fdfbfa31535716f286594695298cadd407013542274973317`  
		Last Modified: Wed, 10 Jun 2026 21:16:32 GMT  
		Size: 1.5 MB (1535769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63669d1ec9138386a3e6b0bdb0c3909aa68139ce64bf8bcbf583201d884a3e1`  
		Last Modified: Wed, 10 Jun 2026 21:16:34 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:cc5a6b1425ca368442f70298a39b733a36d043fc9bea6c9ab740e589c7bc9374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.8 KB (678785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5774694f15a56f761afebaa75959aefda5b942d670ccee78217aaa07fd9a5d26`

```dockerfile
```

-	Layers:
	-	`sha256:1b24fbc83aa1671a85f47b22a1617c761c7eaf5911c9b7ad4865a4edf5104fee`  
		Last Modified: Wed, 10 Jun 2026 21:16:32 GMT  
		Size: 637.9 KB (637946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a4400a3ca5fdc2a098ae4c6beddeeef7ec7e6e3d9cad7906c8df070a9dc51b1`  
		Last Modified: Wed, 10 Jun 2026 21:16:32 GMT  
		Size: 40.8 KB (40839 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.5` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:6043347795458b027b53629303ad8899c9f0f66fb7fc2d6427123037ff6b3835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71093232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f657c6e8400d13c8b58518e70e8461684513996503fb1d693d1c99a7d6f0541b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:41:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:41:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:41:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:41:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:41:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:41:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:41:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:41:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:41:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 10 Jun 2026 20:41:33 GMT
ENV PHP_VERSION=8.5.7
# Wed, 10 Jun 2026 20:41:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 10 Jun 2026 20:41:33 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 10 Jun 2026 20:41:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:41:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:44:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 20:44:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:44:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 20:44:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 20:44:44 GMT
CMD ["php" "-a"]
# Wed, 10 Jun 2026 21:27:40 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 10 Jun 2026 21:27:41 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 10 Jun 2026 21:27:41 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:29:26 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 21:29:26 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 21:29:29 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 10 Jun 2026 21:29:29 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 10 Jun 2026 21:29:29 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 10 Jun 2026 21:29:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 10 Jun 2026 21:29:29 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 21:29:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:29:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:29:29 GMT
USER www-data
# Wed, 10 Jun 2026 21:29:29 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8020ed5d93b43017267e5eb49e3420fc0bb7a351aaea2b2d3e6ac2ec16ed6ca`  
		Last Modified: Wed, 10 Jun 2026 20:44:51 GMT  
		Size: 5.6 MB (5569172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf4a3c9b1e0492065432755f84d74a894eb261396610516b5bfb796f5c2b57b`  
		Last Modified: Wed, 10 Jun 2026 20:44:50 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146565273e366a0f3fc3b71191fa5c3b0a61478f29748e07f157e8ae4081ae26`  
		Last Modified: Wed, 10 Jun 2026 20:44:50 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f133994d364cdf9b1a3afe7289e2c709b436257434b48c1663c9a30c6623b46`  
		Last Modified: Wed, 10 Jun 2026 20:44:51 GMT  
		Size: 14.4 MB (14421904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ad4f59af1244e742bf17a2c70d99c22bea82f1929da5c23b17b7c96e9ef2fa`  
		Last Modified: Wed, 10 Jun 2026 20:44:51 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48295a8b9877c7c3dc05d366963d0b05c5bbfd36900602a36981b847f8051eea`  
		Last Modified: Wed, 10 Jun 2026 20:44:52 GMT  
		Size: 19.8 MB (19753291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cf77d94c37b2c5d16450e9cea575ef9ec4775a316f4b7d6056be6f41185bbf`  
		Last Modified: Wed, 10 Jun 2026 20:44:52 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa3c3067b86ff998a7a43d4e989a75449e326954cd7b09f038c702d83ba922e`  
		Last Modified: Wed, 10 Jun 2026 20:44:52 GMT  
		Size: 23.1 KB (23051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e913a3ce8cc2a10439b9895704c53e70c08d2bd71c7cb65e4341b67bde0841b`  
		Last Modified: Wed, 10 Jun 2026 21:29:35 GMT  
		Size: 11.3 MB (11343342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f818b6ea4d6947728627877465ccab34d121e0a85096a24032c922a6a48ea8cd`  
		Last Modified: Wed, 10 Jun 2026 21:29:35 GMT  
		Size: 14.9 MB (14866446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395d5f6cc7cde48e3acf73ebf9f848a5a62c990070453ac42c677ade10b14b47`  
		Last Modified: Wed, 10 Jun 2026 21:29:34 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9515f917de9004a50445fd2994eab8d8d4ee537f8f70e16bcb492b13544aa6`  
		Last Modified: Wed, 10 Jun 2026 21:29:34 GMT  
		Size: 1.5 MB (1535766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514c7c8f72a230f5d814d510fa327af7d5858f8a3687ba529b29ffc6530a9caa`  
		Last Modified: Wed, 10 Jun 2026 21:29:35 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:9147b87c2c0dec1e1a40a1a55b48a5350ebc723643fd41c4fd3d89b8466d7e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83aef73d564ec6a9969263e98adcfa8855864723014d867f916cfa3eb763a52b`

```dockerfile
```

-	Layers:
	-	`sha256:a107806e7b21b2a7b602fb8a4eaa8c7c74032fbb4bdac03fba5e71ec1d84170e`  
		Last Modified: Wed, 10 Jun 2026 21:29:34 GMT  
		Size: 40.8 KB (40756 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.5` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:6a5df66f7b125dd7b8f5071217ffb9be55823f8b157dcf6b3d7737cc783e9879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69447851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17be3bd97f9d177fae63b121c300791e0d1960592c9c0bff8f085e0ef694235a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:54:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:54:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:54:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:54:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:54:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:54:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:54:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:54:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:54:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 10 Jun 2026 20:54:49 GMT
ENV PHP_VERSION=8.5.7
# Wed, 10 Jun 2026 20:54:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 10 Jun 2026 20:54:49 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 10 Jun 2026 20:54:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:54:52 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:58:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 20:58:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:58:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 20:58:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 20:58:03 GMT
CMD ["php" "-a"]
# Wed, 10 Jun 2026 21:33:19 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 10 Jun 2026 21:33:19 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 10 Jun 2026 21:33:20 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:35:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 21:35:15 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 21:35:17 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 10 Jun 2026 21:35:17 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 10 Jun 2026 21:35:17 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 10 Jun 2026 21:35:17 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 10 Jun 2026 21:35:17 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 21:35:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:35:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:35:17 GMT
USER www-data
# Wed, 10 Jun 2026 21:35:17 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6687cbb6f7b184bcfc568bf3c167f1147fe09f111bf607fac8224f1921bb51`  
		Last Modified: Wed, 10 Jun 2026 20:58:10 GMT  
		Size: 5.2 MB (5223385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c544b903995f77fea3079282988019fe28a3e43050cd7244d4b12f371dba01`  
		Last Modified: Wed, 10 Jun 2026 20:58:10 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3dcc2e444730d371e699befc2411a1baa06a309c96bf627508f746efc48873`  
		Last Modified: Wed, 10 Jun 2026 20:58:10 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930a365f952fbfee6bba95b06f7ad6878e9ecff02eafd3d40a19bb9ff0bab128`  
		Last Modified: Wed, 10 Jun 2026 20:58:11 GMT  
		Size: 14.4 MB (14421917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51707a05f772e237dd792042775f939477c9a25b51a0c99c917e09889fe09b1`  
		Last Modified: Wed, 10 Jun 2026 20:58:11 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d36d0a808509f79ce2d103fcc13e14f54e01c65cd85df2d97442d1f7d4d5a4`  
		Last Modified: Wed, 10 Jun 2026 20:58:12 GMT  
		Size: 18.6 MB (18641313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5103dddb2649647c80cf75e7920afa82fca67d0898236b9377ca4b2b0620c1f`  
		Last Modified: Wed, 10 Jun 2026 20:58:12 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5f6c54fc54bfcc7c040dd54b3b48563fde65378062b7dddcafea26c1020434`  
		Last Modified: Wed, 10 Jun 2026 20:58:12 GMT  
		Size: 23.1 KB (23066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203f5921475b4c1aed431974cd0ef564479485d17bc858b6e46699d6a3b67c23`  
		Last Modified: Wed, 10 Jun 2026 21:35:26 GMT  
		Size: 11.0 MB (10977031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09eb1dbb31299b1204d108a4c3d06110374896a52f7046ddd2aade143a22edab`  
		Last Modified: Wed, 10 Jun 2026 21:35:26 GMT  
		Size: 15.3 MB (15334272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3d0ef6a45c725bfc2a690815e75b70fd68fe4eb05083260e58b3f5d668ec7b`  
		Last Modified: Wed, 10 Jun 2026 21:35:25 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8256d88aff0ee41390e32f7e282a9b59c6d4cdf1d13a37a3ac07d9a44e5d33da`  
		Last Modified: Wed, 10 Jun 2026 21:35:26 GMT  
		Size: 1.5 MB (1535766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808106e337181f5e18c2e509f4d30ff72e4665e2d19caa832542da0f1992c98c`  
		Last Modified: Wed, 10 Jun 2026 21:35:27 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:559ebe09513df6991d7be9cbcb20143143905e916c9759cd2eacdd809dc92b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.1 KB (677061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490c603e7366765262a20a494728873bedf2cd3bc733b492e6b8cbe96a711a35`

```dockerfile
```

-	Layers:
	-	`sha256:23ec8d23cec27313d3879daebf39d1fee9fdf9fbd5628fdfd290bd7e645c1f1a`  
		Last Modified: Wed, 10 Jun 2026 21:35:25 GMT  
		Size: 636.1 KB (636090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8263cd40e452748284789dbc8d2fa7c731eeb74dc539e7662343bb709d654a`  
		Last Modified: Wed, 10 Jun 2026 21:35:25 GMT  
		Size: 41.0 KB (40971 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.5` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:27181690d0d5a0d108fbfa6681864a8529a981661f4b938a706b667c3fc752f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77384825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343927bead3e46b4b27112099c62795192adbacf9e74f51e1d6d62a811e54e12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:56:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:56:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:56:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:56:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHP_VERSION=8.5.7
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 10 Jun 2026 20:56:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:56:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:00:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 21:00:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:00:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 21:00:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 21:00:14 GMT
CMD ["php" "-a"]
# Wed, 10 Jun 2026 21:10:15 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 10 Jun 2026 21:10:15 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 10 Jun 2026 21:10:15 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:11:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 21:11:33 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 21:11:35 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 10 Jun 2026 21:11:35 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 10 Jun 2026 21:11:35 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 10 Jun 2026 21:11:35 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 10 Jun 2026 21:11:35 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 21:11:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:11:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:11:35 GMT
USER www-data
# Wed, 10 Jun 2026 21:11:35 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6ce2b7e213f0f2e1e2f67e3accfc7d3224dc3d6008a413369ab973adeca8c2`  
		Last Modified: Wed, 10 Jun 2026 21:00:22 GMT  
		Size: 6.3 MB (6287195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f96b81406b28ea7f1d59e53560b5e9a837cb667ae9a14bf540d0374f7e32ac`  
		Last Modified: Wed, 10 Jun 2026 21:00:22 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee434fed20582875063c2cb0526d9acf87f97642934668a643251c877ce3f1`  
		Last Modified: Wed, 10 Jun 2026 21:00:22 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aebc0c769d628ef197cbe4b64a27418325ca4b3c9dd3eb0433536d467df70cb`  
		Last Modified: Wed, 10 Jun 2026 21:00:23 GMT  
		Size: 14.4 MB (14421874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fb7c6a4cc00e7de73095956406865ffaa183191e07cb769bd11164216d4b2`  
		Last Modified: Wed, 10 Jun 2026 21:00:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df512ce2d699a6700fd9469da2cae7fffa572c63d15b56fd2f1097944bd70ee9`  
		Last Modified: Wed, 10 Jun 2026 21:00:25 GMT  
		Size: 22.0 MB (21982795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e67b4c903adabb3d1d2b14657d21c930909cd9b643c451ae54a8666eda7e96`  
		Last Modified: Wed, 10 Jun 2026 21:00:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4579febee26bb3e8d83996b6057c42d62c85b7eb74aeea3942a275733df8237a`  
		Last Modified: Wed, 10 Jun 2026 21:00:24 GMT  
		Size: 23.0 KB (23047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e133cd0132ed0b3772b3154b65718be29aeac5b5eef206965298e9c0b43cd7`  
		Last Modified: Wed, 10 Jun 2026 21:11:44 GMT  
		Size: 11.6 MB (11640111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f5ca164edf29fe4a52dd2f9b1b52fca5ada21aa18794c98d19747b884316cb`  
		Last Modified: Wed, 10 Jun 2026 21:11:43 GMT  
		Size: 17.3 MB (17286800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a88c65d89828ab137eb7b9cadd044dd95253fe4e88016e4fd876187bf9a1db`  
		Last Modified: Wed, 10 Jun 2026 21:11:43 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46b3d91150bbefeaba30cc4204352ef4107382b1b94d3c6cb40e09d1bd54edb`  
		Last Modified: Wed, 10 Jun 2026 21:11:43 GMT  
		Size: 1.5 MB (1535735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4be2703c3e53a1dc4caba3012d6a48206810e49cddf20f71835d3bd80420510`  
		Last Modified: Wed, 10 Jun 2026 21:11:44 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:6619b8e87594c3582bd745f59f6d63c0baeeca6b445a441d425f66059c61a24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.1 KB (677113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54a9231f73141acbd811a43c62a715bb8e89e4373a12e7beebde49548c8dcc1`

```dockerfile
```

-	Layers:
	-	`sha256:883d1774c88ca050d5aee468d5876d98c49266bdc770b42075485aeacc0aa380`  
		Last Modified: Wed, 10 Jun 2026 21:11:43 GMT  
		Size: 636.1 KB (636110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53d1050d8b4e8bba4e6bc2b54960b5b30ac725ee751ff000c4cf441ce52037c2`  
		Last Modified: Wed, 10 Jun 2026 21:11:42 GMT  
		Size: 41.0 KB (41003 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.5` - linux; 386

```console
$ docker pull wordpress@sha256:d0883b73400ba50a13af2b31267de53ce6413d13c04c6952c655ab966b4a34bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77884314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2390f9de116b1c325a93c22827081f49a3b9b4406febd1605f135d38b65a45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 21:31:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 21:31:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 21:31:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 21:31:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 21:31:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 21:31:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 21:31:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 21:31:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 21:31:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 10 Jun 2026 21:31:59 GMT
ENV PHP_VERSION=8.5.7
# Wed, 10 Jun 2026 21:31:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 10 Jun 2026 21:31:59 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 10 Jun 2026 21:32:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 21:32:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:35:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 21:35:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:35:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 21:35:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 21:35:50 GMT
CMD ["php" "-a"]
# Wed, 10 Jun 2026 23:11:02 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 10 Jun 2026 23:11:02 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 10 Jun 2026 23:11:02 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 23:12:06 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 23:12:06 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 23:12:08 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 10 Jun 2026 23:12:08 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 10 Jun 2026 23:12:08 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 10 Jun 2026 23:12:08 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 10 Jun 2026 23:12:08 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 23:12:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 23:12:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 23:12:08 GMT
USER www-data
# Wed, 10 Jun 2026 23:12:08 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4001affd3924faf720691c00dfcd72dc8ff7a398a4d4b6025edb61b3f8455a8f`  
		Last Modified: Wed, 10 Jun 2026 21:35:58 GMT  
		Size: 5.8 MB (5823670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60eeb38b0e554e0648d75c7acde172a75f0380f1d13997709924e48c75ea784f`  
		Last Modified: Wed, 10 Jun 2026 21:35:58 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2139ee7f91d16f8f35c1344b15734696e0fe336ab1344aace6a2c64c3391f02`  
		Last Modified: Wed, 10 Jun 2026 21:35:58 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf56f495e6593d837f0a3f813a2332bc3bc3e0b5e7e4a89a2f59dc4e0b60653`  
		Last Modified: Wed, 10 Jun 2026 21:35:59 GMT  
		Size: 14.4 MB (14421869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30a61b15d51651b83909a07f6fb6724af394fef4de46ef8ca9090ff80e3938d`  
		Last Modified: Wed, 10 Jun 2026 21:35:59 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9473bd19165c21b83a9a48ce039b4fda973a63f5bb0221efd7e27ef2a11290`  
		Last Modified: Wed, 10 Jun 2026 21:36:00 GMT  
		Size: 23.3 MB (23258042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ce69582a8ef3d005d5e59095887a1d2e923697835a7c0ec87846c2892f76a`  
		Last Modified: Wed, 10 Jun 2026 21:36:00 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beacb519008f12729ad87fae951c86998c2a7da2cd807d47b8029ec43584a70d`  
		Last Modified: Wed, 10 Jun 2026 21:36:00 GMT  
		Size: 23.2 KB (23227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eef32e9f3ee96a0e5e33afd5da7e15dc327f31c844b0959ff0bb5f7c686d4d0`  
		Last Modified: Wed, 10 Jun 2026 23:12:17 GMT  
		Size: 11.8 MB (11842907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6808d1f3c52e8e49b9afaa0420eb88cb93db3e6c4ee7215689f57e85180c67`  
		Last Modified: Wed, 10 Jun 2026 23:12:17 GMT  
		Size: 17.3 MB (17282203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4215e6016e6860f9576f7dafc388874fc379ffcaf876962655967e416aaac4c0`  
		Last Modified: Wed, 10 Jun 2026 23:12:16 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef162bd37bcc30d1719ad087dd8af6baded457286b02fea9667fb257cdb7906`  
		Last Modified: Wed, 10 Jun 2026 23:12:16 GMT  
		Size: 1.5 MB (1535702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd70e1ed73e5813ac4e8acaa664a8d4f890d621703671fe7ce66d41209ccf02`  
		Last Modified: Wed, 10 Jun 2026 23:12:17 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:fe007e2cb45bd30a2c2c9ff662c188f9ef7343c8ce06fd2e5c7bea212f779ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.7 KB (678719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ba5847e5f0267edea409a207f93563d46f74837506a52f2b2100614c7d3b56`

```dockerfile
```

-	Layers:
	-	`sha256:13ae1c7e117a95a8b016594d2db111a1cb5042d7bb42685281a0d784f7d7f700`  
		Last Modified: Wed, 10 Jun 2026 23:12:16 GMT  
		Size: 637.9 KB (637921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:399c00d1548774d35808e3f7cfa419558b830a6081b0fd8d299831dda84a4946`  
		Last Modified: Wed, 10 Jun 2026 23:12:16 GMT  
		Size: 40.8 KB (40798 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.5` - linux; ppc64le

```console
$ docker pull wordpress@sha256:455041e1759445ac1563d7dd80b2685c11514870e9100dcb974610812b8bba40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77319836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf839af4c6f30cb4327bf5fae55d4fe28c937f4543e6498670f7920322af6b0`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.5.7
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:34:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:34:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:41:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:41:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:41:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:41:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:41:51 GMT
CMD ["php" "-a"]
# Fri, 05 Jun 2026 02:13:05 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 05 Jun 2026 02:13:06 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 05 Jun 2026 02:13:07 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 02:15:18 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 05 Jun 2026 02:15:18 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 05 Jun 2026 02:15:22 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 05 Jun 2026 02:15:22 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Fri, 05 Jun 2026 02:15:22 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Fri, 05 Jun 2026 02:15:22 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 05 Jun 2026 02:15:22 GMT
VOLUME [/var/www/html]
# Fri, 05 Jun 2026 02:15:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 02:15:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jun 2026 02:15:23 GMT
USER www-data
# Fri, 05 Jun 2026 02:15:23 GMT
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
	-	`sha256:13a446573689f8d3cbef54f6c649ba454330116f9d75b4f418c595229567eb07`  
		Last Modified: Fri, 05 Jun 2026 01:42:07 GMT  
		Size: 14.4 MB (14422026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90449a89084b470b4d104decde8a8b7ad5984470fec6f94ef7574b58dc3b20b7`  
		Last Modified: Fri, 05 Jun 2026 01:42:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7dfa59a607b8d6f0abeae5a34ac3b1c360f61ba2e02f2f5648f9ab7aceaba1`  
		Last Modified: Fri, 05 Jun 2026 01:42:07 GMT  
		Size: 23.7 MB (23694906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fc109ed946a7e1ab29ae38cf1c6f153d28120da4b130e4afd9f9ca965ad4ff`  
		Last Modified: Fri, 05 Jun 2026 01:42:06 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af50033b42f1b773139e3d68c9fe3c24dd0f39a4118c03165a681d371a173bd`  
		Last Modified: Fri, 05 Jun 2026 01:42:07 GMT  
		Size: 23.1 KB (23068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52ae90e61150ddcecc900a8a3bcbeb65acc3287c1492ca2844ba60531a72e45`  
		Last Modified: Fri, 05 Jun 2026 02:15:45 GMT  
		Size: 11.8 MB (11831078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5461d47431315c927a3ed515c4f7dfef19bd8444e541eaa7cf5b984b7ea6f02b`  
		Last Modified: Fri, 05 Jun 2026 02:15:45 GMT  
		Size: 18.2 MB (18210284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437fad7f0258f0d3e5e0573674f4ea7e70c0fcbe9b102397fec47a7885d4cc0e`  
		Last Modified: Fri, 05 Jun 2026 02:15:44 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f366b23d48cae986813d00e34054ceeecb0f3c48e5834135b909c773ff3982e`  
		Last Modified: Fri, 05 Jun 2026 02:15:45 GMT  
		Size: 1.5 MB (1535494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78793fd6858d567255ff86d05cb7c8d38c72568001bfa968212974845043b27`  
		Last Modified: Fri, 05 Jun 2026 02:15:46 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:00cb318408aafa277457cf88259a82bbc05fa14e12a68388dea68b367bae8362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.3 KB (675279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca02fbab3388ad29e266e54e2b89ce68620a80796b8bb091b4099c24c8df229`

```dockerfile
```

-	Layers:
	-	`sha256:179da99b2a514873ac70337b91949b01757e8f53d35ef577dfa8719219e71edc`  
		Last Modified: Fri, 05 Jun 2026 02:15:44 GMT  
		Size: 634.4 KB (634388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e34fc43e06ffa14eec928fc3129612e9837ba46af296ab6644d496193999262`  
		Last Modified: Fri, 05 Jun 2026 02:15:44 GMT  
		Size: 40.9 KB (40891 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.5` - linux; riscv64

```console
$ docker pull wordpress@sha256:1a2dbf23cc97df3f0d7f639c42a5e60282b094bb7b78f99f1ef56c8a367524a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72250855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0594639bf32f91e37b9070a20fb41182b18eae6d5b59796dec06888e1ffd49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 16 Apr 2026 00:30:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Apr 2026 00:30:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_VERSION=8.5.7
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 05:18:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 05:18:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 13:29:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 13:29:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 13:29:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 13:29:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 13:29:14 GMT
CMD ["php" "-a"]
# Fri, 05 Jun 2026 14:09:33 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Fri, 05 Jun 2026 14:09:33 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Fri, 05 Jun 2026 14:09:33 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 14:32:44 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 05 Jun 2026 14:32:44 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 05 Jun 2026 14:32:53 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 05 Jun 2026 14:32:53 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Fri, 05 Jun 2026 14:32:53 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Fri, 05 Jun 2026 14:32:53 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Fri, 05 Jun 2026 14:32:53 GMT
VOLUME [/var/www/html]
# Fri, 05 Jun 2026 14:32:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 14:32:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jun 2026 14:32:53 GMT
USER www-data
# Fri, 05 Jun 2026 14:32:53 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78828518b8b5af0bc74ba3bd169a5c835b32f2a1452a7cd03ad8117a0128165b`  
		Last Modified: Thu, 16 Apr 2026 01:32:16 GMT  
		Size: 3.7 MB (3734242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1c9b4ddefe159b602dd6cdf3bcfff1bf48c922a0f1047bb5402dc2c6c988b`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2a62067bd9660d4987f0df8c18a9ac2818a33d0443ac9c5c806eb7925b9957`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83c25d050b633c94fba50d279b2d7b6c29826b999bd81a90516a78c942ae19d`  
		Last Modified: Fri, 05 Jun 2026 06:38:29 GMT  
		Size: 14.4 MB (14422060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabf9ca2a5430c85237d5dcabacf556b0831ae8c97d72577a9fab19b67f2b0de`  
		Last Modified: Fri, 05 Jun 2026 06:38:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf05bc16fb6654c65ce48a229ed109ffa89016258a4e875a440577a9809546c6`  
		Last Modified: Fri, 05 Jun 2026 13:30:22 GMT  
		Size: 21.7 MB (21717742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e4fb6647f78b90cc786f738c07cf3bc3e225e173ccbc81385c79ae93611ec2`  
		Last Modified: Fri, 05 Jun 2026 13:30:19 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1793e23d27fed29fc925dba04cab7c6eefb78fa3166a4e763918b7f1d50e0422`  
		Last Modified: Fri, 05 Jun 2026 13:30:18 GMT  
		Size: 23.1 KB (23082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bac2fe77e6dd0858024463c33f7f798482d37c15d6a1c983c239938847c180`  
		Last Modified: Fri, 05 Jun 2026 14:34:26 GMT  
		Size: 11.7 MB (11658840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1de840da548b2eb139c0e41285c119aab1668f544443a297c46b423a04aa483`  
		Last Modified: Fri, 05 Jun 2026 14:34:26 GMT  
		Size: 15.6 MB (15566789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fc90b90f83a0ab2141cc9dc778246382c89d9edcf48f261cc8eac8c0977a48`  
		Last Modified: Fri, 05 Jun 2026 14:34:22 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f45927e43cfe07c6ac98e3be795fe5c346b1090fea1df1a3291d6270e8e482`  
		Last Modified: Fri, 05 Jun 2026 14:34:23 GMT  
		Size: 1.5 MB (1535477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1fa0f55be6728e36b279bbc6fd3145818b736f98374bf12a03be27b1742207`  
		Last Modified: Fri, 05 Jun 2026 14:34:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:d33c097ee8c91b071d6de18da37288aa9ba40d9c2e4854ed1cc2b96cead3c413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.3 KB (675275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f86147562d6a6a87fcbeced65f68cae2dbdda48aac283210f18a4ed4b27a4ee`

```dockerfile
```

-	Layers:
	-	`sha256:2c19ab8411af73e7f7f182d2305878581784fbbd0570ecb3f28cc0d5c43e047a`  
		Last Modified: Fri, 05 Jun 2026 14:34:22 GMT  
		Size: 634.4 KB (634384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e89a0a2554e082bf09688b6b42655d86c105d5407db324d09f57f8dce2c28b4`  
		Last Modified: Fri, 05 Jun 2026 14:34:22 GMT  
		Size: 40.9 KB (40891 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2.12.0-php8.5` - linux; s390x

```console
$ docker pull wordpress@sha256:8ce2b6f90261fe523da4a62cb59e44c07ea4106c8b2d4204bd1e59e7b941729e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77866473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6a3298297808bee1c7c1c42c0ec2c2a01e6b3bcd331412f059b5235e20d206`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:59:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:59:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:59:37 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:59:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:59:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:59:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_VERSION=8.5.7
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 10 Jun 2026 20:59:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:59:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:05:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 21:05:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:05:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 21:05:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 21:05:45 GMT
CMD ["php" "-a"]
# Wed, 10 Jun 2026 21:59:30 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Wed, 10 Jun 2026 21:59:30 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Wed, 10 Jun 2026 21:59:31 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 22:00:59 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 22:00:59 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 22:01:02 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 10 Jun 2026 22:01:02 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Wed, 10 Jun 2026 22:01:02 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Wed, 10 Jun 2026 22:01:02 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Wed, 10 Jun 2026 22:01:02 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 22:01:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 22:01:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 22:01:02 GMT
USER www-data
# Wed, 10 Jun 2026 22:01:02 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b3da918cbfec773715cb5c2ba09c98813438f50a50d3430a86242f9c3ace75`  
		Last Modified: Wed, 10 Jun 2026 21:06:04 GMT  
		Size: 5.9 MB (5943440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d360246fb66915c6b8442bb5acd4465ad8e9cb2f0adb4488237ce2913320143`  
		Last Modified: Wed, 10 Jun 2026 21:06:03 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed332689978f619c05676c7b3c891e5c4e1deced85ca5ffcbcf5b048210f92d8`  
		Last Modified: Wed, 10 Jun 2026 21:05:15 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c98d2e55df3a968d41bfe27ffed7542089da32070461cf6cd8a6c3f5465653e`  
		Last Modified: Wed, 10 Jun 2026 21:06:04 GMT  
		Size: 14.4 MB (14421886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bfe5d067775dcf75677b829c39bfdd990c8aa2537353e8ba2ed660991a4c66`  
		Last Modified: Wed, 10 Jun 2026 21:06:03 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7d6cac3d30b8afc1b0f09979737069463abf919af9547f080c3dc5d6d442f6`  
		Last Modified: Wed, 10 Jun 2026 21:06:05 GMT  
		Size: 21.7 MB (21653849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80600163203bbf3a809e35d170309d27ccdb81ba48f6fd83b0807c3e238819`  
		Last Modified: Wed, 10 Jun 2026 21:06:05 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0d641b19d934bbbb9939e9f91297ed19cb6c83a63fd365a91abd32936a1f75`  
		Last Modified: Wed, 10 Jun 2026 21:06:05 GMT  
		Size: 23.1 KB (23065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd720ee548449027f7ccee23b8c63ec60df75489d62a70273b5b34aa18714c6`  
		Last Modified: Wed, 10 Jun 2026 22:01:16 GMT  
		Size: 13.1 MB (13126140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f73af2927fe50b117fbb235fe2c433c83fc95473c131e3112420bac26202005`  
		Last Modified: Wed, 10 Jun 2026 22:01:16 GMT  
		Size: 17.4 MB (17427159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0457a99e84bd59d83a99f7506f0b8bcc493538901cb2c8b96492d933b924f6e`  
		Last Modified: Wed, 10 Jun 2026 22:01:16 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0d2e49e866f5c48a5ded00a969f4cf1ab36c4d54aaada45f345d55d2b79844`  
		Last Modified: Wed, 10 Jun 2026 22:01:16 GMT  
		Size: 1.5 MB (1535775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f908da0d204682351ef8010b757fb7c752d463a873f22702732c739668dcb20a`  
		Last Modified: Wed, 10 Jun 2026 22:01:17 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2.12.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:0c7677996b16b50ce245442b5c5a74e6202c155d37c8dbce1eed4c538d965efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.9 KB (676892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f343765760fe1f2d133579fcb1ad2f589fa558e09e72b5ba53749315af58b0f2`

```dockerfile
```

-	Layers:
	-	`sha256:69e742087ff41ac5b814d8fce77dda6f95e6e66deabf8fb85663f7774aa11bb4`  
		Last Modified: Wed, 10 Jun 2026 22:01:16 GMT  
		Size: 636.1 KB (636053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8776ec088a52a4bb4d27cf3e97dd1e99892089af7706a4abcbbe73335ffd25f5`  
		Last Modified: Wed, 10 Jun 2026 22:01:16 GMT  
		Size: 40.8 KB (40839 bytes)  
		MIME: application/vnd.in-toto+json
